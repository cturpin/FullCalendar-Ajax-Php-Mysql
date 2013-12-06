<?php
// Values received via ajax
$title = $_POST['title'];
$start = $_POST['start'];
$end = $_POST['end'];

// connection to the database
try {
$bdd = new PDO('mysql:host=localhost;dbname=fullcalendar', 'root', '');
} catch(Exception $e) {
exit('Unable to connect to database.');
}

// insert the records
$sql = "INSERT INTO evenement (title, start, end) VALUES (:title, :start, :end )";
$q = $bdd->prepare($sql);
$q->execute(array(':title'=>$title, ':start'=>$start, ':end'=>$end));
?>
