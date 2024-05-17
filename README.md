# 9th

<!DOCTYPE html> 
<html> 
<head> 
  <title>Arithmetic Operations Program</title> 
  <script> 
    function performOperation(num1, num2, operator) { 
      var result; 
 
      switch (operator) { 
        case '+': 
          result = num1 + num2; 
          break; 
        case '-': 
          result = num1 - num2; 
          break; 
        case '*': 
          result = num1 * num2; 
          break; 
        case '/': 
          result = num1 / num2; 
          break; 
        default: 
          result = 'Invalid operator.'; 
          break; 
      } 
 
      return result; 
    } 
 
    function calculate() { 
      var num1 = parseFloat(document.getElementById('num1').value); 
      var num2 = parseFloat(document.getElementById('num2').value); 
      var operator = document.getElementById('operator').value; 
      var output = document.getElementById('output'); 
 
      if (isNaN(num1) || isNaN(num2)) { 
        output.innerHTML = 'Invalid input. Please enter valid numbers.'; 
      } else { 
        var result = performOperation(num1, num2, operator); 
        output.innerHTML = 'Result: ' + result; 
      } 
    } 
  </script> 
</head> 
<body> 
  <h1>Arithmetic Operations Program</h1> 
 
  <label for="num1">Number 1:</label> 
  <input type="number" id="num1" placeholder="Enter a number"> 
  <br> 
  <label for="num2">Number 2:</label> 
  <input type="number" id="num2" placeholder="Enter a number"> 
  <br> 
  <label for="operator">Operator:</label> 
  <select id="operator"> 
    <option value="+">+</option> 
    <option value="-">-</option> 
<option value="*">*</option> 
<option value="/">/</option> 
</select> 
<br> 
<button onclick="calculate()">Calculate</button> 
<p id="output"></p> 
</body> 
</html> 
