# Forces and drivers:
## These are the forces we will use in our project: 
* Security: Important to reduce risk of malware that could potentially corrupt or steal data provided by users.
* Availability: System should always be live and ready to perform a given task when needed
* Scalability: Allows the system to scare without the need to reconstruct the entire system
* Modifiability: Allows the system to be adapted to be modified to perform tasks it was not initially designed to perform.
* Modularity: allows us to change a piece of code without breaking the entire system. 

### Driver - Scalability
* The system needs to be scalable so that Västtrafik can expand their area of travel and their customer base with ease,
* the system shall handle any increase of data being added.
Scalability would be a driver in our case as it is important to focus on this aspect early on in the development.

### Driver - Modifiability
* Adding more features to our system will be important as more requirements will come later on in the development process,
we will have to think about how we design our system early on so that adding more functions is easy. Modifiability is a driver

### Driver - Security
* The security aspect is very important since we are using data provided by the customer in the form of their information and location.
If this aspect of our system would fail the consequences would be detrimental,
västtrafik could get into legal problems and the traveler could possibly have their position and travel times leaked.

### Driver - Modularity
* Since we are developing a distributed system modularity is an important aspect in the development process.
Each component should work independently of other components without breaking the entire system.
This Driver is also increasing the maintainability of our code.
