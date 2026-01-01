# engine-mode-controller
Embedded C/AUTOSAR portfolio: powertrain sim, BSW, functions practice.

AUTOSAR: 60mins

Application layer in AUTOSAR
The application layer is the topmost layer in AUTOSAR architecture. It is designed to work for specific tasks and execute the software components involved in that task.
For instance, dimming the light of the vehicle is something that the application layer handles.

Runtime environment (RTE)
The middle layer is the runtime environment layer that handles the communication part between various components. RTE takes care of communication between different ECUs, within the same ECU, between the basic software layer and application layer, etc.
RTE handles the tasks with the help of port interfaces that transfer data using data buffers.

Basic software (BSW)
The final and lowermost layer of AUTOSAR layered architecture is the basic software layer, popularly called as BSW layer.
This layer holds the responsibility of providing services to the AUTOSAR software components.
BSW contains modules standardized for functional use by the upper layer and structured into different layers that perform different jobs.
The modules are common to any other ECU working on AUTOSAR standards and hence make it easier to port or transport.
The microcontroller is the hardware part (not involved as a layer) that takes the instructions for processing further.
BSW layers and their tasks
BSW is an important layer with its own layered architecture underneath. Therefore we may need to detail it a bit more than its brief introduction.

As shown in the diagram above, the BSW layer is a structure of three components (or layers)
Service layer
ECU abstraction layer
Microcontroller abstraction layer

BSW - Service layer
The topmost layer of BSW is the service layer that remains unaffected by the bottom two layers’ work.
The main work of the service layer is to provide services from/to the application layer to/from the microcontroller.
These services vary in a wide range such as network services and memory services.

BSW - ECU abstraction layer
The second layer of BSW works on managing the ECU-related functionalities such as input-output or memory related etc.
This layer is called abstraction because it hides the low-level arrangement of ECU with the developer such as ports and hardware peripherals. It provides APIs that can access the ECU directly by calling them and connecting with the microcontroller.

BSW - Microcontroller abstraction layer
The last layer of BSW is the microcontroller abstraction layer, popularly called MCAL. Its responsibility holds with the hardware connection or simply the microcontroller. It holds the software for the drivers that connect with the microcontroller for further operations.

What is a layered system architecture?
A layered system architecture is the most common type of architecture used in software development or electronics equipment development.

This is done to separate various components of the complete system according to their logic or working. A layered system architecture is made up of layers laid down horizontally one on top of another. Since these layers contain these components and separate them logically, the layered system architecture is often referred to as the “logical separation of the system.”
Layered system architecture may look generally as follows (not necessarily relating to AUTOSAR):
Each layer in such a system holds a responsibility to perform. For instance, the presentation layer deals with a visual representation of components. So, all the components it holds are related to the same job.
Here, in the above image, you can notice the closed rectangle for each layer. This is done to represent the isolation of features. When we isolate these components, the debugging, development and maintenance become easier.
The layer may talk to the one above it (passing the data) or below it (receiving the data). There are no other connections between any other two layers, however.


C : 60 mins
Functions: Declaration and defination 

int fun(int var1,char var2);

int add(int a , int b);
{
int sum;
sum =a+b;
return sum;
}

int torque_calc(int rpm , int load)
{
return(rpm*load)/100;
}
int main()
{
int t=torque_calc(3000);
}


German A1: Dulingo 
Numbers
0-null
1-eins
2-zwei
3-drei
4-vier
5-funf
6-sechs
7-sieben

words
orangen-oranges
kostet-costs
wirklich-reallly
wie vie-how much
