# Εργαστήριο μαθήματος Επικοινωνία Ανθρώπου-Υπολογιστή
## Πρόγραμμα Εργαστηρίου
| Αριθμός μαθήματος | Υλικό |
| --- | --- |
| 1 | [1. Εργαστήριο 1](#εργαστήριο-1) |
| 2 | [2. Εργαστήριο 2](#εργαστήριο-2) |
| 3 | [3. Εργαστήριο 3](#εργαστήριο-3) |
| 4 | [4. Εργαστήριο 4](#εργαστήριο-4) |
| 5 | [5. Εργαστήριο 5](#εργαστήριο-5) |


---
Για την υλοποίηση των εργασιών του εργαστηρίου θα πρέπει να εργαστείτε σε ένα Unix/Linux terminal. Θα αξιοποιήσετε κάποιες από τις ήδη διαθέσιμες εντολές του shell, αλλά θα χρειαστεί να εγκαταστήσετε και κάποια νέα προγράμματα.

Για να εργαστείτε καθένας στο δικό του περιβάλλον εκτέλεσης, μπορείτε να αξιοποιήσετε όποια από τις πιο κάτω επιλογές σας εξυπηρετεί καλύτερα:
 * _Bring your own laptop:_ Ιδανικά με ήδη εγκατεστημένο linux, πχ ως dual boot
 * _Bring your own laptop:_ Εγκατάσταση ενός linux εντός virtual box

   [Virtual box](https://www.virtualbox.org/)
\
   [Download the Linux ISO](https://ubuntu.com/)
\
   [Installing Linux in VB](https://itsfoss.com/install-linux-in-virtualbox/)

```
Χρειαζεται να κατεβάσετε ένα ISO image, του Linux Distribution που θέλετε
να χρησιμοποιήσετε.. 
```

 * _Bring your own laptop:_ Αξιοποίηση Windows Linux Subsystem εφόσον το laptop σας τρέχει Win10
 
 Installing Linux in Windows 10 [Οδηγίες](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

**Step 1**: Enable “Windows Subsystem for Linux” feature
Πηγαίνετε στις εφαρμογές και πατήστε Turn Windows Features On and Off. –Από εκεί πρέπει να τσεκάρετε “Windows Subsystem for Linux” and “Virtual Machine Platform” και μετά να κάνετε μία επανεκκίνηση.
**Powershell** – Πάμε στο Powershell το οποίο τρέχουμε σαν Administrators. Όταν τρέξει το powershell βάζουμε την παρακάτω εντολή: 
**Enable-WindowsOptionalFeature** Online -FeatureName VirtualMachinePlatform -norestartdism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all
Επιβεβαιώνουμε την εντολή με Y
και κάνουμε reboot το σύστημά μας. 
**Step 2**: Download a Linux system from the Windows store
I advise going for Ubuntu in this case

 
 

 
 * Χρήση _persistent live ubuntu usb_ (επιτρέπει την εκτέλεση XUbuntu Desktop περιβάλλοντος το οποίο διατηρεί τις αλλαγές που κάνετε, πχ εγκατάσταση προγραμμάτων)
   <!-- - Μπορείτε να κατεβάσετε ένα κατάλληλο `image` [εδώ](https://195.130.127.104/hci.xubuntu.iso)
     - Μεταφέρετε το image σε ένα usb stick τουλάχιστον 4GB
     - Κάντε boot από οποιοδήποτε desktop του εργαστηρίου
     - _Μετά την ολοκλήρωση της εγκατάστασης το flashάκι σας θα εμφανίζεται να έχει μέγεθος 4GB, χρησιμοποιήστε το [GParted](https://www.howtoforge.com/partitioning_with_gparted) για να δημιουργήσετε ένα νέο partition ό,τι τύπου θέλετε_ -->
   - Ακουλουθήστε [αυτές](https://www.howtogeek.com/howto/14912/create-a-persistent-bootable-ubuntu-usb-flash-drive/) τις οδηγίες και δημιουργήστε το δικό σας persistent live usb

---
### Υλικό εργαστηρίου

0. Github + Terminal onboarding
#### Εργαστήριο 1 
- Εισαγωγή στο Unix/Linux shell
#### Εργαστήριο 2 
- Εγκατάσταση προγραμμάτων μέσω του terminal
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
#### Εργαστήριο 3
- Αξιοποίηση git & github
   * Μελετήστε τη διάλεξη που είναι διαθέσιμη εδώ: https://courses.cs.washington.edu/courses/cse390a/12au/lectures/11/390aGitIntro_12au.pdf
   υλοποιήστε την δραστηριότητα δημιουργώντας ενός local git repository.
   * Αξιοποιήστε το GitHub Learning Lab και εγγραφείτε στην εκπαιδευτική δραστηριότητα [Introduction to GitHub](https://lab.github.com/githubtraining/introduction-to-github) στην οποία θα έχετε τη δυνατότητα να επεξεργαστείτε θέματα όπως:
     - Assign an issue to yourself / Close an issue
     - Create a branch / Commit your file to the branch
     - Open a pull request / Respond to a PR review / Merge a PR
#### Εργαστήριο 4 
- Εξοικείωση με το vim editor
**What is Vim?** Vim is an advanced text editor. The name Vim is a contraction of Vi and Improved. So, Vim is vi improved. I’m not going to bore you with an entire history lesson, but quickly, Vi is a text editor that was originally created for the Unix operating system. Vi is actually short for “visual” and started out as the visual mode for the even older ex line editor. On most modern systems, Vim has replaced vi. Even if you think you’re starting vi by running the vi command, for example, Vim is what actually starts.So, long story short, Vim is a powerful text editor.

**Why bother learning Vim**: Vim is installed in all Unix systems. Often it is the only text editor on the system. Edit something on the command line, and end up in VIM. It makes a lot of sense to have at least some familiarity with VIM. It is very powerful though. You can edit text much easier than any other text editor. 
   
   * Ελέγξτε ποια έκδοση του vi εκτελείται στο τερματικό σας
     - Αν δεν τρέχει VIM αλλά την παλιότερη έκδοση VI, εγκαταστήστε τον vim μέσω του Homebrew
   * Ακολουθήστε το short tutorial [vim editting exercises](https://nsrc.org/workshops/2017/afnog-bootcamp/exercises/exercises-editing.md.htm)
   * Αξιοποιήστε όσες περισσότερες εντολές μπορείτε, _cheat sheet_ [εδώ](https://www.thegeekdiary.com/basic-vi-commands-cheat-sheet/)
* Δύο λόγια για τα VI modes [εδώ](https://www.geeksforgeeks.org/vi-editor-unix/)
Προπαθήστε να τρέξετε την εντολή *vimtutor* στο shell. Θα σας οδηγήσει σε εναν οδηγό εντός του vim ο οποίος είναι πολύ κατατοπιστικός και μπορεί να
ολοκληρωθεί σε περίπου 30 λεπτά.

**Basic Vim Commands** - This list is nothing but the tip, of the tip, of the glacier that is Vim. However\
if you intend to learn Vim, you will soon learn them by heart.\
\
**:help [keyword]** - Performs a search of help documentation for whatever keyword you enter\
**:i** - turns vim to insert mode\
**ESC key** returns from insert mode\
**:e [file]** - Opens a file, where [file] is the name of the file you want opened\
**:w** - Saves the file you are working on\
**:w [filename]** - Allows you to save your file with the name you've defined\
**:wq** - Save your file and close Vim\
**:q!** - Quit without first saving the file you were working on\

Modes of Vim\
**Command mode**: When in command mode you cannot insert text. Yet there are a lot of intersting commands to use here. The command mode is the default mode of vim.\
[Vim editor commands](https://www.radford.edu/~mhtay/CPSC120/VIM_Editor_Commands.htm)\

**insert mode**: We change to insert mode with the **i** key. The mode that allows us to insert text.

**last line mode**: The last vi mode is known as vi last line mode. You can only get to last line mode from command mode, and you get into last line mode by pressing the colon key, like this :

**visual mode**:Visual mode can be very helpful for identifying large of chunks to be manipulated, by changing colors in text.\
[Getting started with Visual mode](https://opensource.com/article/19/2/getting-started-vim-visual-mode)\
[Mastering Visual mode](https://dev.to/iggredible/mastering-visual-mode-in-vim-15pl)

#### Εργαστήριο 4

[How to add something to the path](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/)

**Εισαγωγή στο VIM**
[10 Λόγοι](https://www.linuxtrainingacademy.com/10-reasons-to-learn-the-vim-editor/)

**sudo apt install vim nox**
**vim** για να ξεκινήσει
Το vim έχει διάφορα modes. To command mode είναι το default. To insert mode είναι αυτό το οποίο χρησιμοποιείται για να γράψουμε κείμενο.\
**Στο Insert mode μπαίνουμε με i.** Γυρνάμε στο command mode με το ESC.\
Με **:w** και το όνομα του αρχείου πχ. text.txt τότε σώζουμε ότι γράψαμε ως ένα αρχείο.\ 
Για να ξεκινήσουμε το vim από το shell: vim FILENAME\
:147 --> επιλογή γραμμής βάσει τον αριθμό.\ 
/foo -->αναζήτηση η οποία σε πάει στην πρώτη Instance του foo.\
/ --> επανάληψη της τελευταίας αναζήτησης.\
exit Vim type :q! to trash all changes. or :wq to save all changes


#### Εργαστήριο 5

**Εισαγωγή στον προγραμματισμό με VIM**

**:syntax on**->Ανοίγει τα χρώματα για επεξεργασία κειμένου για προγραμματισμό\
**:set number**--> Βάζει γραμμές στο πλάι της σελίδας για τα errors\
**set showmatch**› › " Show matching brackets. Χρήσιμο για programming γιατί μπορεί κάποιος να χάνεται ανάμεσα στα brackets.\
**set ttyfast** --> faster scrolling.\
**set hlsearch**--> enables search highlighting. Με αυτό τον τρόπο όταν πατάμε / για να ψάξουμε για κάποια λέξη μας δείχνει ighlighted τα matches.\ set showmode this\ shows the mode you're currently in.\
**set title**α δείξει ως τιτλο το Path για το συγκεκριμένο αρχείο.\
**:set filetype=[language]**\

**.vimrc**
Αν θέλουμε να κρατήσουμε τις αλλαγές που κάναμε, πρέπει να τροποποιήσουμε το .vimrc --Αν δεν το έχουμε μπορούμε να το φτιάξουμε. 
Σημείωση: Υπάρχει πιθανότητα να έχετε ήδη ένα .vimrc αρχείο στο σύστημά σας. Το αρχείο .vimrc που θα φτιάξετε\ στο **home folder** θα υπερισχύσει αυτού που υπάρχει ήδη. 

[Οδηγός εγκατάστασης Vim Plugins για προγραμματιστές](https://www.howtoforge.com/tutorial/vim-editor-plugins-for-software-developers/)

**Shell scripting**
[Shell Scripting Tutorials](https://www.tutorialspoint.com/unix/shell_scripting.htm)\

#!/bin/sh This is the shebang command. We use it to say to the system that a shell script is being started.
H εντολή shebang μπαίνει στην αρχή του script. Το αρχείο του βάζουμε την κατάληξη .sh. Τρέχει βάζοντας 
μπροστά την εντολή Bash. 


Εργαστήριο 6

[Help changing branch](https://stackoverflow.com/questions/1777854/how-can-i-specify-a-branch-tag-when-adding-a-git-submodule)
