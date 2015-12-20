# Introduction to Web Development
## Part 2: JavaScript
### Άσκηση 1η

Στόχος αυτής της άσκησης είναι η επανάληψη όλων όσων μάθαμε στο πρώτο κομμάτι από HTML και CSS.

#### Content
1) Ανοίγουμε τον editor της επιλογής μας (Notepad, Notepad++, Sublime, Atom, κτλ).

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
3) Στη συνέχεια προσθέτουμε τον τίτλο της σελίδας μέσα στο `<head>`:
```HTML
	<title>Intro to Web Dev</title>
```

4) Αρχικά θα δημιουργήσουμε τη κεφαλίδα της σελίδας τοποθετώντας τον παρακάτω κώδικα μέσα στο `<body>`:
```HTML
<header>
	<hgroup>
		<h1>Introduction to Web Development</h1>
		<h3>Don't Just Browse, Create!</h3>
	</hgroup>
</header>
```

 5) Έπειτα θα προσθέσουμε μια περιγραφή της σελίδας μας:
 ```HTML
 <section id="description">
	<p>This is a series of web development workshops aimed for anyone who wants to learn how to build websites.</p>
	<p>We will start with the basics of frontend development, then we'll introduce some very usefull frameworks and tools and in the end we'll work on some backend development</p>
	<p>Hope you're as excited, as we are!</p>
</section>
 ```
 
 6) Προσθέτουμε ένα νέο `<section>` για τα άρθρα μας:
 ```HTML
 <section id="articles">
 
 </section> 
 ```
 
 7) Μέσα στο `<section id="articles">`, προσθέτουμε τα εξής δύο άρθρα:
 ```HTML
<article id="article2">
	<header class="articleHeader">
		<h2>Part 2<sup>nd</sup>: Javascript</h2>
	</header>
	<p>
		Time to learn something more interactive!
	</p>
	<p id="postedOn">
		Posted on <time datetime="2015-12-20 15:59">December 20</time> by Annie.
	</p> 
</article> 

<article id="article1">
	<header class="articleHeader">
		<h2>Part 1<sup>st</sup>: HTML/CSS</h2>
	</header>
	<p>
		Beginners you don't need to have any programming skills or familiarity with HTML, JavaScript, JQuery, etc.
	</p>
	<p>
		You are going to learn to understand HTML and JavaScript code not as a web developer.
	</p>
	<p>
		We are -hopefully- going to motivate you to engage more with Web technologies, accessibility, design, and coding in general!
	</p>
	<p id="postedOn">
		Posted on <time datetime="2015-12-12 21:00">December 12</time> by Katerina.
	</p>        
</article>   
```

8) Κλείνουμε τη σελίδα με ένα `<footer>`:
```HTML
<footer>
	<p>&copy 2015<p>
</footer>  
```

9) Αποθηκεύουμε το αρχείο μας με το όνομα `index.html` σε ένα φάκελο με το όνομα exercise1 στην επιφάνεια εργασίας.


#### Styling
1) Τοποθετούμε στο αρχειο `index.html`, μέσα στο `<head>` κάτω από το `<title>` τις παρακάτω συνδέσεις (η πρώτη είναι για εισαγωγή γραμματοσειρών και η δεύτερη για το CSS που θα φτιάξουμε):
```HTML
<link href='https://fonts.googleapis.com/css?family=Ubuntu|Lobster&subset=latin,greek' rel='stylesheet' type='text/css'>
<link rel="stylesheet" type="text/css" href="myStyle.css" />
```

2) Δημιουργούμε το αρχείο `myStyle.css` μέσα στο φάκελο exercise1.

3) Αρχικά κάνουμε αλλαγές στο `body`:
```CSS
body {
	margin:0;
	padding: 0;
	background-color: #556270;
	color: white;
	font-family: 'Ubuntu', sans-serif;
}
```

4) Στη συνέχεια διαμορφώνουμε τη κεφαλίδα της σελίδας μας:
```CSS
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
```

5) Μετά έχουν σειρά τα `section`:
```CSS
section {
	width: 60%;
}

section#description {
	margin: 15px auto;
}

section#articles {
	margin: 20px auto;
}
```

6) Στη συνέχεια φροντίζουμε έτσι ώστε να μπαίνουν οι ημερομηνίες των άρθρων στα δεξιά:
```CSS
.postedOn {
	text-align: right;
}
```

7) Αλλάζουμε το χρώμα και τη γραμματοσειρά στους τίτλους των άρθρων:
```CSS
article header h2 {
	color: #c7f464;
	font-family: 'Lobster', cursive;
}
```

8) Κεντράρουμε το `footer`:
```CSS
footer {
	text-align: center;
}
```
