# DLS DOCUMENTATION

---
## User Stories

### Customer Create Account
As a customer, I want to create a customer account, so that I can login.

#### Acceptance Criteria:
- The username must be unique  
  - Allowed characters: letters, numbers  
  - Must have a minimum length of 3 characters, maximum 12  

- The password should follow these specific password rules:  
  - Has to include 1 or more uppercase, 1 or more lowercase, 1 or more number, and 1 or more symbol.  
  - Must have a minimum length of 8 characters, maximum 64.  

- The e-mail has to be a valid email address  
  - Has to include a prefix, domain, and a `@`  
  - **Prefix (Before `@`)**  
    - Allowed characters: letters (a-z), numbers, underscores, periods, and dashes.  
    - An underscore, period, or dash must be followed by one or more letters or numbers.  
  - **Domain (After `@`)**  
    - Allowed characters: letters, numbers, dashes.  
    - The last portion of the domain must be at least two characters, for example: `.com`, `.org`, `.cc`, `.dk`  
      - (Valid domains: [https://www.iana.org/domains/root/db](https://www.iana.org/domains/root/db))  

- The phone number must be the Danish format:  
  - `+45` followed by 8 numbers (e.g.: `+45 11 11 11 11`), or without the `+45` (e.g.: `11 11 11 11`).  

- The address must be a Danish address:  
  - Street name street number, postal code (4 numbers), city name (e.g.: `Byhaven 1, 2750 Ballerup`).  

---

### Delivery Agent Create Account
As a delivery agent, I want to create a delivery agent account, so that I can login to the MTOGO app.

---

### Restaurant Create Account
As a restaurant, I want to create a restaurant account, so that I can login to the MTOGO app.

---

### Admin Create Account
As an admin, I want to create an admin account, so that I can login to the MTOGO app and see the management dashboard.

---

### Customer Search for Restaurant
As a customer, I want to be able to search for a restaurant, so that I can see restaurants listed.

#### Acceptance Criteria:
- The search result should return results that are identical or almost identical to the search  
- The search result should only show restaurants within 0 - 5 km radius of the customer  
- The search should use pagination and each page should return up to 20 restaurants  
- The list should show the restaurant's name and the address/postal code, how far away in km  
- Should the customer be able to search for keywords/tags, such as “Pizza”, “Burger” etc.?  

---

### Customer Selects Restaurant
As a customer, I want to be able to select a restaurant, so that I can see the given restaurant’s menu.

#### Acceptance Criteria:
- The restaurant's name should be displayed at the top  
- Selecting a restaurant should showcase the restaurant’s menu below its name  

---

### Customer Selects Food
As a customer, I want to be able to select the food items I want, so that I can add them to a cart.

#### Acceptance Criteria:
- The food items should have the price next to them  

---

### Customer Orders Food
As a customer, I want to be able to order the items in my cart, so that the restaurant can prepare my food.

#### Acceptance Criteria:
- The customer should be able to see the accumulated price of their order  
- The customer should be able to annul their order, before paying  

---

### Restaurant Accept Incoming Order
As a restaurant, I want to be able to accept an incoming order, so that we can sell some food.

#### Acceptance Criteria:
- The restaurant should have a clear display over orders coming in  
- The restaurant should be able to accept an order via the display  

---

### Restaurant Rejects Incoming Order
As a restaurant, I want to be able to reject an incoming order, so that we don't get too many orders at once.

---

### Customer Pays for Food
As a customer, I want to be able to pay for my food, so that I will receive my order.

#### Acceptance Criteria:
- The customer should be able to choose a way of payment  
- The customer should be redirected to a secure payment page of their choice (externally)  
- The customer should receive an order confirmation on their email with the order details  

---

### Delivery Agent Information
As a delivery agent, I want to see available orders, so that I can pick it up.

#### Acceptance Criteria:
- The delivery agent should be able to see all orders available in a display  
- The delivery agent should be able to accept an order via the display  

---

### Delivery Agent Picks Up Order
As a delivery agent, I want to pick up an order from a restaurant, so that I can deliver it to the customer.

#### Acceptance Criteria:
- The delivery agent should be able to confirm the order has been picked up on the display to notify the customer  

---

### Customer Receives Order Process Updates
As a customer, I want to receive order process updates, so that I can track the status of my order.

#### Acceptance Criteria:
- The customer should be able to see their order status at all times  
- The customer's order status should update live (every time there is a change?)  

---

### Customer Create Review
As a customer, I want to create a review, so that I can rate my experience.

#### Acceptance Criteria:
- The customer should be able to create a review via the app.  
- A review of the agent and restaurant is a star-rating from 0-5 and a comment of 0-280 characters.  
- There are 2 different reviews:  
  - The customer should be able to review the agent when the order is received.  
  - The customer should be able to review the restaurant and their food when the order is received.  

---

### Customer Login
As a customer, I want to be able to login to my account, so that I can use the MTOGO app.

#### Acceptance Criteria:
- When logging in, it should handle if the password and/or username is wrong. If one of them is wrong, the user is alerted.  
- When the customer is successfully logged in, they should have an authentication token  

---

### Customer See Rating of Restaurants
As a customer, I want to be able to see the restaurant's ratings, so that I can select the best restaurant for me.

#### Acceptance Criteria:
- The customer can see the restaurant's ratings below the restaurant's name  

---

### Customer Cart
As a customer, I want to be able to see my cart, so that I can view or edit my cart.

#### Acceptance Criteria:
- The cart and price should have been updated when a customer adds food, and the combined price should be shown to the customer  
- The customer should be able to view and edit their cart  
- Identical food items should be shown with a combined amount  

---

## Deployment

Run this to setup Docker Swarm:

```docker swarm init```

Run this to set up the Swarm using Docker Stack:

```docker stack deploy -c docker-stack.yml mtogo```

Run this to see the services:

```docker stack services mtogo```

Or this to remove:

```docker stack rm mtogo```