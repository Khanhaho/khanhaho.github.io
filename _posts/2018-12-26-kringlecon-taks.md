---
layout: post
title: "What I did at KringleCon"
categories: misc
---

### How I went pass each challenge in KringleCon

1. This asked for a phrase related to previous Holiday Hack. I first went back to previous Holiday hack and found the answer (Happy Trails). Later, I went through the castle and found Bushy Evergreen, she asked to help with the Vi text editor. The screen said my task is to exit the editor. Typing "exit" did not help, so I pressed Ctrl-C, when the screen displayed "use :quit<Enter> to exit. I entered ":quit" and ENTER, the screen said file not save, use "!" to overwrite, so I entered ":quit!" and ENTER, and it worked. The screen congratulated me.

2. The system is a remote sqlite3 database accessible via a PowerShell injection using the & operator. At clicking "The name Game", a black window pops up. Enter 2 to verify database, then enter "127.0.0.1 & ls" to display what is available at the remote root. After that enter "127.0.0.1 & sqlite3", this will open the sqlite3 program remotely. Enter ".help" to show the available sqlite3 commands. Enter ".open onboard.db" to connect to onboard database, then enter ".dump onboard" and all data from the database is shown. I found Chan to have first name as "Scott". At this point, exit sqlite by enter ".quit", and redo from option 2, and enter "127.0.0.1 & runtoanswer" and enter "scott" (no capital s).
The above was only to help Minty Candycane with her problem. Once you solved her problem, clicking on her and she will tell you about the vulnerability of the CFP site. It turned out that the site has a misconfiguration. Even though the site looks inaccessible, you may only need to remove some letters/characters at the end of the URL and interesting things will show. In this case, after clicking into "Apply Now!", the URL would become "https://cfp.kringlecastle.com/cfp/cfp.html", then we only need to remove the /cfp.html at the end and the site index will show.
As the "rejected-talks.csv" file show, the author of the rejected talk in the question is "John McClane".

3. In this challenge I need first to help Tangle Coalbox with the Lethal ForensicELFication, using forensic skill to find out the name of the girl whom the poem was written about.
Enter "ls" in the terminal window only show the file "runtoanswer", this is where you submit the answer. 
Seeing there is nothing in the directory, use the Up arrow key to see the previous command entered into the system. Some of those commands listed a poem was created using the VIM text editor under .secrets/her/poem.txt
Display this poem using either "cat", "nano" or "vim" and it was obvious that the name of an elf girl was replaced by "NEVERMORE".
There was no other command that showed what was replaced. However VIM has the info data and this can be accessed by "cat .viminfo". From there, we can see that "NEVERMORE" replaced "Elinore".
The truth is I didn't know about this .viminfo file, I saw that from the chat.
Once there you need to find the code to open the door to the unprepared speaker room. The trick is to use the DE Bruijn sequence generator to generate a set of code that you can trial and error. Since the De Bruijn sequence is a circular sequence, if you keep going as per the list (in the excel file) under MOOC/SANS, eventually you'll get that the code for the room is 0120. Enter that to get into the room, meet Morcel and he says a greeting, which is then used to complete the challenge.



![kringle con](/assets/img/kringlecon.jpg)



