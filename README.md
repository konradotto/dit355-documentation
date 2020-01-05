# Visual Transportation Support System 
A Visualization tool to assist city planners and Västtrafik with identifying bottlenecks and blindspots around the city which supports their decisionmaking. 


## Navigate in Readme

* [About](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#about)
* [Software Explained](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#software-explained)
* [Architectural Styles](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#architectural-styles)
* [Forces and Drivers](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#forces-and-drivers)
* [Architectural Modelling](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#architectural-modelling)
* [Structural diagram](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#structural-view)
* [behavioural diagram](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#behavioural-view)
* [Use case diagram](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#use-case-view)
* [deployment models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#deployment-view)
* [Files](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master#files)


## About
This is a repository that documents the system.

It consists of sprint plans, requirements, user-stories, architecture, cost analysis forces and drivers amongst other things.

The system will provide useful information such as location, destination, timestamp of travelers, the purpose of travel as well as issuance. 

Transportation companies can use this tool to improve their services through visualization of the travellers data.

The visualization will allow the service provider to identify blindspots and routes which will assist the decision-making of the city planners.


## Software Explained

*  Mosquitto -  It is an infrastructure for the publish and subscribe architectual style
*  Swift - Used to visualize the data on IOS devices
*  Python - Used to generate data and subscribe to topics 
*  Paho - provides mqtt protocol

## Architectural Styles
Software architecture allows us to plan the structure of the system in beforehand so that
we can foresee possible risks, reduce complexity and development time.

The Architectural styles we are using are:
* Publish and Subscripe
* Pipe and filter

##### Publish and subscribe
Subscribers subscribe to a topic they are interested in.
Publisher sends messages and subscribers of that topic recieves them.
Publishers do not know who the subscribers are and vice versa.

##### Pipe and filter
Pump feeds the data which pipes transport.
The data in turn gets transformed in the filer which pipes then transport to the sink.
The sink feeds out the data.

For more details and models read [Architectures](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

## Forces and drivers: 
##### Forces:
* Security
* Availability
* Scalability
* Modifiability
* Modularity

##### Drivers:
* Scalability
* Modifiability
* Security
* Modularity

 Read [forces and drivers](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/ForcesAndDrivers.md) for additional details and description.


## Architectural modelling: 
With the requirements and our user stories, we have created models.

Each model represent a view of the system.
* Structural view
* Behavioural view
* Use case view
* Deployment view 

### Structural view

#### IOS Class diagram
![Class Diagram](Architecture/IOSClientClassDiagram.png)

* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

__________________________________________________________________________________
#### Publish subscribe component diagram 
![Component Diagram](Architecture/ComponentDiagram_Version4.png)
* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

#### Conceptual component pubsub & pipe n filter - diagram __________________________________________________________________________________
![Conceptual Component Diagram](Architecture/component_diagram_conceptual.jpg)

*  to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/Architecture/component_diagram_conceptual.jpg)
__________________________________________________________________________________

#### IOS Client component diagram
![Component Diagram](Architecture/IOSClientComponentsDiagram.png)
* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

__________________________________________________________________________________


### Behavioural view
#### Get traveler behaviour

![Sequence diagram](Architecture/Get_traveler_behaviour.jpg)
The user(Västtrafik) chooses to view traveler behaviour. The visualizer will then subscribe to the relevant topic from the broker that is getting publishes from our generator.  The coordinates goes through a filter so that whatever is relevant is given to the visualizer. If the amount of data points received by the visualizer is less than a certain threshold it will render the map and show it to the user.

If the amount of data points are more than the threshold the circuit breaker will stop the inbound data temporarily, the visualizer will keep rendering the map with the data points it has already received and tell the circuit breaker when it is ready to receive more data points.

* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

__________________________________________________________________________________

#### IOS behavioural view
![Sequence diagram](Architecture/IOSClientBehaviourDiagram.png)
* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

__________________________________________________________________________________

#### Use case view
![Use Case diagram](Architecture/use_case_diagram.jpg)
* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)

__________________________________________________________________________________

#### Deployment view
![Deployment diagram](Architecture/DIT355_Deployment_Diagram_v1.png)
* to get download version of the model visit  [Models](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)
__________________________________________________________________________________


## Files
* [User stories](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/UserStories.md)
* [Requirements](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/SoftwareRequirementSpecification.md)
* [Forces and Drivers](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/ForcesAndDrivers.md)
* [Cost analysis](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/CostAnalysis.md)
* [Project management documetation](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/ProjectManagementReport)
* [Architectures](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/tree/master/Architecture)
* [JSON structure](https://git.chalmers.se/courses/dit355/2019/group-9/dit355-project-documentation/blob/master/jsonTemplate.json)







