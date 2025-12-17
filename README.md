<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pigmy Lite</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f6ff;
      margin: 0;
      padding: 0;
    }
    header {
      background: #2b59ff;
      color: white;
      padding: 15px;
      text-align: center;
      font-size: 20px;
    }
    .container {
      padding: 20px;
    }
    .card {
      background: white;
      padding: 15px;
      border-radius: 10px;
      margin-bottom: 15px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .amount {
      font-size: 28px;
      color: #2b59ff;
      font-weight: bold;
    }
    button {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 8px;
      background: #2b59ff;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background: #1e3fd6;
    }
    input {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 10px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 16px;
    }
    footer {
      text-align: center;
      padding: 10px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>

<header>Pigmy Lite</header>

<div class="container">

  <div class="card">
    <h3>Total Savings</h3>
    <div class="amount">₹ <span id="total">1250</span></div>
  </div>

  <div class="card">
    <h3>Save Money</h3>
    <input type="number" id="saveAmount" placeholder="Enter amount (10 / 20 / 50)">
    <button onclick="saveMoney()">Save Today</button>
  </div>

  <div class="card">
    <h3>My Goal</h3>
    <p>Festival Savings</p>
    <p>Target: ₹5,000</p>
  </div>

</div>

<footer>
  Simple IDT Prototype | Pigmy Lite App
</footer>

<script>
  let total = 1250;

  function saveMoney() {
    let amount = document.getElementById("saveAmount").value;

    if (amount === "" || amount <= 0) {
      alert("Please enter a valid amount");
      return;
    }

    total = total + parseInt(amount);
    document.getElementById("total").innerText = total;
    document.getElementById("saveAmount").value = "";

    alert("₹" + amount + " saved successfully!");
  }
</script>

</body>
</html>
