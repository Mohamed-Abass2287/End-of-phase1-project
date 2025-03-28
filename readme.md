deployed link:https:(//mohamed-abass2287.github.io/End-of-phase1-project/)

# End-of-phase1-project
deployed link live at https://mohamed-abass2287.github.io/End-of-phase1-project/


Budget Tracker
Track your wallet today, live without regrets tomorrow!
Budget Tracker is a web application designed to help individuals manage their finances effectively. Whether you want to track income, monitor expenses, or gain insights into your spending habits, this app is your ultimate tool for financial management.

<!-- Project Structure -->
End-of-phase1-project/
├── index.html          # Main HTML file
├── css/
│   └── style.css       # Stylesheet for the app
├── js/
│   └── app.js          # JavaScript code
├── db.json             # Mock database
└── README.md           # Project documentation


<!-- Setup Instructions -->
Clone the Repository:

bash
git clone https://github.com/Mohamed-Abass2287/End-of-phase1-project.git
Navigate into the project directory:

bash
cd End-of-phase1-project

<!-- browsing test -->
Open the Application: Open the index.html file in your preferred browser to test the functionalities.

<!-- Update the API endpoint in js/index.js with: -->
javascript
const fetchTransactions = () => {
  fetch('http://localhost:3000/transactions')
};

<!-- Fetch Transactions -->
Fetch all transactions dynamically when the page loads. Ensure that your API or backend server provides the following endpoint:eg 

json
GET /transactions
[
  {
    "id": 1,
    "description": "Salary",
    "amount": 50000,
    "type": "income"
  },
  {
    "id": 2,
    "description": "Groceries",
    "amount": 2000,
    "type": "expense"
  }
]

<!-- Add Transactions -->
Use the "Add Transaction" form to submit new transactions. These transactions are sent to the server:

json
POST /transactions
{
  "id": 3,
  "description": "Utilities",
  "amount": 1500,
  "type": "expense"
}

<!-- Delete Transactions -->
Click the "Delete" button next to a transaction to remove it. It sends a DELETE request to the server:

json
DELETE /transactions/3
Search Transactions
Enter keywords in the search bar to filter transactions by description.

 <!-- // Data Structure -->
  The database consists of an array of transaction objects under the key transactions. Each transaction has the following properties:
  
  Fields:
  id: A unique identifier for the transaction.
  
  Type: String or Number
  
  Example: "1" or 1734676788999
  
  description: A brief description of the transaction.
  
  Type: String
  
  Example: "Salary", "Groceries", "Transportation"
  
  amount: The monetary value associated with the transaction.
  
  Type: Number
  
  Example: 50000, 8000
  
  type: Specifies whether the transaction is an income or expense.
  
  Type: String
  
  Values: "income" or "expense"

  <!-- API Endpoints: The server will expose the following endpoints: -->

Get All Transactions: GET /transactions

Add a Transaction: POST /transactions

Update a Transaction: PUT /transactions/:id

Delete a Transaction: DELETE /transactions/:id




