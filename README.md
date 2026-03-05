# Random Quote Generator (Serverless)

This project is a modern, serverless web application that generates random motivational quotes. The frontend is a single HTML page with embedded CSS and JavaScript, featuring a glassmorphism design, animated pop-ups, celebration particle effects, and dynamic gradient backgrounds.

The backend is implemented using AWS Lambda (Python) and accessed through Amazon API Gateway. Each time a user clicks the “Generate Quote” button, the frontend sends a request to the API Gateway, which triggers the Lambda function to select a random quote and return it to the dashboard.

Services used and configurations:

AWS Lambda: Configured with Python runtime to handle quote generation and API requests.

API Gateway: Configured to expose a REST endpoint for the frontend to call, including CORS headers.

Frontend: Single-page HTML with embedded CSS and JavaScript for styling, animations, and API integration.

This setup demonstrates a small-scale serverless architecture with a functional, visually appealing frontend and a cloud-hosted backend API.


## Features

• Random motivational quote generator  
• Modern glass-style UI dashboard  
• Animated popup quote display  
• Celebration particle animation  
• Dynamic gradient background changes  
• Serverless cloud backend


## Tech Stack

Frontend
- HTML
- CSS
- JavaScript

Backend
- AWS Lambda (Python)

API Layer
- Amazon API Gateway

Cloud Platform
- Amazon Web Services


## System Architecture

User Browser  
↓  
Frontend Dashboard (HTML)  
↓  
API Gateway  
↓  
AWS Lambda Function  
↓  
Random Quote Response

![image alt](image-url)

## Author
Arjun Nalge - DevOps Engineer
