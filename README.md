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
      <?php
    // Open the file for writing
    $file = fopen("test.txt", "w") or die("Unable to open file!");

    // Get the data from the HTML form
    $name = $_POST["firstName"];
    $surname = $_POST["lastName"];
    $street = $_POST["address"];

    // Write the data to the file
    fwrite($file, "Name: $name\n");
    fwrite($file, "Surname: $surname\n");
    fwrite($file, "Address: $street\n");

    // Close the file
    fclose($file);

    // Display a confirmation message
    echo "Your data has been saved to test.txt";
    ?>
     
    });
  </script>
</body>
</html>
