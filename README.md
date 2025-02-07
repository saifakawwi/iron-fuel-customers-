
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iron Fuel Customer Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        .counter-container {
            max-width: 400px;
            margin: 100px auto;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        h1 {
            color: #333;
        }
        p {
            font-size: 24px;
            color: #555;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="counter-container">
        <h1>Iron Fuel Customer</h1>
        <p id="visitorCounter">0 customers</p>
    </div>

    <script>
        // Visitor Counter Logic
        let visitorCount = localStorage.getItem('visitorCount') ? parseInt(localStorage.getItem('visitorCount')) : 0;
        visitorCount++;
        localStorage.setItem('visitorCount', visitorCount);
        document.getElementById('visitorCounter').textContent = `${visitorCount} customers`;
    </script>
</body>
</html>
