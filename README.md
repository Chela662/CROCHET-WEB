<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yvonne's Crochet</title>
    <style>
        body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 0;
    background-color: #f9f5f0;
}
.container {
    max-width: 700px;
    margin: 20px auto;
    padding: 20px;
}
button {
    background-color: #ff7f50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}
button:hover {
    background-color: #ff5722;
}
  
    </style>
    <script>
        
  document.addEventListener("DOMContentLoaded", function() {
    const form = document.querySelector("form");
    const button = document.querySelector("button[type='submit']");
    const dateInput = document.querySelector("input[name='delivery_date']");

    form.addEventListener("submit", function(e) {
      // Validate delivery date
      const selectedDate = new Date(dateInput.value);
      const today = new Date();
      today.setHours(0, 0, 0, 0);

      if (dateInput.value && selectedDate < today) {
        e.preventDefault();
        alert("Please choose a valid delivery date (not in the past).");
        return;
      }

      // Disable button to prevent multiple submissions
      button.innerText = "Submitting...";
      button.disabled = true;

      // Show thank you message
      alert("Thank you for your order! We'll get back to you soon.");
    });
  });


    </script>
</head>

<body>
   
    <h1>
       Welcome to Yvonne's crochet
    </h1>
    <h2>
        My name is Yvonne, and I am a crochet artist.
    </h2>
    <div class="container">
    <p>
        I am passionate about creating unique and beautiful crochet items. 
        From cozy sweaters to stylish bags, I pour my heart into every piece I make.
        <br>
        <img src="crochet.jpg" width="150" height="200">
        <img src="tote.jpg" width="150" height="200">
        <img src="sweater.jpg" width="150" height="200">
        <img src="hat.jpg" width="150" height="200">
    </p>
    </div>
        <div class= "container">
        <h2>This my art.handmade with love!</h2>
        <p>Explore my collections that i made with much care and creativity</p>
        
        
    </div>
    
  <h1>Place Your Order</h1>
  <form action="submit_order.php" method="POST" class="container">
    <label>Name:</label><br>
    <input type="text" name="name" required><br><br>

    <label>Email:</label><br>
    <input type="email" name="email" required><br><br>

    <label>Item Description:</label><br>
    <textarea name="description" rows="4" cols="40" placeholder="What would you like to order?" required></textarea><br><br>

    <label>Preferred Delivery Date:</label><br>
    <input type="date" name="delivery_date"><br><br>

    <button type="submit">Submit Order</button>
    

    <h2>About Us</h2>
    <p>
        I make all sorts of items and all designs depending with dear client's order.
        <h2>contact us</h2>
        <p>
            Phone no: 0700043535
        </p>
        <p>
            Instagram:@y.crochet
        </p>
    </p>
</body>
</html># CROCHET-WEB
