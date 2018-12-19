# Όνομα μαθήματος : Επικοινωνία Ανθρώπου-Υπολογιστή
## Όνομα : Αντωνία Σμυρλιάδη
## Αριθμός Μητρώου: Π2017130

## Σύνοψη

Η παρούσα αναφορά πραγματεύεται την υλοποίηση δύο επιμέρους εργασίες που διαθέτουν από δύο παραδοτέα αντίστοιχα στο μάθημα Επικοινωνία Ανθρώπου-Υπολιστή του Γ'εξαμήνου. Παρακάτω αναλύονται τα δεδομένα, τα αποτελέσματα και τα συμπεράσματα αυτών των εργασιών.

##  Σύντομη εισαγωγή

Από τις διαθέσιμες εργασίες που διαθέτει το μάθημα ολοκλήρωσα επιτυχώς και τα δύο παραδοτέα της Εργασίας Περιεχομένου, όλα τα ζητούμενα από το πρώτο παραδοτέο της Εργασίας Ανάπτυξης καθώς επίσης και το πρώτο ζητούμενο από το δεύτερο παραδοτέο. Ακολουθεί η ανάλυση της υλοποίησης των ζητούμενων των παραδοτέων των εργασιών.


# Όνομα εργασίας : Εργασία Ανάπτυξης 

