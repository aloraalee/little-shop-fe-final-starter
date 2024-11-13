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
(Provide ONE gif or screenshot of your application - choose the "coolest" piece of functionality to show off. gifs preferred!)

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
(What were the learning goals of this project? What tech did you work with?)

### Wins + Challenges:
(What are 2-3 wins you have from this project? What were some challenges you faced - and how did you get over them?)
