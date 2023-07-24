# surphae.github.io
<!DOCTYPE html>
<html>
<head>
  <title>Capture Name and Surname</title>
</head>
<body>
  <form id="nameForm">
    <label for="firstName">First Name:</label>
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
  
      // You can also send the captured data to a server using AJAX or fetch API
      // Here's an example using fetch:
      /*fetch('https://example.com/submit', {
        method: 'POST',
        body: JSON.stringify({ firstName: firstName, lastName: lastName }),
        headers: {
          'Content-Type': 'application/json'
        }
      }).then(function(response) {
        // Handle the response from the server
      });*/
    });
  </script>
  
  <?php
    // Open the file for writing
    $file = fopen("test.txt", "w") or die("Unable to open file!");

    // Get the data from the HTML form
    $name = firstName;
    $surname = lastName;
    $street = address;

    // Write the data to the file
    fwrite($file, "Name: $name\n");
    fwrite($file, "Surname: $surname\n");
    fwrite($file, "Address: $street\n");

    // Close the file
    fclose($file);

    // Display a confirmation message
    echo "Your data has been saved to test.txt";
    ?>
  
</body>
</html>
