# DLS DOCUMENTATION


## User Stories

### Customer Create Account
**As a** customer,  
**I want** to create a customer account,  
**so that** I can login.

#### Acceptance Criteria:
- **Username**  
  - Must be unique.  
  - Allowed characters: letters, numbers.  
  - Minimum length: 3 characters.  
  - Maximum length: 12 characters.  

- **Password**  
  - Must include:
    - 1 or more uppercase letters.
    - 1 or more lowercase letters.
    - 1 or more numbers.
    - 1 or more symbols.  
  - Minimum length: 8 characters.  
  - Maximum length: 64 characters.  

- **Email**  
  - Must be a valid email address.  
  - Must include a prefix, domain, and a `@`.  
  - **Prefix**:
    - Allowed characters: letters (a-z), numbers, underscores, periods, and dashes.
    - Underscore, period, or dash must be followed by one or more letters or numbers.  
  - **Domain**:
    - Allowed characters: letters, numbers, dashes.  
    - Last portion of the domain must have at least two characters (e.g., `.com`, `.org`).  

- **Phone Number**  
  - Must be in the Danish format:  
    - With `+45`: `+45 11 11 11 11`.  
    - Without `+45`: `11 11 11 11`.  

- **Address**  
  - Must be a Danish address:
    - Format: `Street name street number, postal code (4 numbers) city name`.  
    - Example: `Byhaven 1, 2750 Ballerup`.  

---

### Delivery Agent Create Account
**As a** delivery agent,  
**I want** to create a delivery agent account,  
**so that** I can login to the MTOGO app.

---

### Restaurant Create Account
**As a** restaurant,  
**I want** to create a restaurant account,  
**so that** I can login to the MTOGO app.

---

### Admin Create Account
**As an** admin,  
**I want** to create an admin account,  
**so that** I can login to the MTOGO app and see the management dashboard.

---

### Customer Search for Restaurant
**As a** customer,  
**I want** to be able to search for a restaurant,  
**so that** I can see restaurants listed.

#### Acceptance Criteria:
- Results should match the search term (exact or approximate).  
- Results should only include restaurants within a 0–5 km radius.  
- Search results should use pagination (up to 20 restaurants per page).  
- Results should display:
  - Restaurant name.  
  - Address/postal code.  
  - Distance in kilometers.  
- Support keyword/tag searches (e.g., "Pizza", "Burger").  

---

### Customer Selects Restaurant
**As a** customer,  
**I want** to select a restaurant,  
**so that** I can see the given restaurant’s menu.

#### Acceptance Criteria:
- Restaurant name should appear at the top.  
- Menu should be displayed below the restaurant's name.

---

### Customer Selects Food
**As a** customer,  
**I want** to select food items,  
**so that** I can add them to a cart.

#### Acceptance Criteria:
- Food items should have prices displayed.

---

### Customer Orders Food
**As a** customer,  
**I want** to order the items in my cart,  
**so that** the restaurant can prepare my food.

#### Acceptance Criteria:
- Show the accumulated price of the order.  
- Allow customers to annul their order before paying.

---

### Restaurant Accepts Incoming Order
**As a** restaurant,  
**I want** to accept an incoming order,  
**so that** we can sell some food.

#### Acceptance Criteria:
- Display incoming orders clearly.  
- Allow restaurants to accept orders via the display.

---

### Restaurant Rejects Incoming Order
**As a** restaurant,  
**I want** to reject an incoming order,  
**so that** we don't get too many orders at once.

---

### Customer Pays for Food
**As a** customer,  
**I want** to pay for my food,  
**so that** I will receive my order.

#### Acceptance Criteria:
- Allow customers to choose a payment method.  
- Redirect customers to a secure external payment page.  
- Send order confirmation email with details.

---

### Delivery Agent Information
**As a** delivery agent,  
**I want** to see available orders,  
**so that** I can pick them up.

#### Acceptance Criteria:
- Display all available orders.  
- Allow delivery agents to accept orders via the display.

---

### Delivery Agent Picks Up Order
**As a** delivery agent,  
**I want** to pick up an order from a restaurant,  
**so that** I can deliver it to the customer.

#### Acceptance Criteria:
- Delivery agents should confirm the pickup via the display to notify the customer.

---

### Customer Receives Order Process Updates
**As a** customer,  
**I want** to receive order process updates,  
**so that** I can track the status of my order.

#### Acceptance Criteria:
- Display live updates of the order status.

---

### Customer Creates Review
**As a** customer,  
**I want** to create a review,  
**so that** I can rate my experience.

#### Acceptance Criteria:
- Allow reviews through the app.  
- Reviews include:
  - Star rating (0–5).  
  - Comment (0–280 characters).  
- Two types of reviews:
  - Agent review when the order is received.  
  - Restaurant review (including food) when the order is received.  

---

### Customer Login
**As a** customer,  
**I want** to login to my account,  
**so that** I can use the MTOGO app.

#### Acceptance Criteria:
- Handle incorrect username/password alerts.  
- Issue an authentication token upon successful login.

---

### Customer See Ratings of Restaurants
**As a** customer,  
**I want** to see restaurant ratings,  
**so that** I can select the best restaurant for me.

#### Acceptance Criteria:
- Display restaurant ratings below their names.

---

### Customer Cart
**As a** customer,  
**I want** to see my cart,  
**so that** I can view or edit it.

#### Acceptance Criteria:
- Cart and price should update when food is added.  
- Show combined price.  
- Allow viewing and editing of the cart.  
- Combine identical food items into one entry.
