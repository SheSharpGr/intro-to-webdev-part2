# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 2η


Σε αυτή την άσκηση θα δούμε μια εντολή JavaScript που επηρεάζει το περιεχόμενο της σελίδας και θα διαπιστώσουμε πως έχει σημασία η σειρά του που μπαίνει ο κώδικας.

#### Κομμάτι Α - script στο head
1) Δημιουργούμε έναν φάκελο στην επιφάνεια εργασίας με το όνομα `ex2`

2) Ανοίγουμε ένα νέο αρχείο στον editor και κάνουμε αντιγραφή/επικόλληση το παρακάτω κώδικα:
```HTML
<!DOCTYPE html>
<html>
<head>
	<title>Intro to Web Dev</title>
	<link href='https://fonts.googleapis.com/css?family=Ubuntu|Lobster&subset=latin,greek' rel='stylesheet' type='text/css'>
	<link rel="stylesheet" type="text/css" href="myStyle.css" />	
	<!-- Εδώ θα μπεί το νέο μας style -->
	
</head>
<body>
	<header>
		<hgroup>
			<h1>Introduction to Web Development</h1>
			<h3>Don't Just Browse, Create!</h3>
		</hgroup>
	</header>
	
	<!-- Εδώ θα μπεί το νέο section -->
	
	<footer>
		<p>&copy 2015</p>
	</footer>     
</body>
</html> 
```

3) Αποθηκεύουμε το αρχείο μας μέσα στο φάκελο `ex2` με το όνομα `example2a.html`.

4) Δημιουργούμε ένα νέο αρχείο στο φάκελο `ex2` με το όνομα myStyle.css, κάνουμε επικόλληση το παρακάτω κώδικα σε αυτό και αποθηκεύουμε τις αλλαγές:
```CSS
body {
	margin:0;
	padding: 0;
	background-color: #556270;
	color: white;
	font-family: 'Ubuntu', sans-serif;
}

header {
	margin: 0 auto;
	text-align: center;
	width: 500px;
}

header h1 {
	font-family: 'Lobster', cursive;
	margin-bottom: 5px;
	color: #4ecdc4;
}

header h3 {
	text-align: left;
	margin: 0 0 10px 20px;
	color: white;
}

section {
	width: 60%;
}

footer {
	text-align: center;
}
```

5) Επιστρέφουμε στο αρχείο `example2a.html` και δημιουργούμε ένα νέο section ανάμεσα στο `header` και το `footer`. Αποθηκεύουμε τις αλλαγές μας:
```HTML
<section id="main">
		<p id="hideandseek">Now You See Me.</p>
</section>
```

5) Μορφοποιούμε το section που προσθέσαμε παραπάνω με ένα `style` στο `head`:
```HTML
<style>
	#main {
		text-align: center;
		margin: 20px auto;
	}
</style>
```

6) Κάτω από το `style` στο `head` τοποθετώ τον εξής κώδικα:
```HTML
<script>
	document.getElementById("hideandseek").innerHTML="Now You Don't!"
</script>
```

7) Αποθηκεύουμε τις αλλαγές μας και τρέχουμε τη σελίδα. Παρατηρούμε ποιο κομμάτι φαίνεται στη σελίδα (`Now You See Me.` ή `Now You Don't`;)

#### Κομμάτι B - script στο body
1) Κάνουμε Αποθήκευση Ως το αρχείο στον ίδιο φάκελο `ex2` με το όνομα `example2b.html`

2) Κάνουμε αποκοπή (`Ctrl + X`) το κομμάτι:
```HTML
<script>
		document.getElementById("hideandseek").innerHTML="Now You Don't!"
</script>
```

3) Κάνουμε επικόλληση το κώδικα κάτω από το footer.

4) Αποθηκεύουμε τις αλλαγές μας στο `example2b.html` και τρέχουμε τη σελίδα.

5) Ξανα-εξετάζουμε το κομμάτι που φαίνεται στη σελίδα (`Now You See Me.` ή `Now You Don't`;)

#### Κομμάτι Γ - εξωτερικό link
1) Κάνουμε Αποθήκευση Ως το αρχείο στον ίδιο φάκελο `ex2` με το όνομα `example2c.html`

2) Κάνουμε αποκοπή (`Ctrl + X`) το κομμάτι:
```HTML
<script>
		document.getElementById("hideandseek").innerHTML="Now You Don't!"
</script>
```

3) Προσθέτουμε το παρακάτω στο `head`:
```HTML
<script type="text/javascript" src="script.js"></script>
```

3) Αποθηκεύουμε τις αλλαγές μας στο `example2c.html`

4) Δημιουργούμε ένα νέο αρχείο με το όνομα `script.js` και το αποθηκεύουμε στον ίδιο φάκελο `ex2`.

5) Μέσα στο αρχείο `script.js` κάνουμε επικόλληση και διαγράφουμε τα tags `<script>` και `</script>`.

5) Τρέχουμε τη σελίδα `example2c.html`. Ποιο κομμάτι δείχνει;