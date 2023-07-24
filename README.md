# surphae.github.io
<!DOCTYPE html>
<html>
<head>
  <title>Capture Name and Surname</title>
</head>
<body>
  <form id="nameForm">
    <label for="firstName">First Name: </label>
    <input type="text" id="firstName" required><br><br>
     <label for="lastName">Last Name:</label>
    <input type="text" id="lastName" required><br><br>
    <label for="Address">Address:</label>
    <input type="text" id="address" required><br><br>
    <input type="submit" value="Submit">
  </form>
 
  <script>
    document.getElementById('nameForm').addEventListener('submit', function(event) {
      event.preventDefault(); // Prevent form submission
  
      // Get the values from the input fields
      var firstName = document.getElementById('firstName').value;
      var lastName = document.getElementById('lastName').value;
      var address = document.getElementById('address').value;
      
  
      // Do something with the captured name and surname
      alert('Hello, ' + firstName + ' ' + lastName + ' ' + address + '!');
  
     
    });
  </script>
</body>
</html>
