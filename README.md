# Carpooling App for Temporary Workers

## Introduction

This project was completed during my career transition into the IT field. We collaborated with a school partner, the temporary work agency **Actual**, to develop a carpooling service for temporary workers. This application was presented as an end-of-year project by a team of two.

Since the development was carried out for **Actual**, the codebase cannot be disclosed. However, this project is presented to populate my portfolio and demonstrate my skills.

## Architecture

| Component | Technology |
|-----------|------------|
| Backend | PHP, Laravel |
| Frontend | JavaScript, React, Expo |
| Database | MySQL |

Our project is designed as a service within the existing **"MyActual"** application, which provides temporary workers with a simple tool to manage their profiles and consult missions.

## Tools Used

- **Postman**: For E2E testing
- **OSRM**: For geolocation services
- **VSCode**: As the Integrated Development Environment (IDE)



## Live Demo

A video demonstrating the application's functionality is available. Further details are provided in the [Functionality](#functionality) section.
[![Live Demo](demo_full.mp4)](demo_full.mp4)


## Functionality

### Overview

1. **Data Retrieval**: User information such as name, home address, and mission address is retrieved from the main application.
2. **User Roles**: Users can choose to be either a driver or a passenger.
3. **Search and Pre-Match**: Passengers can search for trips. A pre-match is conducted via MySQL to find the 50 closest people to the user's home and mission address.
4. **Distance Calculation**: On-premise calculations using OSRM determine the actual distance and walking time to the meeting point.
5. **Communication**: Users can call each other to finalize details. This MVP does not include a messaging system.
6. **Request System**: Passengers can send carpooling requests, which must be accepted by the driver.

### Technical Details

#### Backend (PHP/Laravel)
- **API RESTful** Without authentification. This part was out of scope and managed by Actual.
- **Geospatial queries** using MySQL spatial functions for efficient proximity searches.
- **OSRM on premise integration** for real-time distance and route calculations. 
- **Database design** optimized for carpooling relationships and trip management.

#### Frontend (React Native/Expo)
- **Cross-platform mobile app** supporting Android (need to be tested on iOS)
- **State management**  with Zustand
- **Expo Go** for rapid testing 

#### DevOps & Infrastructure
- **Docker containerization** for consistent development environments
- **Multi-service architecture** with backend, database, and OSRM services


## Timeline

| Period | Activity |
|--------|----------|
| January - May | Framing the MVP, determining needs, creating user stories, MoSCoW classification, user flow, and mock-ups |
| June | Development focus on backend and distance calculations |
| July | Frontend development using Copilot for AI-assisted coding |
| Mid-July | Presentation to the Actual team and end-of-year project submission at Holberton, achieving a final grade of **99.45%** !!|

## Retrospective

### Learnings

- Gained experience with **PHP/Laravel**
- Enhanced understanding of software architecture
- Improved organizational skills with **Poker Planning**
- Developed client relations and solution proposal skills
- Learned to create user stories and apply MoSCoW prioritization
- Acquired mock-up creation skills

### Transferable Skills Demonstrated

- **Full-stack development** from database design to mobile UI
- **API design and documentation** following REST principles
- **Agile methodology** implementation with user stories and sprint planning
- **Client communication** and requirement gathering
- **Problem-solving** with geospatial and performance constraints

### Successes

- Efficient project setup
- Successful backend creation with Laravel
- Effective application streaming via Expo-Go
- Comprehensive E2E testing with Postman
- Organized project tracking using GitHub Projects

### Challenges

- Insufficient unit and integration testing
- Over-reliance on AI for frontend development, leading to a "black box" scenario


### Areas for Improvement

- Early implementation of CI/CD
- Integration of unit and integration tests from the start
- Early preparation and use of poker planning for better time estimation
- Judicious use of AI with thorough review and understanding of generated code
- Skill enhancement in JavaScript

