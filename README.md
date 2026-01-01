# engine-mode-controller
Embedded C/AUTOSAR portfolio: powertrain sim, BSW, functions practice.

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

As shown in the diagram above, the BSW layer is a structure of three components (or layers):

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

Since this is also an abstraction layer, it hides its low-level functionality and works independently from the upper layers such as application and RTE.

All these three layers of BSW make sure that the architecture is isolated and consistent across microcontrollers and ECU. Due to this, if any other software needs to be run on MCAL or another ECU is required, it can be done very easily.

AUTOSAR: Better software, lower costs
The main motive for shaking hands on a fixed standard is to increase portability and minimize costs.

If a vendor suddenly increases the price of ECU, why should companies bear the costs of shifting their methodologies to a new architecture or making new vendors adapt to theirs?

Porsche Turbo S dashboard
AUTOSAR eliminates these scenarios and provides a standard layered architecture followed by OEMs in their ECU communications.

To summarise, the primary benefits of AUTOSAR layered architecture are as follows:

Higher-quality ECU software
Lower development costs
No need to re-develop similar ECU software components repeatedly for the same applications
This post was all about AUTOSAR layered architecture and the layers underneath them as well. We tried to explore their working and impact on the overall system of microcontrollers and ECU.

I hope this post enlightened you about AUTOSAR and related technologies. Thank you for giving this post your valuable time.

The information contained in this blog post is provided for informational purposes only and should not be construed as an endorsement or advice from GoDaddy on any subject matter.

Frequently Asked Questions
Here we define a few concepts that will make the picture clearer.

What is an ECU?
An ECU is abbreviated for Electronic Control Unit or sometimes called Engine Control Unit with respect to automobiles.

An ECU is the brain of the vehicle, without which even the car’s engine would not ignite.

This device controls almost everything that happens inside a car. For example:

Airbag control during crashes
Maintaining the required temperature in the cabin
The ignition and the fuel injection into the engine
In earlier times, OEMs used a single ECU that could perform all the necessary operations alone. But as the vehicles improved and became more complex, you may find more than 100 ECUs with dedicated functions today.

This is a better strategy, as if one ECU goes down, the car would not stop (unless it is engine-related ECU).

What is a layered system architecture?
A layered system architecture is the most common type of architecture used in software development or electronics equipment development.

This is done to separate various components of the complete system according to their logic or working. A layered system architecture is made up of layers laid down horizontally one on top of another. Since these layers contain these components and separate them logically, the layered system architecture is often referred to as the “logical separation of the system.”

Layered system architecture may look generally as follows (not necessarily relating to AUTOSAR):

Diagram showing layered architecture
Source
Each layer in such a system holds a responsibility to perform. For instance, the presentation layer deals with a visual representation of components. So, all the components it holds are related to the same job.

Here, in the above image, you can notice the closed rectangle for each layer. This is done to represent the isolation of features. When we isolate these components, the debugging, development and maintenance become easier.

The layer may talk to the one above it (passing the data) or below it (receiving the data). There are no other connections between any other two layers, however.
