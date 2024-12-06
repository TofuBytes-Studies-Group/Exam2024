# Software Development Exams 2024

This repository is the central hub for all microservices, models, and documentation related to the MTOGO system for our Software Development Exams 2024. 


## Group F

| Name                      | GitHub Profile                              |
|---------------------------|---------------------------------------------|
| Jamie Grønbæk Callan      | [@thejamiegc](https://github.com/thejamiegc)      |
| Markus Isak Møgelvang     | [@solskinIsak](https://github.com/solskinIsak)  |
| Helena Botn Lykstoft      | [@HelenaLykstoft](https://github.com/HelenaLykstoft) |
| Caroline Lærke Høg Rendtorff | [@CarolineHoeg](https://github.com/CarolineHoeg)   |

---


## Table of Contents

1. [Overview](#overview)
2. [System Architecture](#system-architecture)
   - [Monolith](#monolith)
   - [Microservices](#microservices)
     - [Service Directory](#service-directory)
3. [GitHub Projects](#github-projects)
4. [Documentation](#documentation)
   - [System Integration](#system-integration)
   - [Development of Large Systems](#development-of-large-systems)
   - [Software Quality](#software-quality)
5. [Models](#models)

---

## Overview

MTOGO is a food delivery service, where customers can order food, which is then made by local restaurants and delivered to the customer. The customers can then choose to leave feedback on their experience. 

The MTOGO case describes the functional and non-functional requirements for the solution. 
The aim of this project was to design and develop a modern integrated software system based on the MTOGO case. 

The current version of our product is a software system, which focuses primarily on creating value for the customer of MTOGO. Therefore, we chose to prioritize what we have called the *golden path* for our system, which is how the customer interacts with it. This includes registration, login, ordering, receiving order status updates, and creating reviews. 



## System Architecture
![MTOGO_eksamensprojekt-architecture_diagram](https://github.com/user-attachments/assets/c377e1a0-b371-4506-a2d5-7fc0e8fcd82b)


## Monolith
This is the directory for [Accounts](https://github.com/TofuBytes-Studies-Group/Accounts), which represents our legacy system, built as a monolith using hexagonal architecture. It handles customer account registration, login, and authentication. 

## Microservices

We have create a template for our microservices, so they could be made with domain-driven design in mind. The repository is [this](https://github.com/TofuBytes-Studies-Group/MTOGO_template).

### Service Directory

Below is the directory of microservices in the MTOGO system:

| Service Name   | Description                                                                      | Repository Link                                                         |
|----------------|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Catalog        | Manages restaurants and their menus                                             | [Catalog Repo](https://github.com/TofuBytes-Studies-Group/Catalog)      |
| Cart           | Manages a customer's cart and calculates subtotal and total price of dishes     | [Cart Repo](https://github.com/TofuBytes-Studies-Group/Cart)            |
| Ordering       | Transforms cart data into an order and sends it to the Payment system           | [Ordering Repo](https://github.com/TofuBytes-Studies-Group/Ordering)    |
| Order Status   | Listens to Kafka for order status updates that can be accessed via an endpoint             | [Order Status Repo](https://github.com/TofuBytes-Studies-Group/Order_status) |
| Review         | Manages customer reviews of restaurants and delivery agents                    | [Review Repo](https://github.com/TofuBytes-Studies-Group/Review)        |
| Dashboard  | The management's dashboard for checking open orders, still in progress | [Dashboard Repo](https://github.com/TofuBytes-Studies-Group/MTOGODashboard) |



## Github Projects

To stay organized and to track our progress we used Github Projects. Our board can be found [here](https://github.com/orgs/TofuBytes-Studies-Group/projects/1). 



## Documentation

### System Integration

For System Integration exam, see [this folder](https://github.com/TofuBytes-Studies-Group/Exam2024/tree/main/Documentation/System%20Integration).

### Development of Large Systems

For Development of Large Systems exam, see [this folder](https://github.com/TofuBytes-Studies-Group/Exam2024/tree/main/Documentation/Development%20of%20Large%20Systems).

### Software Quality

For Development of Software Quality exam, see [this folder](https://github.com/TofuBytes-Studies-Group/Exam2024/tree/main/Documentation/System%20Quality).

### Models

All diagrams and models can be found in [this folder](https://github.com/TofuBytes-Studies-Group/Exam2024/tree/main/Documentation/Models).

---
