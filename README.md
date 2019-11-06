# Εργαστήριο μαθήματος Επικοινωνία Ανθρώπου-Υπολογιστή
---
Για την υλοποίηση των εργασιών του εργαστηρίου θα πρέπει να εργαστείτε σε ένα Unix/Linux terminal. Θα αξιοποιήσετε κάποιες από τις ήδη διαθέσιμες εντολές του shell, αλλά θα χρειαστεί να εγκαταστήσετε και κάποια νέα προγράμματα.

Για να εργαστείτε καθένας στο δικό του περιβάλλον εκτέλεσης, μπορείτε να αξιοποιήσετε όποια από τις πιο κάτω επιλογές σας εξυπηρετεί καλύτερα:
 * _Bring your own laptop:_ Ιδανικά με ήδη εγκατεστημένο linux, πχ ως dual boot
 * _Bring your own laptop:_ Εγκατάσταση ενός linux εντός virtual box
 * _Bring your own laptop:_ Αξιοποίηση Windows Linux Subsystem εφόσον το laptop σας τρέχει Win10
 * Χρήση _persistent live ubuntu usb_ (επιτρέπει την εκτέλεση XUbuntu Desktop περιβάλλοντος το οποίο διατηρεί τις αλλαγές που κάνετε, πχ εγκατάσταση προγραμμάτων)
   <!-- - Μπορείτε να κατεβάσετε ένα κατάλληλο `image` [εδώ](https://195.130.127.104/hci.xubuntu.iso)
     - Μεταφέρετε το image σε ένα usb stick τουλάχιστον 4GB
     - Κάντε boot από οποιοδήποτε desktop του εργαστηρίου
     - _Μετά την ολοκλήρωση της εγκατάστασης το flashάκι σας θα εμφανίζεται να έχει μέγεθος 4GB, χρησιμοποιήστε το [GParted](https://www.howtoforge.com/partitioning_with_gparted) για να δημιουργήσετε ένα νέο partition ό,τι τύπου θέλετε_ -->
   - Ακουλουθήστε [αυτές](https://www.howtogeek.com/howto/14912/create-a-persistent-bootable-ubuntu-usb-flash-drive/) τις οδηγίες και δημιουργήστε το δικό σας persistent live usb

---
### Υλικό εργαστηρίου

1. Εργαστήριο #1 - Εισαγωγή στο Unix/Linux shell
2. Εργαστήριο #2 - Εγκατάσταση προγραμμάτων μέσω του terminal
   * Εγκαταστήστε το [homebrew](https://docs.brew.sh/Homebrew-on-Linux) στο Linux σύστημά σας, παρότι υπάρχουν κάποια security concerns, πχ [εδώ](https://discourse.brew.sh/t/security-issues-using-homebrew-malicious-insertion/3379/2), η χρήση του σε ένα περιορισμένο, εκπαιδευτικό περιβάλλον θα διευκολύνει πολύ την εγκατάσταση των απαιτούμενων προγραμμάτων
     - Η εγκατάσταση του Homebrew προαπαιτεί τη παρουσία διαφόρων λογισμικών, όπως πχ git, τα οποία μπορεί να λείπουν από το περιβάλλον σας και τα οποία θα πρέπει να εγκαταστήσετε - σε περιβάλλον ubuntu αυτό μπορείτε να το πετύχετε ως superuser με την εντολή `sudo apt-get install <package-name>`
   * Εγκατάσταση [asciinema](https://asciinema.org/docs/installation), πχ μέσω brew
   * Εγκατάσταση των
     - [cheat](https://github.com/cheat/cheat)
     - [tldr](https://tldr.sh/)
     - [neofetch](https://github.com/dylanaraps/neofetch)
   * Εξάσκηση στη χρήση του asciinema
     - Έναρξη καταγραφής `asciinema rec`
     - _εκτέλεση shell εντολών της επιλογής σας_
     - Παύση καταγραφής `exit`
     - Για τοπική αποθήκευση `Ctrl+C`
       - σημειώστε το `/path/to/file.cast`
     - Αναπαραγωγή καταγραφής `asciinema play /path/to/file.cast`
   * Μελετήστε τις παραμέτρους που μπορεί να πάρει η `asciinema` και
     - ελαχιστοποιήστε το idle recording time σε 1 sec
     - προσθέστε ένα τίτλο στην καταγραφή
3. Εργαστήριο #3 - Αξιοποίηση git & github
   * Μελετήστε τη διάλεξη που είναι διαθέσιμη εδώ: https://courses.cs.washington.edu/courses/cse390a/12au/lectures/11/390aGitIntro_12au.pdf
   υλοποιήστε την δραστηριότητα δημιουργώντας ενός local git repository.
   * Αξιοποιήστε το GitHub Learning Lab και εγγραφείτε στην εκπαιδευτική δραστηριότητα [Introduction to GitHub](https://lab.github.com/githubtraining/introduction-to-github) στην οποία θα έχετε τη δυνατότητα να επεξεργαστείτε θέματα όπως:
     - Assign an issue to yourself / Close an issue
     - Create a branch / Commit your file to the branch
     - Open a pull request / Respond to a PR review / Merge a PR
4. Εργαστήριο #4 - Εξοικείωση με το vim editor
   * Ελέγξτε ποια έκδοση του vi εκτελείται στο τερματικό σας
     - Αν δεν τρέχει VIM αλλά την παλιότερη έκδοση VI, εγκαταστήστε τον vim μέσω του Homebrew
   * Ακολουθήστε το short tutorial [vim editting exercises](https://nsrc.org/workshops/2017/afnog-bootcamp/exercises/exercises-editing.md.htm)
   * Αξιοποιήστε όσες περισσότερες εντολές μπορείτε, _cheat sheet_ [εδώ](https://www.thegeekdiary.com/basic-vi-commands-cheat-sheet/)
* Δύο λόγια για τα VI modes [εδώ](https://www.geeksforgeeks.org/vi-editor-unix/)
