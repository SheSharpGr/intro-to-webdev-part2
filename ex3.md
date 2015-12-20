# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 3η

Σε αυτή την άσκηση θα δούμε πως μπορεί η JavaScript να πειράξει τις ιδιότητες των elements της HTML.

1) Δημιουργούμε έναν φάκελο στην επιφάνεια εργασίας με το όνομα `ex3` και ένα νέο αρχείο με το όνομα `ex3.html`.

2) Πληκτρολογούμε τα παρακάτω αναγκαία tags:
```HTML
<!DOCTYPE html>
<html>
    <head>
      
    </head>
    <body>
        
    </body>
</html> 
```

3) Βάζουμε τίτλο στη σελίδα μας:
```HTML
<title>Exercise 3 - JS</title>
```

4) Στη συνέχεια μέσα στο `body` βάζουμε ένα κουμπί:
```HTML
<button id="myBTN" onclick="disableMe()">Push the Button!</button>
```

5) Έπειτα στο `head` γράφουμε το εξής script:
```HTML
<script>
  function disableMe() {
    document.getElementById("myBTN").disabled = true;
  }
</script>
```

6) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε τη σελίδα.

7) Πατάμε το κουμπί και παρατηρούμε ότι απενεργοποιείται!
