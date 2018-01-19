# Αναφορά
# Μάθημα: Πολυμέσα

## Εισαγωγή
Στα πλαίσια του μαθήματος πολυμέσα του Έ εξαμήνου επέλεξα την τροποποίηση , την προσθήκη νέων δυνατοτήτων στο παιχνιδι Super Mario link αποθετηριού κώδικα :https://github.com/ioniodi/Super-Mario, Link παραδοτέων: https://github.com/courses-ionio/projects/blob/master/super-mario/index.md

##  Σύνοψη
Υλοποίησα όλα τα ζητούμενα και των τεσσάρων παραδοτέων. Επίσης έδωσα  την δυνατότητα στον παίκτη να μπορεί να ρίχνει φωτιές από τα χέρια του για  ένα  περιορισμένο χρονικό διάστημα όταν πάρει ένα sprite φωτιάς το οποίο περιστρέφεται στην πίστα. Επίσης έγινε προσθήκη βοηθητικών πινακίδων(αναλύονται στην συνέχεια).

## Διαδικάσια ανάπτυξης
Διαδικασία ανάπτυξης Για την συγγραφή και την εκτέλεση του κώδικα έγινε χρήση ενός τοπικού ide(visual studio code) έναντι της online πλατφόρμας του github. Στην συνέχεια βρήκα το πολυμεσικό περιεχόμενο που θα ή να ήθελα να προσθέσω στο παιχνίδι τα links  (παραθέονται  στο τέλος της αναφοράς)που χρησιμοποίησα. Για την υλοποίηση κάθε παραδοτέου αρχικά σχεδίασα σε ένα φύλλο χαρτί το πώς θα ήθελα να είναι το επιθυμητό αποτέλεσμα  , μετά υλοποίησα τον κώδικα . Όσο αφορά το προγραμματιστικό κομμάτι  πολλές φορές αντιμετώπισα προβλήματα  λογικής και συντακτικής φύσεως για την αντιμετώπιση των προβλημάτων προέβηκα στις ακόλουθες ενέργειες. Αρχικά υλοποίησα λειτουργεία προγραμματιστή για να μπορέσω να δοκιμάζω την πίστα μου  , ακόμα Ιστοσελίδες που με βοήθησαν σε αρκετό βαθμό για την αντιμετώπιση σφαλμάτων αποτέλεσαι 
 1. https://www.google.com/ 
 2. https://stackoverflow.com/ 
 3. https://phaser.io/ 
 4. http://www.html5gamedevs.com/




## Επιλογή Εργαλείων
 1. IDE: Visual Studio Code
 2. Γλώσσα προγραμματισμού: Javascript
 3. Βιβλιοθήκη Phaser
 4. Αλλό λογισμικό: Tiled(δημιουργία πιστών)
 
## States 
Καταστάσεις στις οποίες μπορεί να μεταβεί το παιχνίδι μας, οι καταστάσεις αυτές είναι
1. preload state : Αναλαμβάνει να φορτώσει τους πόρους για εμάς οπως εικόνες,spritesheets,ηχους  παράλληλα δείχνει loading bar υποδηλώνοντας οτι φορτώνει πόρους, endofgameAnimation.
2. MenuState: οθόνη του αρχικού μενού.
3. SelectMapState: κατάσταση υπεύθυνση για την επιλογή της πίστας.
4. PlayState: δημιουργεί Πίστες και τοποθετεί σε αυτήν κερματα,Bonus,HUD,τον ηρωα μας ,εχθρύς, και αόρατα sprites που αμα πατήσεις πάνω τους σε σωλήνες μπορείς να τηλεμεταφερφείς.
5. WonGameState: μετάβαση οταν ο παίκτης ολοκληρώση την τελευταία πίστα.
6. GameOverState: μετάβαση οταν ο παίκτης χάσει ολες τις ζωές του.
7. LoadNextLevelState : οταν ολοκληρωθεί μια πίστα αναλαμβάνει την φόρτωση της επόμενης.

## PlayState

