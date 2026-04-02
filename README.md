
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Microsoft Office Licensed Activated</title>

<style>
/* --- General Styles --- */
body {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    font-family: Arial, sans-serif;
    margin: 0;
    background: #f4f6f8;
    color: #333;
}

#store {
    flex: 1;
}

/* --- Header --- */
header {
    background: #0078D7;
    color: white;
    text-align: center;
    padding: 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

/* --- Hero Section --- */
.hero {
    text-align: center;
    padding: 40px 15px;
    background: white;
    margin: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}

.hero img {
    width: 100px;
    margin-bottom: 15px;
}

.price {
    font-size: 28px;
    color: #28a745;
    margin: 10px 0;
    font-weight: bold;
}

.btn {
    background: #0078D7;
    color: white;
    padding: 14px;
    width: 100%;
    max-width: 250px;
    border: none;
    font-size: 16px;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s ease;
}

.btn:hover {
    background: #005ea6;
}

/* --- Sections --- */
.section {
    margin: 20px;
    background: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}

/* --- Features Grid --- */
.features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 15px;
}

.feature {
    background: #f0f4f8;
    padding: 15px;
    border-radius: 8px;
    text-align: center;
    font-weight: 600;
}

/* --- Form Inputs --- */
input {
    width: 100%;
    padding: 12px;
    margin: 8px 0;
    border-radius: 5px;
    border: 1px solid #ccc;
}

/* --- Payment Box --- */
.payment-box {
    background: #e3f2fd;
    padding: 15px;
    border-radius: 5px;
    margin-top: 10px;
}

/* --- Dashboard Tables --- */
.checkout-dashboard, .admin {
    display: none;
}

.checkout-dashboard table, .admin table {
    width: 100%;
    border-collapse: collapse;
}

.checkout-dashboard th, .checkout-dashboard td, 
.admin th, .admin td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: center;
}

.checkout-dashboard td {
    cursor: text;
}

/* --- Policies Section --- */
.policies {
    background: #f0f0f0;
    color: #333;
    font-size: 14px;
    padding: 20px;
    border-radius: 10px;
    line-height: 1.6;
}

.policies h3 {
    color: #0078D7;
}

/* --- Footer --- */
footer {
    background: #0078D7;
    color: white;
    text-align: center;
    padding: 15px;
    font-weight: bold;
}

/* --- Responsive --- */
@media (max-width: 600px) {
    .features {
        grid-template-columns: 1fr;
    }
}
</style>
</head>

<body>

<header>
    <h2>Microsoft Office Licensed Activated</h2>
</header>

<div id="store">

<div class="hero">
    <img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Microsoft_logo.svg" alt="Microsoft">
    <h3>Get the full Microsoft Office suite for your PC</h3>
    <div class="price">₱199</div>
    <button class="btn" onclick="scrollToCheckout()">Buy Now</button>
    <p id="confirmation-msg" style="color:green;margin-top:10px;"></p>
</div>

<div class="section">
    <h3>Included Apps</h3>
    <div class="features">
        <div class="feature">Word</div>
        <div class="feature">Excel</div>
        <div class="feature">PowerPoint</div>
        <div class="feature">Outlook</div>
        <div class="feature">OneNote</div>
        <div class="feature">Access</div>
        <div class="feature">Publisher</div>
    </div>
</div>

<div class="section">
    <h3>Payment Instructions</h3>
    <div class="payment-box">
        <p><strong>Send to:</strong> 09157406673</p>
        <p><strong>Amount:</strong> ₱199</p>
        <p>After payment, fill the form below to simulate order submission.</p>
    </div>
</div>

<div class="section">
    <h3>Checkout</h3>
    <form onsubmit="submitOrder(event)">
        <input type="text" placeholder="Full Name" required>
        <input type="email" placeholder="Email" required>
        <input type="text" placeholder="Payment Reference" required>
        <button class="btn">Submit Order</button>
    </form>
</div>

<div class="section">
    <h3>Checkout Dashboard</h3>
    <button class="btn" style="background:#dc3545;margin-bottom:10px;" onclick="clearOrders()">Clear All Orders</button>
    <div class="checkout-dashboard">
        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Email</th>
                    <th>Reference</th>
                </tr>
            </thead>
            <tbody id="checkout-orders"></tbody>
        </table>
    </div>
</div>

<div class="section">
    <h3>Contact</h3>
    <p>Facebook: <a href="https://www.facebook.com/share/1CX8kZ4VGk/" target="_blank">https://www.facebook.com/share/1CX8kZ4VGk/</a></p>
</div>

<div class="section policies">
    <h3>Instructions & Policies</h3>
    <ul>
        <li>Keep your email updated to see simulated confirmations.</li>
        <li>Fill up the checkout form.</li>
        <li><strong style="color:#0078D7;">Contact me in Facebook after the checkout form.</strong></li>
        <li>If you encounter any issues or errors, please contact us on Facebook.</li>
    </ul>
</div>

</div>

<!-- Footer -->
<footer>
    JP Mini-Store
</footer>

<script>
// Orders stored in localStorage
let orders = JSON.parse(localStorage.getItem("orders")) || [];

// Save orders
function saveOrders() {
    localStorage.setItem("orders", JSON.stringify(orders));
}

// Render Checkout Dashboard
function renderCheckoutDashboard() {
    const table = document.getElementById("checkout-orders");
    table.innerHTML = "";
    orders.forEach((o, index) => {
        table.innerHTML += `
            <tr>
                <td contenteditable="true" onblur="updateOrder(${index}, 'name', this.innerText)">${o.name}</td>
                <td contenteditable="true" onblur="updateOrder(${index}, 'email', this.innerText)">${o.email}</td>
                <td contenteditable="true" onblur="updateOrder(${index}, 'ref', this.innerText)">${o.ref}</td>
            </tr>
        `;
    });
    document.querySelector(".checkout-dashboard").style.display = orders.length ? "block" : "none";
}

// Update order
function updateOrder(index, field, value) {
    orders[index][field] = value.trim();
    saveOrders();
}

// Submit order
function submitOrder(e) {
    e.preventDefault();
    let inputs = e.target.querySelectorAll("input");
    const order = {
        name: inputs[0].value,
        email: inputs[1].value,
        ref: inputs[2].value
    };
    orders.push(order);
    saveOrders();
    renderCheckoutDashboard();
    document.getElementById("confirmation-msg").innerText = "Order submitted successfully!";
    e.target.reset();
}

// Clear orders
function clearOrders() {
    if(confirm("Are you sure you want to clear all orders?")) {
        orders = [];
        saveOrders();
        renderCheckoutDashboard();
        document.getElementById("confirmation-msg").innerText = "All orders cleared.";
    }
}

// Scroll to checkout
function scrollToCheckout() {
    document.querySelector(".section form").scrollIntoView({ behavior: "smooth" });
}

// Initial render
renderCheckoutDashboard();
</script>

</body>
</html>