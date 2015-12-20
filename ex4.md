# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 4η

Σε αυτήν την άσκηση θα δούμε πως επηρέαζει η JavaScript τη μορφοποίηση, δηλαδή το styling μιας σελίδας.

1) Δημιουργούμε έναν φάκελο στην επιφάνεια εργασίας με το όνομα `ex4` και ένα νέο αρχείο με το όνομα `ex4.html`.

2) Πληκτρολογούμε τα παρακάτω αναγκαία tags:
```HTML
<!DOCTYPE html>
<html>
    <head>
      <title>Example 4 - JS</title>
    </head>
    <body>
        
    </body>
</html> 
```

3) Μέσα στο `body` βάζουμε ένα text input και ένα κουμπί:
```HTML
Color: <input type="text" name="color" id="bgColor" ><br>
<button onclick="colorMe()">Change the Color</button>
```

5) Έπειτα στο `head` γράφουμε το εξής script:
```HTML
<script>
  function colorMe() {
    document.body.style.backgroundColor = document.getElementById("bgColor").value; 
  }
</script>
```

6) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε τη σελίδα.

7) Στο πεδίο κειμένου πληκτρολογούμε ένα χρώμα στα αγγλικά και πατάμε το κουμπί.
