# Smart India Hackathon Workshop
# Date:15-05-2024
## Register Number:212223040113
## Name:MOHAMMED PARVEZ S
## Problem Title
E-Waste Facility Locator
## Problem Description
Website that tells you the location of the nearest e-waste collection and recycling facility. Offers educational pop-ups on the harmful components of your e-waste and their effects on the environment and human health if not disposed correctly. There could be an option to input the model of your old device and earn credit points relative to the amount of precious metals recovered from the device if disposed correctly.
## Problem Creater's Organization
Ministry of Environment

## Idea

![alt text](<IMG 1 IDEA.jpg>)

Locator Map:

Interactive map with GPS integration to locate the nearest e-waste facilities.
Filtering options to find specific types of facilities (e.g., recycling centers, donation points, hazardous waste sites).
Search Functionality:

Search by location (city, ZIP code) or facility type.
Advanced search filters for specific electronic items (e.g., batteries, computers, mobile phones).
Facility Information:

Detailed information about each facility, including address, contact details, operating hours, and accepted e-waste items.
User reviews and ratings for each facility.
Educational Resources:

Articles and tips on the importance of proper e-waste disposal.
Guidelines on how to prepare e-waste for recycling.
Information on the environmental impact of e-waste.
User Account and Tracking:

User accounts for personalized experience.
Track e-waste disposal history and contributions to recycling efforts.
Earn rewards or badges for responsible e-waste disposal.
Notifications and Reminders:

Set reminders for e-waste disposal dates and facility events.
Notifications for nearby e-waste collection drives or events.
Partnerships and Community Involvement:

Collaborations with local governments, NGOs, and businesses to promote e-waste recycling.
Community challenges and events to encourage collective action.
Sustainability Tips:

Suggestions for reducing electronic waste, such as repair and reuse options.
Recommendations for purchasing sustainable electronic products.

## Proposed Solution / Architecture Diagram

![alt text](<IMG 2.png>)


Mobile App (Frontend UI):

Platform: iOS and Android
Functions:
User interface for searching and locating e-waste facilities.
Interactive map with GPS integration.
User account management and tracking.
Educational content and tips.
Backend Server:

API Gateway & Logic:
Handles all incoming requests from the mobile app.
Routes requests to appropriate services (User API, Facility API, etc.).
Contains business logic for processing data and ensuring security.
User Auth Service:

Manages user authentication and authorization.
Handles user data securely, including account details and preferences.
E-Waste Facility Locator Service:

Provides location-based search results for e-waste facilities.
Maintains an updated database of facility information (address, hours, accepted items).
Third-Party APIs:

Maps API: Provides mapping and location data.
Weather API: Optionally, to inform users about weather conditions during facility visits.
Push Notification Service:

Manages notifications and reminders for users.
Sends alerts about upcoming e-waste collection events or facility updates.
Database:

Stores all data related to users, facilities, and educational content.
Includes user activity logs, facility details, and other essential data.
APIs:

User API: Handles user-specific operations like login, registration, and profile management.
Facility API: Manages data related to e-waste facilities.
Notification API: Manages the sending and scheduling of notifications.
Database API: Interfaces with the database for all read/write operations.

## Use Cases

![alt text](<IMG 3.jpg>)


1. User Registration and Authentication
Actor: Individual User

Description: A new user registers for an account and logs into the app.

Steps:

User opens the app and selects the option to register.
User enters necessary information (name, email, password) and submits the form.
The system sends a confirmation email.
User verifies the email address through a link provided.
User logs in with the registered credentials.
Preconditions: User has an email account.

Postconditions: User is registered and logged in.

2. Locate Nearest E-Waste Facility
Actor: Individual User

Description: A user wants to find the nearest e-waste facility to recycle their electronic items.

Steps:

User logs into the app.
User navigates to the "Locate Facility" section.
User allows the app to access their current location or enters a location manually.
The app displays a map with nearby e-waste facilities.
User selects a facility to view details such as address, operating hours, and accepted items.
Preconditions: User is logged in, and location services are enabled.

Postconditions: User finds and gets directions to a nearby e-waste facility.

3. Search for Specific E-Waste Disposal
Actor: Individual User

Description: A user searches for a facility that accepts a specific type of electronic item (e.g., batteries, computers).

Steps:

