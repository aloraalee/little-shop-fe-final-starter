# Little Shop - Coupon Codes | Final Project | Frontend Starter Repo

This Vite Little Shop - Coupon Codes FE Final Project Boilerplate is built to consume and display the data from the BE Rails API built in the Mod 2 Final Project.  


[GitHub BE Link](https://github.com/aloraalee/little-shop-be-final-starter.git) [LinkedIn link](https://www.linkedin.com/in/alora-riley)

### Abstract:
This application is a Merchant-Coupon management system built with a Ruby on Rails backend API and a vanilla JavaScript frontend. The app allows users to view merchants and their associated coupons, solving the problem of efficient coupon management and distribution for multiple merchants.

Key features include:
1. Displaying a list of merchants
2. Viewing coupons for each merchant
3. RESTful API endpoints for merchants and coupons
4. Responsive frontend design for easy user interaction

This application solves the problem of coupon management by providing a centralized platform where users can easily access and view coupons from various merchants. It streamlines the process of coupon discovery and usage, benefiting both merchants and consumers.

### Installation Instructions:
To get this application running on your local machine, follow these steps:

1. Backend Setup:
- Clone the backend repository: git clone [GitHub BE Link](https://github.com/aloraalee/little-shop-be-final-starter.git)
- Navigate to the backend directory: cd `little-shop-be-final-starter`
- Install dependencies: bundle install
- Set up the database: rails db:create db:migrate db:seed
- Start the Rails server: rails server
- Ensure the server is running on localhost:3000

2. Frontend Setup:
- Clone the frontend repository: git clone [GitHub FE Link](https://github.com/aloraalee/little-shop-fe-final-starter/tree/main)
- Navigate to the frontend directory: cd `little-shop-fe-final-starter`
- Install dependencies: npm install 
- Start the frontend development server: npm run dev


### Preview of App:
<img width="811" alt="Screenshot 2024-11-12 at 8 15 45 PM" src="https://github.com/user-attachments/assets/e0ba0adb-f66b-4495-a161-7ea1ca2996fe">

### Context:
I had 6 days to work on this project, with the majority of my time focused on developing the backend functionality. The frontend work was a smaller portion of my overall contribution, but it was crucial for demonstrating the backend capabilities. Here's an overview of my work:

Backend Development (Primary Focus):
1. Implemented model associations:
- Created a Coupon model that belongs to a Merchant
- Updated the Invoice model to optionally belong to a Coupon, ensuring an invoice can have at most one coupon
2. Developed full CRUD functionality for coupons with specific business rules:
- Implemented a limit of 5 activated coupons per merchant
- Created an activation/deactivation system instead of deletion for coupons
- Designed Coupon attributes including name, unique code, and discount value (percent-off or dollar-off)
- Ensured coupon codes are unique across the entire database
3. Adjusted existing tests to accommodate the new optional association between Invoice and Coupon
4. Set up seed data or console commands to add coupons to existing invoices for testing purposes

Frontend Enhancements (Secondary Focus):
1. Iteration 1: Display Coupon Data
- Implemented functionality to fetch and display coupon data for each merchant
- Created a basic layout to show coupon information
2. Iteration 2: Update Display Options
- Added logic to dynamically update the UI based on the current view (Merchants vs Coupons)
- Implemented showing/hiding of relevant UI elements when switching between views

While the frontend work was less extensive, it was crucial in showcasing the backend functionality and improving the overall user experience. The project allowed me to gain comprehensive full-stack development experience, with a deeper dive into backend development practices using Ruby on Rails, including model associations, business logic implementation, and database management. The frontend work enhanced my skills in JavaScript and DOM manipulation, particularly in the context of integrating with a Rails API.

### Learning Goals:
The learning goals for this project were comprehensive, covering both backend and frontend development aspects. They included:
1. Database Management:
  - Writing migrations to create tables and establish relationships between them
  - Implementing CRUD (Create, Read, Update, Delete) functionality for resources, particularly for the Coupon model
2. Architecture and Code Organization:
  - Utilizing the Model-View-Controller (MVC) pattern to organize code effectively
  - Limiting logic in serializers and controllers to maintain clean, maintainable code
3. ActiveRecord and Data Manipulation:
  - Leveraging built-in ActiveRecord methods for complex operations such as joining tables, making calculations, and grouping data based on attributes
4. Testing:
  - Writing comprehensive model tests to ensure data logic integrity
  - Developing request tests to cover the full functionality of the application
5. Frontend Integration:
  - Displaying data for users in a frontend application by manipulating DOM elements
    
The technologies I worked with during this project included:

Backend:
  - Ruby on Rails: Used as the primary framework for building the API
  - ActiveRecord: For database operations and ORM (Object-Relational Mapping)
  - PostgreSQL: As the database management system
  - RSpec: For writing and running tests
   
Frontend:
  - JavaScript: For client-side scripting and DOM manipulation
  - HTML/CSS: For structuring and styling the frontend application
  - Fetch API: For making HTTP requests to the Rails backend

Version Control and Deployment:
  - Git: For version control and collaboration
  - GitHub: For repository hosting and project management

This project provided an excellent opportunity to work across the full stack, deepening my understanding of how backend and frontend technologies interact. It reinforced my skills in Ruby on Rails development, particularly in areas like database design, API development, and testing. On the frontend, it enhanced my ability to work with vanilla JavaScript for DOM manipulation and API integration, providing a solid foundation for future work with more advanced frontend frameworks.

### Wins
1. Successful Implementation of Complex Business Logic:
One of my biggest wins was successfully implementing the intricate business rules for the coupon system. Specifically, I managed to create a system where merchants could have a maximum of 5 activated coupons, and implemented an activation/deactivation feature instead of deletion. This required careful planning and execution, and I'm proud of how I was able to translate these requirements into functional code.
2. Effective Database Design and Management:
Another significant achievement was designing and implementing a database structure that efficiently handled the relationships between Merchants, Coupons, and Invoices. I successfully created migrations that established these relationships and ensured data integrity. This included making the Coupon-Invoice relationship optional without breaking existing functionality, which was a delicate balance to maintain.
3. Comprehensive Test Coverage:
I'm particularly proud of the extensive test suite I developed. Writing thorough model and request tests not only ensured the reliability of my code but also deepened my understanding of test-driven development practices in Rails.

## Challenges:
1. Keeping Controllers Slim:
One of the main challenges I faced was keeping my controllers slim and adhering to the principle of "skinny controllers, fat models". Initially, I found myself putting too much logic in the controllers. To overcome this, I systematically reviewed my controller code and extracted complex logic into the models. This often involved creating new methods in the models and using ActiveRecord callbacks where appropriate. The process improved the overall structure of my code, making it more maintainable and easier to test.
2. Balancing Backend and Frontend Development:
Given the limited time and the focus on backend development, I found it challenging to allocate sufficient time for frontend implementation. To address this, I prioritized the most critical frontend features that would showcase the backend functionality. I created a basic but functional UI that demonstrated the core features, focusing on JavaScript functionality over extensive styling. This approach allowed me to meet the project requirements while still delivering a working full-stack application.

These challenges pushed me to deepen my understanding of Rails, database design, and full-stack development. Overcoming them not only improved the project outcome but also significantly enhanced my problem-solving skills and technical knowledge.
