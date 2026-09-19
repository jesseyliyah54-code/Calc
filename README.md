<!DOCTYPE html>
<html>
<head>
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f2f2f2;
    }

    .calculator {
      width: 280px;
      padding: 20px;
      background: white;
      border-radius: 15px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.2);
    }

    #display {
      width: 100%;
      height: 60px;
      font-size: 25px;
      text-align: right;
      margin-bottom: 15px;
      box-sizing: border-box;
      padding: 10px;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }

    button {
      height: 55px;
      font-size: 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      opacity: 0.8;
    }

    .operator {
      background: #ddd;
    }

    .equals {
      background: #4CAF50;
      color: white;
    }

    .clear {
      background: #f44336;
      color: white;
    }
  </style>
</head>

<body>

  <div class="calculator">
    <input type="text" id="display" readonly>

    <div class="buttons">
      <button class="clear" onclick="clearDisplay()">C</button>
      <button onclick="deleteLast()">⌫</button>
      <button class="operator" onclick="addToDisplay('%')">%</button>
     