### Πίστες
1. Δημιουργία δύο πιστών
![super_mario_map1](https://user-images.githubusercontent.com/22703561/34296978-0ad9a6f4-e71e-11e7-9a63-9ed1eadeaac9.png).
![super_mario_map2](https://user-images.githubusercontent.com/22703561/34296979-0af81f08-e71e-11e7-801b-2e414837bc72.png).
  Στις πίστες αυτές εγινε προσθήκη  layers Pipes,invisibleWalls,teleport,endOfLevel. Το πρώτο layer χρησιμοποίηθηκε ως layer για να   κρύψουμε το φυτό piranhas στον σωλήνα. InvisibleWalls εκει τοποθετούμε αόρατα αντικείμενα για να καταλαβαίνουν οι εχθροί οτι σε αυτό το σημείο θα πρέπει να αντιστρέψουν  τη φορά του διανύσματος της ταχύτητας τους. Teleport layer για να καταλαβαίνει σε ποια σημεία μπορεί να κάνει τηλεμεταφορά ο παίκτης. Τέλος εγινε προσθήκη μουσικής.
   
### Ηρωας
   1. Εγινε Αλλαγή στην εμφάνιση του παίκτη μας  ![playerpurple](https://user-images.githubusercontent.com/22703561/34297275-e5f86292-e71f-11e7-9fdb-a67157174a6a.png). Απο το Spritesheet αυτο χρησιμοποιήθηκαν frames για την κίνηση του παίκτη. προστέθηκαν 
   ηχοι οταν ο παίκτης μαζεύει κερματα,χτυπάει εχθρό τύπου goomba στο κεφάλι,κάνει αλματα. Η τηλεμεταφορά μπορεί να γίνει πάνω σε ειδικούς σωλήνες. 
   
## Πλήκτρα χειρισμού παίκτη
Τα control πλήκτρα του παίκτη είναι 
 ασιστερο,δεξιό βελάκι για την κίνηση προς την αριστερή και δεξία κατεύθυνση. Το πάνω βελάκι για αλμα το κάτω βελάκι για teleport σε ειδικούς σωλήνες. Τέλος το space για να ρίχνει φωτιές στην περίπτωση που έχει πάρει Bonus φωτίας.


### Εχθροί-Αντικείμενα
1. Συμπεριφορά  κινούνται συνέχεια προς τα αριστερά πρώτο frame, Οταν ακουμπήσουν τον παίκτη του αφαιρούνε μια ζωή, αμα ακουμπήσει κάποιο    εμπόδιο το οποίο μπορεί να είναι  κάποιος σωλήνας , είτε αόρατο αντικείμενο.Goomba σκοτώνεται μόνο αμα χτυπηθεί στο κεφάλι, η του ρίξουν φωτιά  τα δύο τελευταία frames του spritesheet  του χρησιμοποιούνται για να αναπαρασταση του κτυπημένου goomba το οποιο πέφτει κάτω απο την πλατφόρμα. 
Το spriteSheet goomba ![goomba](https://user-images.githubusercontent.com/22703561/34297403-a57c2446-e720-11e7-8d98-dfd4084d4c4d.png).
   2. φάντασμα το οποίο αιωρείται και κινείται τυχαία στον χώρο,περνάει μέσα απο τους τοίχους,οταν ο παίκτης φτάσει κοντά στο φάντασμα
τότε τον ακολουθεί.Σε αντίθεση με τους αλλους εχθρούς το φάντασμα σκοτώνεται μόνο οταν συγκουστεί με τον παίκτη μας Και το οποίο θα οδηγήσει επίσης τον παίκτη να χάσει μια ζωή για να αντιμετωπίσεις το φάντασμα πρέπει να αποφύγης να πας πολύ κοντά του η αμα πας αρκετά κοντά πρέπει να τρέξεις για να μην συγκρουστής μεταξύ του. 
 spritesheet ghost: ![ghost](https://user-images.githubusercontent.com/22703561/33543170-b28062d8-d8de-11e7-8ab2-6bd75f76db15.png)
 
3. Piranha Plant το οποίο κρύβεται στον σωλήνα μετά απο κάποια δευτερόλεπτα εμφανίζεται το φυτό δεν σκοτώνεται ούτε και να το 
χτυπήσεις στο κεφάλι ούτε με φωτιά.ο παίκτης χάνει ζωή αμα πέσει πάνω του. Καταληλη στιγμή για να το αποφύγεις είναι οταν μπεί στο 
σωλήνα , η οταν κατεβαίνει σιγα σιγά για να μπεί στον σωλήνα.
 sprietsheet pirana:![piranaplant](https://user-images.githubusercontent.com/22703561/33653633-53b103cc-da76-11e7-8cb3-b9ae8b4009f9.gif)![pipe](https://user-images.githubusercontent.com/22703561/34297761-b992ad36-e722-11e7-90ca-b08e7fd00814.png)
 
 
 
 

4. Προειδοποιητική πινακίδα που ενημερώνει οτι σε αυτόν τον σωλήνα βρίσκεται piranha φυτό  
![plantwarning](https://user-images.githubusercontent.com/22703561/33543562-2bd6ff10-d8e0-11e7-8684-dbdc5f940555.png)

### Κέρματα
 Αλλαγή εμφάνισης κερμάτων![full coins](https://user-images.githubusercontent.com/22703561/34297993-03562816-e724-11e7-9fc9-1e09f8cb1e28.png).
 
### Bonus-αντικείμενα
 * Προσθήκη QuestionBox το οποίο αμα το χτύπησει ο παίκτης απο την κάτω μεριά βγαίνει μανιτάρι το οποίο δίνει μια ζωή στον παίκτη και του αυξάνει το score
![questionblock-0](https://user-images.githubusercontent.com/22703561/33657111-ec4129e6-da80-11e7-8dc8-31c2b29d66b0.png)
![1upmushroom](https://user-images.githubusercontent.com/22703561/33657176-1fcac4de-da81-11e7-9c6f-14de0a84a6f6.png).
* οταν χτυπάς goomba στο κεφάλι τότε υπάρχει πιθανότητα διπλασιάσει το score του παίκτη.
* τοποθέτηση fire sprite αντικειμένου σε διάφορα σημεία της πίστας οταν ο παίκτης το πάρει τοτε θα μπορεί να ρίχνει 
  φωτιές απο τα χέρια του για ενα σύντομο χρονικό διάστημα.Οι οπόιες μπορούν να σκοτώνουν τους εχθρούς αλλα καταστρέφονται οταν χτυπούν   σε σημεία της πίστας π.χ σωλήνες.![fire](https://user-images.githubusercontent.com/22703561/34299486-df8b5958-e72b-11e7-9193-170067770281.png)
  
### HUD
ο αριθμός δίπλα στο κέρμα υποδηλώνει το τρέχων score του παίκτη. Οι καρδίες που δεν εχουν κόκκινο χρώμα υποδηώνουν οτι ο παίκτης δεν εχει αυτή την ζωή.Ο παίκτης ξεκινάει με πέντε καρδίες και έχει το πολλύ εφτά ζωές
* ![hud](https://user-images.githubusercontent.com/22703561/34298340-fbec0ba2-e725-11e7-83fd-aa39ecdf6e39.png)

### Τηλεμεταφορά
  Τηλεμεταφορά του παίκτη μας 
  γίνεται με βάσει τους σωλήνες,ο παίκτης μας τηλεμεταφέρεται σε σημεία τα οποία τα οποία των βοηθούν να πάρει περισσότερα κέρματα και 
  δεν τον βοηθάει να να τερματίσει την πίστα νωρίτερα.Τελός η παρακάτω πινακίδα υποδηλώνει σε ποιους σωλήνες μπορούν να γίνουν teleports
 ![teleport](https://user-images.githubusercontent.com/22703561/33654964-65ce9958-da7a-11e7-88d6-b649580ba8fd.png)
 ![teleportgif](https://user-images.githubusercontent.com/22703561/35149062-6bc4a634-fd1d-11e7-9f70-6807f8908982.gif)
 
### endofLevelAnimation
 με το πέρας τις πίστας ο παίκτης είναι αφθαρτος, παγωμένος(δεν μπορεί να κουνηθεί)εμφανίζεται η πριγκίπισσα  η οποία χαιρέτα τον ηρώα μας πλησιάζει προς το μέρος του το δίνει φιλάκι και κάνει fade την κάμερα μας και επιτρέπει την μετάβαση στο LoadNextLevelState.
 ![wongame](https://user-images.githubusercontent.com/22703561/35149198-de21ca86-fd1d-11e7-8e35-ff388284764d.gif)
 
 ![wongame](https://user-images.githubusercontent.com/22703561/35149198-de21ca86-fd1d-11e7-8e35-ff388284764d.gif)

### WonGame
   ![screenshot_2](https://user-images.githubusercontent.com/22703561/34299726-2d9d6054-e72d-11e7-838b-fe1da1f1b0c4.png)
   Οθόνη δείχνει το score που έκανε και του δίνει την δυνατότητα κάνοντας κλικ στο κουμπί να μεταβεί πίσω στο κύριο Menu.

### GameOver 
  Οθόνη όταν ο παίκτης έχασε όλες τις ζωές του ολοκλήρωση τις πίστας δείχνει το score που κατάφερε, επίσης δίνει την δυνατότητα στο άτομο αυτό να διαλέξει άμα θα ήθελε να μεταβεί στο κύριο μενού η 
  να κάνει επανεκκίνηση την τρέχουσα πίστα που δεν κατάφερε να ολοκληρώσει.
  ![screenshot_1](https://user-images.githubusercontent.com/22703561/34299643-bc046b0e-e72c-11e7-8523-57882618a597.png)


## LoadNextLevelState
Με το πέρας μια πίστας αναλαμβάνει να φορτώσει την επόμενη πίστα, όταν δεν θα υπάρξει επόμενη πίστα να φορτώσει τότε θα μεταβεί στο WonGame State.

## Menu
  * 1) Μενού έχει διαθέσιμα δυο κουμπιά το ένα είναι το mapstart το οποίο συνδέεται με την φόρτωση μιας τυχαίας πίστας από τις διαθέσιμες, δεύτερη επιλογή είναι το levelSelect το οποίο ξεκινάει το LevelSelectState. 
  
  ![playmap](https://user-images.githubusercontent.com/22703561/35149192-da9e709e-fd1d-11e7-91b8-db27bd28fc8f.gif)
  
## LevelSelect
 
 ![lvlselection](https://user-images.githubusercontent.com/22703561/33653702-8cfeff26-da76-11e7-870d-d1043b096394.png)
 * 2)Μενού επιλογής πίστας, τα αστεράκια υποδηλώνουν την δυσκολία τις πίστας μας ,το λουκέτο δείχνει ότι είναι κλειδωμένη
 (Σημείωση δεν έχει γίνει υλοποίηση περισσότερων από δυο πίστες). Τέλος το κουμπί go-back σηματοδοτεί την επιστροφή πίσω στη κατάσταση 
 του μενού.
 
 
## Συμπεράσματα 
Η παρών εργασία μου έδωσε την δυνατότητα να μάθω αρκετά πράγματα για την javascipt και την Phaser . Παρόλο που το τελικό αποτέλεσμα μπορεί να θέλει ακόμα αρκετή δουλεία, πιστεύω ότι έχω κάνει ένα καλό βήμα και ευελπιστώ να μάθω ακόμα περισσότερα.


## link αποθετηρίου κώδικα
https://github.com/P15GitHubStudent/Super-Mario/tree/master
## link demo παιχνιδιού
https://p15githubstudent.github.io/Super-Mario


## Links πολυμεσικού περιεχομένου 
https://opengameart.org/content/kenney-16x16
https://scratch.mit.edu/projects/49905542/
http://www.nesmaps.com/maps/SuperMarioBrothers/sprites/SuperMarioBrothersSprites.html
https://www.spriters-resource.com/snes/smarioworld/sheet/52777/
https://freesound.org/
