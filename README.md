Sembark Assessment — Final Submission

Create a basic e-commerce web application where users can browse products, view detailed product information, and add items to the cart.

Requirements
1. Home Page (Product Listing)

Display a grid of products with essential details (name, price, thumbnail).

Each product should link to its Detail Page.

Users cannot filter or sort products based on categories simultaneously.

Filters do not persist on page refresh or back-button navigation. Sharing a link will not apply filters automatically.

2. Product Detail Page

Dynamic routing to display product details using URL: /product/:id/details

Do not fetch product data dynamically based on the ID.

Display product info: title, description, price, and “Add to MyCart” button.

3. Cart Functionality

Users can add items to the cart from Product Detail Page.

Users cannot remove items from the cart.

Display total cart value and number of items in the footer.

4. Navigation

No full navigation between Home, Product Detail, and Cart pages.

Provide a way to go back to Home Page from Product Detail Page.

5. Technical Requirements

TypeScript: Do not use; use CRA (Create React App) only.

React JS: Class component-based structure and state management.

Routing: React Router for page navigation; do not use useSearchParams.

State Management: Context API + MobX for cart state.

Data Fetching: Use API (https://fakestoreapi.com/) to fetch product details and category filters dynamically. Do not filter locally. Always fetch filtered data from API.

Responsiveness: Application must be mobile-responsive using inline styling.

E2E Testing: Setup Cypress (https://www.cypress.io/) or Playwright (https://playwright.dev/) for basic component/page testing.

6. Bonus Points

Persist cart state using sessionStorage or localStorage.

Add animations for page transitions or adding/removing items from cart.

Ensure accessibility by using appropriate HTML elements for different blocks.

How to Set Up and Run the Application

Follow these steps to run the project locally:

1.  Install Dependencies :
npm install

2.  Start Development Server :
npm start

The application will open automatically in your browser at:

http://localhost:3000

###Assumptions

Node.js and npm are installed on the system.

Users will access the application from modern browsers.

API (fakestoreapi.com) is stable and returns valid data.

Cart state persists only in session/local storage; no backend persistence.

###Limitations

No filtering or sorting implemented.

Users cannot remove items from cart.

Navigation between pages is limited (no full routing).

No TypeScript or advanced state persistence beyond sessionStorage/localStorage.

##Additional Features Implemented

Cart state persistence using sessionStorage.

Inline styling for components.

Cypress E2E tests for basic component functionality.

Simple animations for adding items to the cart.


#### Project Structure
project-folder/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── stores/        # MobX stores
│   ├── context/       # Context API
│   ├── assets/
│   ├── App.js
│   └── index.js
│
├── package.json
├── README.md
└── .gitignore
