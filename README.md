# Haynes_SDC310_wk2PA
<?php
// Initialize variables
$name = "";
$dob = "";
$color = "";
$place = "";
$nickname = "";

// Check if form was submitted
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'] ?? "";
    $dob = $_POST['dob'] ?? "";
    $color = $_POST['color'] ?? "";
    $place = $_POST['place'] ?? "";
    $nickname = $_POST['nickname'] ?? "";
}
?>

<!DOCTYPE html>
<html>
<head>
    <title>Jonathan Haynes Wk2 PA</title>
</head>
<body>

<h1>Jonathan Haynes Wk2 PA</h1>

<form method="post">
    Name: <input type="text" name="name"><br><br>

    Date of Birth: <input type="date" name="dob"><br><br>

    Favorite Color: <input type="text" name="color"><br><br>

    Favorite Place to Visit: <input type="text" name="place"><br><br>

    Nickname: <input type="text" name="nickname"><br><br>

    <input type="submit" value="Submit">
</form>

<hr>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    echo $name ? "Your name is $name<br>" : "You didn't enter your name<br>";
    echo $dob ? "Your date of birth is $dob<br>" : "You didn't enter your date of birth<br>";
    echo $color ? "Your favorite color is $color<br>" : "You didn't enter your favorite color<br>";
    echo $place ? "Your favorite place to visit is $place<br>" : "You didn't enter your favorite place<br>";
    echo $nickname ? "Your nickname is $nickname<br>" : "You didn't enter your nickname<br>";
}
?>

</body>
</html>
