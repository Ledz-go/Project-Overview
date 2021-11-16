# Project-Overview
The architectural and logical overview for the LEDZ GO project

## General Architecture
The image bellow describes the general architecture for the project. We can distinguish 3 different agents in the project :
- **Smartphone** : Containing the application the user will interact with
- **Master Node** : Receiving the commands from the smartphone and dispatching it to the other nodes
- **Nodes** : Receiving the commands from the Master Node and translates it into a DMX signal to the DMX light

We can also distinguish 3 different connection types:
- **Smartphone - Master Node** : Via bluetooth
- **Master node - Nodes** : Via WiFi
- **Node - DMX Light** : Via DMX signal

![Architecture Plan](https://github.com/Ledz-go/Project-Overview/blob/main/images/Architecure.png)

## Team Work
The project is divided into 4 parrallel workflow :
- Communication Layer 
  - WiFi connection between Nodes and Master Node
  - SSID and general parameters configuration for automatic connection
  - *"Plug and Play"* feature 
  - TCP/UDP socket 
  - Network maintenance protocols (Keep Alive...)
- Application Layer
  - JSON messages format
  - Master Node dispatch
  - Master Node *"DMX Light Automatic Function Mode"* handler
  - Network maintenance messages
- Smartphone App Frontend
  - User interface in the smartphone
  - Opens Bluetooth connection with Smartphone
  - Handles the Bluetooth connection with Smartphone
- DMX Node Communication
  - Parses the input data
  - Translate it into approriate DMX signal
