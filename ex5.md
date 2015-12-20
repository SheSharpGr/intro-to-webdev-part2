# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 5η

Σε αυτήν την άσκηση θα παίξουμε με τις εικόνες και τα events onmouseover/onmouseout/onclick.

1) Δημιουργούμε έναν φάκελο στην επιφάνεια εργασίας με το όνομα `ex5` και ένα νέο αρχείο με το όνομα `ex5.html`.

2) Πληκτρολογούμε τα παρακάτω αναγκαία tags:
```HTML
<!DOCTYPE html>
<html>
    <head>
      <title>Example 5 - JS</title>
    </head>
    <body>
        
    </body>
</html> 
```

3) Φτιάχνουμε έναν υποφάκελο μέσα στον `ex5` με το όνομα `images` και βάζουμε μέσα 3 εικόνες: [html.png](https://raw.githubusercontent.com/SheSharpGr/intro-to-webdev-part2/master/resources/html.png), [css.png](https://raw.githubusercontent.com/SheSharpGr/intro-to-webdev-part2/master/resources/css.png) και [js.png](https://raw.githubusercontent.com/SheSharpGr/intro-to-webdev-part2/master/resources/js.png).

4) Μέσα στο `body` γράφουμε το παρακάτω:
```HTML
<section id="gallery">
  <img id="myIMG" src="images/html.png" alt="Just another image" onmouseover="changeIMG()" />
</section>
```

5) Στο `head` προσθέτουμε styling για την εικόνα:
```HTML
<style>
  img {
    width: 600px;
    margin: 50px auto;
  }

  section#gallery{
    margin: 10px auto;
    text-align: center;
    width: 800px;
  }
</style>
```

6) Συνεχίσουμε στο `head` και προσθέτουμε script για την αλλαγή της εικόνας μόλις περάσει το ποντικί πάνω από τη φωτογραφία (`onmouseover`).
```HTML
<script>
  function changeIMG(){
    document.getElementById("myIMG").src = "images/css.png";
  }
</script>
```

7) Αποθηκεύουμε τις αλλαγές μας στο αρχείο `ex5.html` και τρέχουμε τη σελίδα.

8) Στη συνέχεια θέλουμε η εικόνα να επιστρέφει στη προηγούμενη μόλις φύγει το ποντικί από πάνω της (`onmouseout`). Για αυτό προσθέτουμε ακόμη μία μέθοδο στο `script`:
```JS
function returnIMG(this){
  this.src = "images/html.png";
}
```

9) Έπειτα πρέπει να προσθέσουμε και το ανάλογο event, στην περίπτωσή μας το `onmouseout` πάνω στην εικόνα. Οπότε αλλάζουμε τον κώδικα της εικόνας:
```HTML
  <img id="myIMG" src="images/html.png" alt="Just another image" onmouseover="changeIMG()" onmouseout="returnIMG(this)" />
```

10) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε και πάλι την σελίδα.

11) Τέλος, θέλουμε να αλλάζει η εικόνα και όταν κάνουμε κλικ πάνω της σε μία τρίτη. Για αυτό θα χρησιμοποιήσουμε το event `onclick`.

12) Αλλάζουμε το κώδικα της σελίδας με το παρακάτω:
```HTML
  <img id="myIMG" src="images/html.png" alt="Just another image" onmouseover="changeIMG()" onmouseout="returnIMG(this)" onclick="this.src='images/js.png'" />
```

13) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε την σελίδα.
