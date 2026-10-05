# Expense-tracker
A simple web application to track income, expenses, and manage personal finances
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Expense Tracker</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">

        <h1>💰 Expense Tracker</h1>
        <p class="subtitle">Manage your income and expenses easily</p>

        <!-- Balance -->
        <div class="balance-card">
            <h3>Current Balance</h3>
            <h2 id="balance">₹0.00</h2>
        </div>

        <!-- Income and Expense -->
        <div class="summary">
            <div class="summary-box income">
                <h3>Total Income</h3>
                <p id="income">₹0.00</p>
            </div>

            <div class="summary-box expense">
                <h3>Total Expense</h3>
                <p id="expense">₹0.00</p>
            </div>
        </div>

        <!-- Add Transaction -->
        <div class="card">
            <h2>Add Transaction</h2>

            <form id="transactionForm">

                <label for="description">Description</label>
                <input
                    type="text"
                    id="description"
                    placeholder="e.g. Grocery shopping"
                    required
                >

                <label for="amount">Amount</label>
                <input
                    type="number"
                    id="amount"
                    placeholder="Enter amount"
                    min="1"
                    step="0.01"
                    required
                >

                <label for="type">Transaction Type</label>
                <select id="type">
                    <option value="expense">Expense</option>
                    <option value="income">Income</option>
                </select>

                <label for="category">Category</label>
                <select id="category">
                    <option value="Food">Food</option>
                    <option value="Shopping">Shopping</option>
                    <option value="Travel">Travel</option>
                    <option value="Bills">Bills</option>
                    <option value="Entertainment">Entertainment</option>
                    <option value="Salary">Salary</option>
                    <option value="Other">Other</option>
                </select>

                <button type="submit">Add Transaction</button>

            </form>
        </div>

        <!-- Transaction History -->
        <div class="card">
            <h2>Transaction History</h2>

            <ul id="transactionList"></ul>

            <p id="emptyMessage" class="empty">
                No transactions yet.
            </p>
        </div>

    </div>

    <script src="script.js"></script>

</body>
</html>
