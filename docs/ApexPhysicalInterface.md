## Neptune Apex Physical Interface

On the surface, [Neptune Apex Aqua Controller](https://www.neptunesystems.com/) appears to be using a standard USB cable to connect to various modules. As mentioned in Apex documentation, this is actually not a USB interface, but rather a different interface that uses USB cables and sockets. Collectively, the Neptune's commercial name for the interface is AquaBus. 
At the physical layer, AquaBus is implemented using a standard CAN transciever. Many Apex Classic modules are found to use [MAX3059](https://datasheets.maximintegrated.com/en/ds/MAX3058-MAX3059.pdf) transceiver. It is important to note that this is not a CAN controller, but rather a CAN transceiver connected to UART of a basic controller for the purpose of converting CANbus signal to be UART compatible. The rest of the protocol is handled by a controller based on standard UART communication.

![Example 1. Aquabus CAN Transceiver Schematics](https://github.com/Stonyx/AquaBusLib/raw/master/docs/AquaBusSchematic1.JPG)