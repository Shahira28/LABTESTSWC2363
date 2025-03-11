<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cookie Sales System</title>
    <style>
        table {
            width: 50%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        table, th, td {
            border: 1px solid black;
        }
        th, td {
            padding: 8px;
            text-align: left;
        }
    </style>
</head>
<body>
    <h1>Cookie Sales System</h1>
    <form method="post" action="cookies_sales.php">
        <label for="name">Customer Name:</label><br>
        <input type="text" id="name" name="name" required><br><br>

        <label for="cookie">Cookie Selection:</label><br>
        <select name="cookie" id="cookie">
            <option value="Pineapple Tarts">Pineapple Tarts - RM25</option>
            <option value="Almond London">Almond London - RM30</option>
            <option value="Kuih Bangkit">Kuih Bangkit - RM20</option>
            <option value="Semperit">Semperit - RM22</option>
            <option value="Sugee Cookies">Sugee Cookies - RM28</option>
        </select><br><br>

        <label for="quantity">Quantity (per container):</label><br>
        <input type="number" id="quantity" name="quantity" required><br><br>

        <label for="delivery">Delivery Option:</label><br>
        <select name="delivery" id="delivery">
            <option value="Self-Pickup">Self-Pickup</option>
            <option value="Standard Delivery">Standard Delivery</option>
            <option value="Express Delivery">Express Delivery</option>
        </select><br><br>

        <input type="submit" 
    /form>
    </form>

    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        // Step 2: Handle form input
        $customer_name = $_POST['name'];
        $cookie = $_POST['cookie'];
        $quantity = $_POST['quantity'];
        $delivery_option = $_POST['delivery'];

        // Define cookie prices
        $cookie_prices = [
            "Pineapple Tarts" => 25,
            "Almond London" => 30,
            "Kuih Bangkit" => 20,
            "Semperit" => 22,
            "Sugee Cookies" => 28
        ];

        // Define delivery charges
        $delivery_charges = [
            "Self-Pickup" => 0,
            "Standard Delivery" => 10,
            "Express Delivery" => 20
        ];

        // Step 3: Calculate the total cost
        $cookie_price = $cookie_prices[$cookie];
        $delivery_charge = $delivery_charges[$delivery_option];

        $cookie_cost = $cookie_price * $quantity;

        // Step 4: Apply discount if applicable
        $discount = 0;
        if ($quantity >= 5) {
            $discount = 0.05 * $cookie_cost;  // 5% discount for 5 or more containers
        }

        // Total cost calculation
        $total_cost = $cookie_cost - $discount + $delivery_charge;
    ?>
    <! Step 5: Display results in a table >
    <h2>Order Summary</h2>
    <table>
        <tr>
            <th>Customer Name</th>
            <td><?php echo $customer_name; ?></td>
        </tr>
        <tr>
            <th>Cookie Type</th>
            <td><?php echo $cookie; ?></td>
        </tr>
        <tr>
            <th>Quantity</th>
            <td><?php echo $quantity; ?></td>
        </tr>
        <tr>
            <th>Price per Container</th>
            <td>RM<?php echo number_format($cookie_price, 2); ?></td>
        </tr>
        <tr>
            <th>Delivery Option</th>
            <td><?php echo $delivery_option; ?></td>
        </tr>
        <tr>
            <th>Discount</th>
            <td>-RM<?php echo number_format($discount, 2); ?></td>
        </tr>
        <tr>
            <th>Delivery Charge</th>
            <td>RM<?php echo number_format($delivery_charge, 2); ?></td>
        </tr>
        <tr>
            <th>Total Estimated Cost</th>
            <td>RM<?php echo number_format($total_cost, 2); ?></td>
        </tr>
    </table>
    <?php
    }
    ?>
 <?php if (!empty($price)): ?>
        <h3>TotalCost for <?php echo htmlspecialchars($CustomerName); ?></h3>
        <table border="1">
            <tr>
                <th>CustomerName</th>
                <th>CookiesType (20%)</th>
                <th>QuantityOfCookies (10%)</th>
                <th>PricePerContainer (30%)</th>
                <th>DeliveryOption (40%)</th>
                
            <?php foreach ($cookies as $price => $data): ?>
                <tr>
                    <td><?php echo htmlspecialchars($subject); ?></td>
                    <td><?php echo $data['cookie_cost']['cookie_price']; ?></td>
                    <td><?php echo $data['price_percontainer']['quantity of cookies']; ?></td>
                    <td><?php echo $data['price_percontainer']['price_percontainer']; ?></td>
                    <td><?php echo $data['delivery_option']['delivery_charge']; ?></td>
                </tr>
            <?php endforeach; ?>
        </table>
    <?php endif; ?>
</body>
</html></body>
</html>