User logs into the app.
User navigates to the "Search" section.
User enters the type of item they want to dispose of.
The app filters and displays facilities that accept the specified item.
User selects a facility to view details and instructions for disposal.
Preconditions: User is logged in.

Postconditions: User finds a facility that accepts their specific e-waste item.

4. View Educational Content
Actor: Individual User

Description: A user wants to learn more about e-waste disposal and its environmental impact.

Steps:

User logs into the app.
User navigates to the "Learn" section.
User selects an article or resource on e-waste.
The app displays the selected content, including tips and guidelines for proper disposal.
Preconditions: User is logged in.

Postconditions: User gains knowledge about e-waste and its proper disposal.

5. Schedule E-Waste Collection
Actor: Business User

Description: A business user schedules a bulk e-waste collection from their premises.

Steps:

Business user logs into the app.
User navigates to the "Schedule Collection" section.
User enters details about the e-waste items and preferred collection date and time.
The app confirms the availability of the service and schedules the collection.
User receives a confirmation notification with the collection details.
Preconditions: User is logged in as a business account.

Postconditions: E-waste collection is scheduled, and the user receives a confirmation.

6. Track E-Waste Disposal History
Actor: Individual User

Description: A user wants to view their history of e-waste disposal activities.

Steps:

User logs into the app.
User navigates to the "History" section.
The app displays a list of all previous disposals, including dates, items, and locations.
User can view detailed records for each disposal activity.
Preconditions: User is logged in.

Postconditions: User views their e-waste disposal history.



## Technology Stack

![alt text](<IMG 4.png>)

Frameworks:

React Native: For cross-platform mobile app development (iOS and Android).
Pros: Single codebase for both platforms, large community, reusable components.
Alternatives: Flutter, if more native performance and rich UI customization are needed.
UI Libraries:

React Native Elements: For pre-styled, customizable UI components.
React Navigation: For handling navigation and routing within the app.
State Management:

Redux: For managing the app’s state.
Context API: For simpler state management in less complex parts of the app.
Location Services:

React Native Maps: For integrating maps and displaying facility locations.
Geolocation API: For accessing the device’s location.
Backend
Framework:

Node.js with Express: For building the backend server and APIs.
Pros: Non-blocking I/O operations, large ecosystem, fast development.
Alternatives: Django (Python), if a more structured and battery-included framework is preferred.
Database:

MongoDB: For storing facility information, user data, and other resources.
Pros: Flexible schema design, scalability, and ease of integration with Node.js.
Alternatives: PostgreSQL, if relational data and ACID compliance are prioritized.
Authentication:

Auth0 or Firebase Authentication: For managing user authentication and authorization.
Pros: Secure, scalable, and integrates well with mobile apps.
APIs:

RESTful APIs: For communication between the mobile app and the backend.
GraphQL: Optionally, for more efficient data retrieval and flexible queries.
Third-Party Services
Maps:

Google Maps API: For providing map functionalities and geocoding services.
Mapbox: As an alternative for more customizable map experiences.
Notifications:

Firebase Cloud Messaging (FCM): For sending push notifications to the mobile app.
OneSignal: As an alternative for robust notification management.
Payment Gateways (if required for donations or premium features):

Stripe or PayPal: For handling payments securely.
Weather API:

OpenWeatherMap API: For providing weather information relevant to facility visits.
DevOps and Deployment
Version Control:

Git: For version control and collaboration.
GitHub or GitLab: For repository hosting and CI/CD integration.
Continuous Integration and Continuous Deployment (CI/CD):

GitHub Actions or GitLab CI/CD: For automated testing, building, and deployment.
Jenkins: As an alternative for more customizable CI/CD pipelines.
Hosting and Infrastructure:

Heroku or Vercel: For hosting the backend server and API.
AWS (Amazon Web Services) or Google Cloud Platform (GCP): For scalable infrastructure and additional services like databases, storage, and serverless functions.
Containerization:

Docker: For containerizing the backend application to ensure consistent environments across development, testing, and production.
Monitoring and Analytics:

Google Analytics or Firebase Analytics: For tracking user interactions and app performance.
New Relic or Datadog: For monitoring backend performance and infrastructure health.


## Dependencies

Mapping Services – 20 Days,Data Collection – 25 Days,Estimated Budget – Rs.25,0000