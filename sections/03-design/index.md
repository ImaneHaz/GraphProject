---
title: Design
has_children: false
nav_order: 4
---

# Design

This chapter explains the strategies used to meet the requirements identified in the analysis.

## Architecture

At a high level, GraphProject consists of three fundamental components:

-The backend, which provides a REST API using Node.js and Express for core functionalities like tutor recommendations and graph plotting.
-The frontend web application, which interfaces with the backend through the REST API to allow users to input preferences for tutor recommendations and graph plotting.
-The client-side in-memory data storage, which temporarily stores user preferences, tutor information, and graph data using JavaScript arrays.

The chosen architecture follows a layered approach:

- Presentation layer: Handles user interactions and displays tutor recommendations and graphs.
- Business layer: Implements the core application logic, including matching user preferences with tutor data and managing graph plotting requests.
- Persistence layer:  Interfaces with in-memory data structures (JavaScript arrays) for storing and retrieving tutor data, user preferences, and graph configurations.
- Database layer: Manages temporary data storage in JavaScript arrays for quick access during a user session, but this data is not persisted across server restarts.
  
## Modelling

- The system’s domain is modeled around key entities such as User, Tutor, Graph, and Recommendation.
- The domain model is structured to handle user preferences, tutor data, and graph generation seamlessly.
- Class diagrams will highlight the relationships between these core entities and showcase how these designs address the requirements.
    - For instance, how Tutor objects are filtered and matched based on user criteria (e.g., age, location, preferred mode of tutoring).
    - Tactical patterns and Domain-Driven Design (DDD) principles are applied to model complex behaviors like tutor recommendation and graph plotting.
      
## Interaction

- The behavior of the system will be illustrated using sequence and activity diagrams.
    - Sequence diagram: For example, a sequence diagram can show how the system processes a tutor recommendation request, from user input to filtering matching tutors from the in-memory data arrays and delivering them to the frontend.
    - Graph Plotting Flow: Another sequence diagram could illustrate the graph plotting process, from user equation input to graph rendering based on the defined X and Y ranges.
## Behaviour

- This section will explain the possible states of the system, using UML state diagrams to show:
    - States like User Input Received, Recommendation Generated, and Graph Rendered.
    - Transitions between these states are triggered by user actions, such as inputting preferences, requesting tutor recommendations, or submitting equations for graph plotting.
      
## Data-related aspects

- Data schema: The data is stored in in-memory JavaScript arrays for the current version of the project. These arrays store entities like Users, Tutors, Recommendations, and Graph Configurations.
    - User Array: Stores user details, including their preferences for tutor recommendations and past graphing activities.
    -Tutor Array: Contains tutor-specific details such as subject expertise, location, and availability.
    - Recommendation Array: Logs the results of tutor searches based on user preferences.
    - Graph Configuration Array: Stores user-defined equations and graph settings for quick retrieval and rendering.
- Data Persistence Technologies: Currently, the project uses in-memory storage via JavaScript arrays to temporarily hold data during the session. This allows fast access, but the data is lost when the session ends. In future iterations, a more robust solution (like a NoSQL or SQL database) could be implemented for persistent storage.
- Backup and Recovery: As there is no permanent storage in the current version, backup and recovery processes are not required at this stage. However, in future developments, a persistent database solution would include regular backups to ensure data integrity and enable quick recovery in case of system failure.
