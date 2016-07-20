# Lexicon_Project

### Lexicon: Dictionary, anywhere

Lexicon is a native linux dictionary made for providing meaning of a word anywhere, instantly.
It fetches the meaning from database and pushes it through notification. No need to Google the word or open a dictionary.

- Highlight the word.

- Press ALT + CTRL + Z.    
![Screenshot](http://i.imgur.com/QV3wLFe.png?1)

---

### Features: 

- Non-intrusive interface
- Synonym support
- Works offline
- Online support
- Translation support for major languages.
- Auto-correct (beta)
- Works everywhere on the desktop

---
### Debian Installation guide:

1) Edit /etc/apt/sources.list and add the following line at the end:

    deb http://insomniacprogrammer.hol.es/repo/ trusty main

2) Run the following commands:

    gpg --keyserver keyserver.ubuntu.com --recv-keys 793175CB
    gpg --armor --export 793175CB | sudo apt-key add -
    sudo apt-get update
    sudo apt-get install lexicon
 
 3) Run:
     lexicon
 and click launch.

For more help run:

    man lexicon    

**If the process complains about package yad, run:**

    sudo add-apt-repository ppa:webupd8team/y-ppa-manager
    sudo apt-get update
    sudo apt-get install yad
    sudo apt-get install lexicon

---
### AUR for arch users

    yaourt -S lexicon-dictionary

---

Originally posted: [here](https://redd.it/3z1ci3) and [here](https://redd.it/3z1b0m)

--------------------------------------------------------------------------------

*/usr/bin* - has main lexicon script. The Launcher.

*/usr/lib/lexicon* - has all the source code. AutoCorrect and Lexicon named scripts contain all the functioning.

*/usr/share/lexicon* - has all the database.

For further information and installation instructions, follow [here](https://redd.it/3z1b0m) or [here](https://redd.it/3z1ci3).

------------------------------------------------------------------------------------------------------

Team Lexicon has hopes that the project can grow strong as **GoldenDict** and that's why we need help of capable programmers in refining and improving following features:

  * **Combined Database** - A single database containing Meanings, Phonetics, Synonyms, Translation (Spanish, French, Italian, German).    
Wiktionary has good database, containing all that is required. But parsing their [Dump](http://dumps.wikimedia.org/enwiktionary/latest/enwiktionary-latest-pages-articles.xml.bz2) to a structured sqlite3 is backbreaking.    

  * **Autocorrect** - Better, tested, algorithm required.    
Current auto-correct is based on little remodeling of a-grep(Wu-Manber algorithm). The Auto-Correct works but it's annoying since it always manage to find substitute for words not in dictionary, thus not allowing it to search online.    
  
  * **Porting to different platforms** - Currently, Lexicon only support Debian. Porting to popular platforms like Fedora, RedHat, Arch, Gentoo, Slackware is required.

---------------------------------------------------------------------------------------------------------------

Right now, we further have online translation support and faster notification push method ~~(Not Published Online). We are hoping to integrate all the features together to big release.~~ 
Translation support and faster notification push method along with IPA support committed on 20/July/2016.  

You can contact Project_Lexicon at LinuxSDA@gmail.com    

*“It is amazing what men can accomplish if they do not care who gets the credit.” ― Harry S. Truman*
