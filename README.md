# fraserhacks
<?
<?php


if($weight=="" OR $height==""){
echo "<p></p>";
}

else{

   if ($_GET['submit']){
function calcBMI($weight,$height) {
     $top = $weight*70.3;
     $bottom = pow($height,2);
     $BMI = $top/$bottom;
     return $BMI;
}

calcBMI($weight,$height);
$BMI = calcBMI($weight,$height);

if ( calcBMI($weight,$height) < 18.5) {
echo "<p>";
$judgeme = "underweight. <br /><br />";
echo "</p>";
}

if ( calcBMI($weight,$height) < 24.9 AND calcBMI($weight,$height)>18.5) {
echo "<p>";
$judgeme = "normal weight. <br /><br />";
echo "</p>";
}

if ( calcBMI($weight,$height) < 25.0 AND calcBMI($weight,$height)>29.9) {
echo "<p>";
$judgeme = "overweight. <br /><br />";
echo "</p>";
}

if ( calcBMI($weight,$height) > 30.0 ) {
echo "<p>";
$judgeme = "obese. <br /><br />";
echo "</p>";
}





echo "<p>Your BMI is ";
echo 10*(calcBMI($weight,$height));
echo ". This means you are "; 
echo $judgeme;
echo "</p>";
}
}
?>
