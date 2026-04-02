<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Microsoft Office Licensed Activated ₱199</title>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #f5f5f5;
}

header {
    background: #0078D7;
    color: white;
    text-align: center;
    padding: 15px;
}

.hero {
    text-align: center;
    padding: 30px 15px;
    background: white;
}

.hero img {
    width: 120px;
}

.price {
    font-size: 30px;
    color: green;
    margin: 10px 0;
}

.btn {
    background: #28a745;
    color: white;
    padding: 14px;
    width: 100%;
    max-width: 300px;
    border: none;
    font-size: 16px;
    border-radius: 5px;
    cursor: pointer;
}

.section {
    margin: 15px;
    background: white;
    padding: 20px;
    border-radius: 8px;
}

.features {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

.feature {
    background: #eee;
    padding: 10px;
    border-radius: 5px;
    text-align: center;
}

input {
    width: 100%;
    padding: 12px;
    margin: 8px 0;
}

.payment-box {
    background: #e8f5e9;
    padding: 15px;
    border-radius: 5px;
    margin-top: 10px;
}

.admin {
    display: none;
}

.admin table {
    width: 100%;
    border-collapse: collapse;
}

.admin th, .admin td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: center;
}

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
    <h3>Get Microsoft Office Licensed Activated for ₱199</h3>
    <div class="price">₱199</div>
    <button class="btn" onclick="scrollToCheckout()">Buy Now</button>
</div>

<div class="section">
    <h3>Includes</h3>
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
    <h3>Payment (GCash)</h3>
    <div class="payment-box">
        <p><strong>Send to:</strong> 09157406673</p>
        <p><strong>Amount:</strong> ₱199</p>
        <p>After payment, fill the form below.</p>
    </div>
</div>

<div class="section">
    <h3>Checkout</h3>
    <form onsubmit="submitOrder(event)">
        <input type="text" placeholder="Full Name" required>
        <input type="email" placeholder="Email" required>
        <input type="text" placeholder="GCash Reference Number" required>
        <button class="btn">Submit Order</button>
    </form>
</div>

<div class="section">
    <h3>Contact</h3>
    <p>Facebook: <a href="https://www.facebook.com/share/1CX8kZ4VGk/" target="_blank">https://www.facebook.com/share/1CX8kZ4VGk/</a></p>
</div>

</div>

<div id="admin" class="admin section">
    <h3>Admin Dashboard</h3>
    <button class="btn" onclick="showStore()">Back to Store</button>
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Email</th>
                <th>Reference</th>
            </tr>
        </thead>
        <tbody id="orders"></tbody>
    </table>
</div>

<script>
let orders = [];

function scrollToCheckout() {
    document.querySelector(".section form").scrollIntoView({ behavior: "smooth" });
}

function submitOrder(e) {
    e.preventDefault();

    let inputs = e.target.querySelectorAll("input");

    let order = {
        name: inputs[0].value,
        email: inputs[1].value,
        ref: inputs[2].value
    };

    orders.push(order);
    renderOrders();

    alert("Order submitted! Wait for confirmation via email.");

    e.target.reset();
}

function renderOrders() {
    let table = document.getElementById("orders");
    table.innerHTML = "";

    orders.forEach(o => {
        table.innerHTML += `
            <tr>
                <td>${o.name}</td>
                <td>${o.email}</td>
                <td>${o.ref}</td>
            </tr>
        `;
    });
}

if (window.location.hash === "#admin") {
    document.getElementById("store").style.display = "none";
    document.getElementById("admin").style.display = "block";
}

function showStore() {
    document.getElementById("store").style.display = "block";
    document.getElementById("admin").style.display = "none";
}
</script>

</body>
</html>