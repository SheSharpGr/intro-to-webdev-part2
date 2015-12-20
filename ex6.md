# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 6η

Σε αυτήν την άσκηση θα χρησιμοποιήσουμε τη σελίδα από το προηγούμενο workshop για να δημιουργήσουμε μια αντίστροφη μέτρηση για τα Χριστούγεννα!

1) Κατεβάζουμε το αρχείο [`SheSharp_Demo.zip`](https://github.com/SheSharpGr/intro-to-webdev-part2/blob/master/resources/SheSharp_Demo.zip?raw=true).

2) Αποσυμπιέζουμε το φάκελο, προτιμότερα στην `Επιφάνεια Εργασίας`.

3) Ανοίγουμε με τον editor της επιλογής μας το αρχείο `index.html` που βρίσκεται μέσα στο φάκελο `SheSharp_Demo`

4) Προσθέτουμε στο `<nav class="clear">` άλλο ένα `<li>` με τη σελίδα που θα φτιάξουμε για την αντίστροφη μέτρηση:
```HTML
<li><a href="countdown.html">Countdown</a></li>
```

5) Κάνουμε αποθήκευση του αρχείου `index.html` και φτιάχνουμε ένα νέο αρχείο με το όνομα `countdown.html` στον ίδιο φάκελο με το πρώτο.

6) Στο αρχείο αυτό (`countdown.html`) προσθέτουμε αρχικά τον εξής κώδικα:
```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
        <title>SheSharp demo</title>
        <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,400italic' rel='stylesheet' type='text/css'>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
        <link rel="stylesheet" type="text/css" href="styles.css" />
        <link href="img/fav.png" type='image/x-icon' rel='shortcut icon' />
    </head>

    <body>
    	<section id="page"> <!-- Defining the #page section with the section tag -->
        <header> <!-- Defining the header section of the page with the appropriate tag -->
          <hgroup>
            <h1>SHE<span class="h1_2">SHARP</span></h1>
            <h3>#include women</h3>
          </hgroup>
          <nav class="clear"> <!-- The nav link semantically marks your main site navigation -->
            <ul>
              <li><a href="index.html">Home</a></li>
              <li><a href="#article2">About</a></li>
              <li><a href="#article3">Contact</a></li>
              <li><a href="countdown.html">Countdown</a></li>
            </ul>
          </nav>
        </header>

        <!-- Εδώ θα μπεί το section για το countdown! -->

        <footer> <!-- Marking the footer section -->
          <div class="line"></div>
            <a href="#" class="up">Top</a>
            <a href="https://www.facebook.com/shesharpgr" class="fb"><i class="fa fa-facebook"></i></a>
            <a href="https://twitter.com/SheSharpGr" class="tw"><i class="fa fa-twitter"></i></a>
        </footer>
        </section> <!-- Closing the #page section -->

        <!-- JavaScript Includes -->
      </body>
</html>
```

7) Στη συνέχεια ανάμεσα στο `</header>` και το `<footer>` προσθέτουμε το section για την ένδειξη της αντίστροφης μέτρησης:
```HTML
<section id="xmasCountdown">
  <h2>Christmas Countdown</h2>
  <h2 id="timeLeft">?</h2>
</section>
```

8) Κάνουμε λίγο styling γα το section στο `head`:
```HTML
<style>
  section#xmasCountdown {
  margin: 25px auto;
  width: 900px;
  text-align: center;
}
  .notPink {
    color: #ff6b6b;
}
</style>
```

9) Προσθέτουμε ένα εξωτερικό link για το κώδικα της αντίστροφης χρονομέτρησης στο `head`:
```HTML
<script type="text/javascript" src="xmasscript.js"></script>
```

10) Αποθηκεύουμε τις αλλαγές μας αρχείο `countdown.html`.

11) Δημιουργούμε ένα νέο αρχείο με όνομα `xmasscript.js` στον ίδιο φάκελο.

12) Προσθέτουμε τον εξής κώδικα στο αρχείο `xmasscript.js`:
```JS
var xmassDate = setInterval(function(){isItXmass(new Date("December 25, 2015 00:00:00"),"timeLeft")}, 1000);

function isItXmass(examDate,timeID){	
  examDate-=new Date();
	writeDate(examDate,timeID);			
}

function writeDate(countDown, timeID){
	if (countDown <= 0){				
		document.getElementById(timeID).innerHTML="Christmas is Over :/";
		clearTheInterval(timeID);	
	}
	else{
		countDown=countDown/1000;
		seconds=countDown%60;
		countDown=countDown/60;
		minutes=countDown%60;
		countDown=countDown/60;
		hours=countDown%24;
		days=countDown/24;
		document.getElementById(timeID).innerHTML=parseInt(days)+"<span class='notPink'>days</span> " +parseInt(hours)+"<span class='notPink'>hours</span> " +parseInt(minutes)+"<span class='notPink'>minutes</span> "+ parseInt(seconds)+"<span class='notPink'>seconds</span> ";
	}
}
```

13) Αποθηκεύουμε τις αλλαγές μαςστο αρχείο `xmasscript.js` και επιστρέφουμε στο `countdown.html`

14) Μένει να βάλουμε μια εικόνα! Κατεβάζουμε αυτήν [εδώ](https://raw.githubusercontent.com/SheSharpGr/intro-to-webdev-part2/master/resources/xmasslogo.png) και την αποθηκεύουμε μέσα στο φάκελο `img` του `SheSharp_Demo`.

15) Προσθέτουμε τον εξής κώδικα κάτω από την αντίστροφη μέτρηση!
```HTML
<img src="img/xmasslogo.png" alt="SheSharp Logo - Xmass Edition" />
```

16) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε το αρχείο!
