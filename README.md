
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Office Store PH</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f4f4;
    }

    header {
      background: #0078D4;
      color: white;
      padding: 15px;
      text-align: center;
    }

    .container {
      padding: 20px;
    }

    .product {
      background: white;
      padding: 15px;
      margin: 15px 0;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    button {
      background: #0078D4;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }

    button:hover {
      background: #005fa3;
    }

    footer {
      text-align: center;
      padding: 10px;
      background: #222;
      color: white;
      margin-top: 20px;
    }
  </style>
</head>
<body>

<header>
  <h1>Office Store PH</h1>
  <p>Affordable Microsoft Office Licenses</p>
</header>

<div class="container">

  <div class="product">
    <h2>Microsoft Office 2021</h2>
    <p>One-time purchase for PC</p>
    <h3>₱2,999</h3>
    <button onclick="buy('Office 2021')">Buy Now</button>
  </div>

  <div class="product">
    <h2>Microsoft 365 Personal</h2>
    <p>1-year subscription</p>
    <h3>₱3,499</h3>
    <button onclick="buy('Microsoft 365 Personal')">Buy Now</button>
  </div>

  <div class="product">
    <h2>Microsoft 365 Family</h2>
    <p>Up to 6 users</p>
    <h3>₱4,999</h3>
    <button onclick="buy('Microsoft 365 Family')">Buy Now</button>
  </div>

</div>

<footer>
  <p>Contact: your@email.com | GCash Available</p>
</footer>

<script>
  function buy(product) {
    alert("You selected: " + product + "\nMessage us to complete your order!");
  }
</script>

</body>
</html>