* [Eκτελέσιμο link](https://p17smyr.github.io/D3js-US-educational-attainment/)

* [Link αποθετηρίου](https://github.com/p17smyr/D3js-US-educational-attainment)
 
### Ζητούμενα - Παραδοτέο 1
 - [x] Άλλαξα τα χρώματα στα 3 γραφήματα.
 - [x] Αντικατέστησα τις διεπαφές στα "κουμπιά" του 2ου και 3ου γραφήματος.
 - [x] Όταν το ποντίκι διέρχεται επάνω από κάθε επιλογή του menu στην κορυφή της σελίδας, ακούγεται κάποιος ήχος.
 - [x] Όταν το ποντίκι διέρχεται πάνω από κάποια πρόταση/κείμενο της σελίδας ή περιοχή που περιλαμβάνει γραπτή πληροφορία (π.χ. κάποιο τμήμα γραφήματος), ακούγεται αυτόματα η αφήγηση του κειμένου (text-to-speech).
 - [x] Εφάρμοσα responsive design στη σελίδα (Bootstrap) και κυρίως στο αρχικό menu έτσι ώστε να προσαρμόζεται σε οθόνες διαφορετικών διαστάσεων.

A. Η αλλαγή των χρωμάτων (σε δεκαεξαδική μορφή) αλλάχθηκε από το αντίστοιχο αρχείο script.js.

Γράφημα 1: ...var colour = d3.scaleOrdinal().range...

Γράφημα 2: ...var color = d3.scaleLinear().domain...

Γράφημα 3: ...var colors = d3.scaleOrdinal() .range...

![ScreenShot](1.JPG)

B. Η αλλαγή των ετικετών στα κουμπιά διεπαφής πραγματοποιήθηκε από το αρχείο style.css.

....radio-toolbar label { ...

....radio-toolbar input[type="radio"]:checked+label { ...

![ScreenShot](2.JPG)

Γ. Για τον ήχο που κάνει το ποντίκι όταν διέρχεται πάνω από το μενού αρχικά κατέβασα ένα αρχείο .mp3 από το http://soundbible.com/tags-click.html κι έπειτα το έκανα online convert σε .ogg. Στη συνέχεια έκανα upload στο αποθετήριο της εργασίας όπως και το αρχείο sound-mouseover.js κι έκανα τις απαραίτητες αλλαγές στο αρχείο index.

...href="#top" onmouseover="playclip();" >Top</a></li> ...

Επιπλέον πρόσθεσα και το </script> <audio>

...source src="Click.mp3">...

Δ. Το 4ο ζητούμενο πραγματοποιήθηκε με τη βοήθεια του onmouseover="responsiveVoice.speak και onmouseleave="responsiveVoice.cancel() σε κάθε σημείο του αρχείου που θέλαμε να ακολουθεί την οδηγία text-to-speech.

![ScreenShot](3.JPG)

Ε. Για το 5ο ζητούμενο έγιναν οι απαραίτητες αλλαγές στο index αρχείο ώστα να προσαρμόζεται το εκτελέσιμο αρχείο στα διάφορα μεγέθη οθονών.

...<script src="https://stackpath.bootstrapcdn.com/bootstrap...

### Ζητούμενα - Παραδοτέο 2

- [x] Τροποποιήστε τον κώδικα και το μενού της εφαρμογής έτσι ώστε κάθε στιγμή να είναι εμφανές μόνο ένα από τα 3 γραφήματα, παραμένοντας πάντα στη σελίδα index.html.   
- [ ] Αντικαταστήστε το κάθε ένα από τα 3 γραφήματα με κάποιο άλλο διαδραστικό γράφημα της D3js.

- [ ] Σε μια καινούργια σελίδα, να τοποθετήσετε αντίστοιχα 3 νέα διαδραστικά γραφήματα D3js της επιλογής σας, τα οποία θα οπτικοποιούν καινούργια στατιστικά δεδομένα που θα βρείτε από κάποια επίσημη στατιστική αρχή (π.χ. ΕΛΣΤΑΤ, Eurostat κ.λπ.).

Α. H εμφάνιση και αντίστοιχα η απόκρυψη του κάθε γραφήματος έγινε μέσω της προσθηκης του συνάρτησης showhide η οποία εντάχθηκε στο index.html αρχείο.

![ScreenShot](hide.JPG)

Η συνάρτηση αυτή καλείται πριν από κάθε διάγραμμα αλλά και στο μενού επιλογών ώστε πατώντας μία προς μία κάθε επιλογή (εκτός του Top) να εμφανίζεται το κάθε διάγραμμα αλλά να συνοδεύεται και με τον ήχο των επιλογών.

![ScreenShot](menu.JPG)


# Όνομα εργασίας : Εργασία Περιεχομένου
* [Eκτελέσιμο link](https://p17smyr.github.io/gr/)


* [Link αποθετηρίου](https://github.com/p17smyr/gr)

### A: Τα links των εικόνων
* [atari](https://p17smyr.github.io/gr/gallery/atari/)
  
* [multi_tuch](https://p17smyr.github.io/gr/gallery/multi_touch)
  
* [lego_turing_mashine](https://p17smyr.github.io/gr/gallery/lego_turing_mashine/)
  
* [fingerprint_reader](https://p17smyr.github.io/gr/gallery/fingerprint_reader/)
  
* [turing_test](https://p17smyr.github.io/gr/gallery/turing_test/)
  
### Β: Τα links των διαδραστικών παραδειγμάτων
* [Button Design](https://p17smyr.github.io/gr/remix/button-design-years/)
  
* [Timer](https://p17smyr.github.io/gr/remix/timer/)


## Τελική Αναφορά  
* [Eκτελέσιμο link](https://p17smyr.github.io/FINAL-REPORT/)


* [Link αποθετηρίου](https://github.com/p17smyr/FINAL-REPORT)


## Συμπεράσματα

Εν κατακλείδι, με το πέρας των παραδοτέων έγινε σαφές ότι το περιβάλλον του Github είναι πολύπλευρο και με πολλές δυνατότητες για νέους αλλά και έμπειρους προγραμματιστές. Είναι απαραίτητη η συνεχόμενη εξάσκηση με τη πλατφόρμα μιας και είναι μεγάλος ο όγκος πληροφοριών που δέχεται ο χρήστης από αυτήν. Μέσα από τη παρούσα εργασία έγινε η γνωριμία με νέες γλώσσες προγραμματισμού όπως η Javascript, η HTML, και η CSS. 

## Αναφορές

* [responsive voice](https://responsivevoice.org/)
* [Stack Over Flow](https://stackoverflow.com/)
* [d3 github](https://github.com/d3/d3/wiki/Gallery)
* [Google Chart](https://developers.google.com/chart/interactive/docs/gallery)









