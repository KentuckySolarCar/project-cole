# Project C.O.L.E. 
(**C**AN **O**ver **L**T**E**)

This project is a complete re-imagining of both the solar car dashboard as well as the telemetry collection system. It aims to fuse them together in a highly efficient effective manner, allowing for centralized data collection and dashboard data distribution.

## Components
- [can_proxy](https://github.com/KentuckySolarCar/can_proxy): This is the CAN data collection component underpinning the whole system. Its job is to read the CAN data lightning quick, package it up in to a neat JSON packet, and then send it off via an incoming message queue so that the dashboard webserver  can read it, as well as to a database to store it for later collection. This is written in C++ and uses a mix of modern C++ and C for interacting with the Linux kernel via SocketCAN.
- [dashboard_webserver](https://github.com/KentuckySolarCar/dashboard_webserver): Webserver component of the project, for pushing data to the dashboard
- [flutter_dashboard](https://github.com/KentuckySolarCar/flutter_dashboard): Dashboard component of the project, built in Flutter
