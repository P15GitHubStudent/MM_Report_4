# MM_Report_4
# Μάθημα: Πολυμέσα

## Εισαγωγή
Σε αυτήν την εργασία ανέλαβα την επέκταση, τροποποίηση του Super Mario. Ο κώδικας μου είχε ως βάση  (https://github.com/ioniodi/Super-Mario) οι αλλαγές που εκανα βασίζονται στα παραδοτεά που περιγράφονται αναλυτικά στο link αυτό https://courses-ionio.github.io/projects/super-mario/

## Επιλογή Εργαλείων
 1. IDE: Visual Studio Code
 2. Γλώσσα προγραμματισμού: Javascript
 3. Βιβλιοθήκη Phaser
 4. Αλλό λογισμικό: Tiled(δημιουργία πίστων)
 
 ## Πίστες
   1. Προσθήκη Πίστας
    * Πρώτη Πίστα
   ![super_mario_map1](https://user-images.githubusercontent.com/22703561/34296978-0ad9a6f4-e71e-11e7-9a63-9ed1eadeaac9.png).
   *  Δεύτερη Πίστα
   ![super_mario_map2](https://user-images.githubusercontent.com/22703561/34296979-0af81f08-e71e-11e7-801b-2e414837bc72.png).
   2. Προσθήκη μουσικής για την πίστα.
  
  ## Ηρωας
   1. Αλλαξα την εμφάνιση του παίκτη μου με το παρακάτω spriteSheet * ![playerpurple](https://user-images.githubusercontent.com/22703561/34297275-e5f86292-e71f-11e7-9fdb-a67157174a6a.png).
   2. Προσθήκη ηχων για τον παίκτη . Οταν παίρνει κέρμα,αλμα,χτυπήσει goomba στο κεφάλι.
   3. Ο πάικτης ξεκινάει με 5 καρδίες και μπορεί να πάρει το πολλύ 7.
   ![lives] (https://userimages.githubusercontent.com/22703561/34297992-00dc1af0-e724-11e7-907a-b1d6cec3e449.png) 
   4. κάθε φορά που ο παίκτης χάζει ζωή γίνεται επανεκκίνηση της πίστας. Αμα χάσει ολες του τις ζωές τότε ο πάικτης μεταβαίνει στην       οθόνη του gameOver.
  
    
 ## Εχθροί 
   1. Συμπεριφορά  κινούνται προς τα συνέχεια προς τα αριστερά, Οταν ακουμπήσουν τον παίκτη του αφαιρούνε μια ζωή, αμα ακουμπήσει κάποιο     * εμπόδιο το οποίο μπορεί να είναι είτε εμπόδιο κάποιος σωλήνας , είτε αόρατο εμπόδιο που τοποθετείται για να μην επιτρέψει το goomba να μην μπορεί να φύγει απο κάποιο σημείο π.χ κάποιο υψος.Το spriteSheet goomba ![goomba](https://user-images.githubusercontent.com/22703561/34297403-a57c2446-e720-11e7-8d98-dfd4084d4c4d.png).
   2. φάντασμα το οποίο αιωρείται και κινείται τυχαία στον χώρο,περνάει μέσα απο τους τοίχους,οταν ο παίκτης φτάσει κοντά στο φάντασμα
τότε τον ακολουθεί.Σε αντίθεση με τους αλλους εχθρούς το φάντασμα σκοτώνεται μόνο οταν συγκουστεί με τον παίκτη μας
* spritesheet ghost: ![ghost](https://user-images.githubusercontent.com/22703561/33543170-b28062d8-d8de-11e7-8ab2-6bd75f76db15.png)

3. Piranha Plant το οποίο κρύβεται στον σωλήνα μετά απο κάποια δευτερόλεπτα εμφανίζεται το φυτό δεν σκοτώνεται ούτε και να το 
χτυπήσεις στο κεφάλι ούτε με φωτιά.ο παίκτης χάνει ζωή αμα πέσει πάνω του.
 * spritsheet pirana:![piranaplant](https://user-images.githubusercontent.com/22703561/33653633-53b103cc-da76-11e7-8cb3-b9ae8b4009f9.gif)![pipe](https://user-images.githubusercontent.com/22703561/34297761-b992ad36-e722-11e7-90ca-b08e7fd00814.png)

4. Προειδοποιητική πινακίδα που ενημερώνει οτι σε αυτόν τον σωλήνα κρύβεται piranha φυτό  
![plantwarning](https://user-images.githubusercontent.com/22703561/33543562-2bd6ff10-d8e0-11e7-8684-dbdc5f940555.png)


## Κέρματα
 Αλλαγή εμφάνισης κερμάτων ![full coins](https://user-images.githubusercontent.com/22703561/34297993-03562816-e724-11e7-9fc9-1e09f8cb1e28.png).
 

 ## Bonus 
 * Προσθήκη QuestionBox το οποίο αμα το χτύπησει ο παίτης απο την κάτω μεριά βγαίνει μανιταρι το οποίο δίνει μια ζωή στον παίκτη και του αυξάνει το score
![questionblock-0](https://user-images.githubusercontent.com/22703561/33657111-ec4129e6-da80-11e7-8dc8-31c2b29d66b0.png)
![1upmushroom](https://user-images.githubusercontent.com/22703561/33657176-1fcac4de-da81-11e7-9c6f-14de0a84a6f6.png).
* οταν χτυπάς goomba στο κεφάλι τότε διπλασιάζει το score του παίκτη.
* τοποθέτηση fire sprite αντικειμένου σε διάφορα σημεία της πίστας οταν ο παίκτης το πάρει τοτε θα μπορεί να ρίχνει 
  φωτιές απο τα χέρια του για ενα σύντομο χρονικό διάστημα.Οι οπόιες μπορούν να σκοτώνουν τους εχθρούς αλλα καταστρέφονται οταν χτυπούν   σε σημεία της πίστας π.χ σωλήνες.![fire](https://user-images.githubusercontent.com/22703561/34299486-df8b5958-e72b-11e7-9193-170067770281.png)



## HUD
ο αριθμός δίπλα στο κέρμα υποδηλώνει το τρέχων score του παίκτη. Οι καρδίες που δεν εχουν κόκκινο χρώμα υποδηώνουν οτι ο παίκτης δεν εχει αυτή την ζωή.
* Προσθήκη ![hud](https://user-images.githubusercontent.com/22703561/34298340-fbec0ba2-e725-11e7-83fd-aa39ecdf6e39.png)


## Menu
 ![menu1](https://user-images.githubusercontent.com/22703561/33543806-158f0d50-d8e1-11e7-95f7-c81dfc3aebf2.png)
  * 1)Προσθήκη μενού στην αρχή του παιχνιδιού(Σημείωση η επιλογή help δεν είναι διαθέσιμη για αυτό το παραδοτεό)
 
 ![lvlselection](https://user-images.githubusercontent.com/22703561/33653702-8cfeff26-da76-11e7-870d-d1043b096394.png)
 * 2)Μενου επιλογής πίστας,τα αστεράκια υποδηλώνουν την δυσκολία τις πίστας μας και το λουκέτο δείχνει οτι είναι κλειδωμένη
 (Σημείωση οι κλειδωμένες πίστες δεν είναι διαθέσιμες για αυτό το παραδοτέο).Επίσης το κουμπί go_back πηγαίνει τον πάικτη μας πίσω
 
 
  ## Τηλεμεταφορά
  Τηλεμεταφορά του παίκτη μας
  γίνεται με βάσει τους σωλήνες,ο παίκτης μας τηλεμεταφέρεται σε σημεία τα οποία τα οποία των βοηθούν να πάρει περισσότερα κέρματα και 
  δεν τον βοηθάει να να τερματίσει την πίστα νωρίτερα.Τελός η παρακάτω πινακίδα υποδηλώνει σε ποιους σωλήνες μπορούν να γίνουν teleports
 ![teleport](https://user-images.githubusercontent.com/22703561/33654964-65ce9958-da7a-11e7-88d6-b649580ba8fd.png)

   ## WonGame
  ![screenshot_1](https://user-images.githubusercontent.com/22703561/34299643-bc046b0e-e72c-11e7-8523-57882618a597.png)


  ## GameOver 
   
![screenshot_2](https://user-images.githubusercontent.com/22703561/34299726-2d9d6054-e72d-11e7-838b-fe1da1f1b0c4.png)

  ## End of game Animation
 με το πέρας τις πίστας εμφανίζεται η πριγκίπισσα η οποία χαιρέτα τον ηρωά μας πλησιάζει προς το μέρος του το δίνει φιλάκι και κάνει fade την καμερά μας 
 ![princess](https://user-images.githubusercontent.com/22703561/33654872-26172d5c-da7a-11e7-873c-f57c60ca5508.png)


## link αποθετηρίου κωδικα
https://github.com/P15GitHubStudent/Super-Mario/tree/Par3
## link demo παιχνιδιού
https://p15githubstudent.github.io/Super-Mario






## Links πολυμεσικού περιεχομένου 
https://opengameart.org/content/kenney-16x16
https://scratch.mit.edu/projects/49905542/
http://www.nesmaps.com/maps/SuperMarioBrothers/sprites/SuperMarioBrothersSprites.html
https://www.spriters-resource.com/snes/smarioworld/sheet/52777/
