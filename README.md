
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Cards</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="card card1">
            <h2>Card 1</h2>
            <p>This is a simple card with a shadow effect.</p>
        </div>
        <div class="card card2">
            <h2>Card 2</h2>
            <p>This card has a flip effect on hover.</p>
        </div>
        <div class="card card3">
            <h2>Card 3</h2>
            <p>This card zooms in on hover.</p>
        </div>
    </div>
</body>
</html>
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f5f5f5;
}

.container {
    display: flex;
    gap: 20px;
}

.card {
    background-color: white;
    border-radius: 10px;
    padding: 20px;
    width: 250px;
    text-align: center;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s;
}

.card h2 {
    margin: 0 0 10px;
}

.card p {
    color: #555;
}
.card1:hover {
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
.card2 {
    perspective: 1000px;
}

.card2-inner {
    position: relative;
    width: 100%;
    height: 100%;
    transition: transform 0.6s;
    transform-style: preserve-3d;
}

.card2:hover .card2-inner {
    transform: rotateY(180deg);
}

.card2 .card2-front,
.card2 .card2-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
}
.card2 .card2-back {
    transform: rotateY(180deg);
    background-color: #007BFF;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
}
.card3:hover {
    transform: scale(1.05);
    box-shadow: 0 16px 32px rgba(0, 0, 0, 0);
		}

<div class="card card2">
    <div class="card2-inner">
        <div class="card2-front">
            <h2>Card 2</h2>
            <p>This card has a flip effect on hover.</p>
        </div>
        <div class="card2-back">
            <h2>Card 2 Back</h2>
            <p>More information here!</p>
        </div>
    </div>
</div>
</body>
</html>
