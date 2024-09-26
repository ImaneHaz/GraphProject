---
title: Concept
has_children: false
nav_order: 2
---

# Concept

Graph Project

The project focuses on developing an intelligent tutor recommendation system integrated with a graph plotting tool to enhance personalized learning experiences. The aim of the system is to provide tutor recommendations based on individual preferences and allow students to graphically visualize mathematical concepts or equations for a more interactive learning process.

The relationship between the two functionalities lies in supporting a comprehensive learning approach: students can find a tutor while also being able to explore mathematical concepts within the same environment through graphical visualizations. The system thus integrates both practical and theoretical learning, helping users choose the ideal tutor while assisting in the visual understanding of difficult concepts.

The application will consist of:
•	Backend, which will provide access to various functionalities, such as tutor recommendations and graph plotting, and handle data persistence.
•	Frontend, available as a web application 


# Use case 1: Tutor Recommendations

Actors: User, Tutor
Description: The user can input their age and filter preferences (mode of tutoring and location) to receive personalized tutor recommendations. Currently, the user is only able to view the list of available tutors that match their preferences. Interaction with tutors (e.g., messaging or scheduling) is not yet developed but is planned as a future enhancement of the system.

Main Flow:
Main Flow:
1.	The user opens the recommendation system.
2.	Specify their age and preferences (remote or in-person tutoring mode, location).
3.	The system retrieves a list of tutors matching the specified criteria.

# Use case 2: Graph Plotting

Actors: User
Description: The user can input equations and specify the X and Y axis values to generate and visualize graphs. This tool currently exists independently of the tutor recommendation system and serves as a standalone feature for visualizing mathematical equations or concepts. 

Main Flow:
1.	The user opens the graph plotting tool.
2.	Inputs an equation (e.g., y = x^2).
3.	Specifies the X and Y axis range for the graph.
4.	The system generates and displays the graph.

Connection Between Use Cases
At present, the two functionalities of the system — tutor recommendations and graph plotting — exist independently. Users can view potential tutors based on their preferences and use the graph plotting tool for personal exploration of mathematical concepts. 

