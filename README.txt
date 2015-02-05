UTEID: jmt2939; dbd453;
FIRSTNAME: Jeremy; Daniel;
LASTNAME: Thompson; Durbin;
CSACCOUNT: jmt2939; majisto;
EMAIL: jthompson2214@gmail.com; majisto@gmail.com;

[Program 5]
[Description]
Our program begins by creating Password Objects for each line in the password input file by calling fill_password_list.  The Password Class splits the input line into the relevant information we want to store, including the salt, whole_password and the username.  These will be referenced throughout the program.  We store these objects in a LinkedList called password_list.  The input dictionary is initially stored in user_dict as a LinkedList.  The mangles are stored in user_dict_mangle.  We also keep a Stopwatch running. 

The main loop goes through the password_list until it is empty.  In each step, a password is removed and run through a stage.  Each stage is detailed in the finish part below.   If the password is not found, it is enqueued at the back of the list and we check the next password.  If it is found, we print out the information, and do not enqueue it, thus it will not be checked again.  We also stop checking anytime the password is found at each stage instead of running through the entire dictionary.   There are 6 stages in total with brute forcing being the last.  Each stage is required to be run for each password before we move onto the next stage.  This way, even if the first password requires brute force, we will still find the others since they will run through the other stages.

[Finish]
We finished all of it. The way we have things there are 6 stages
1. check against the user dict
2. check against a list of the 10k most common passwords.
3. do the first mangle and check against those results
4. do the second mangle and check against those results
5. do the third mangle (just the delete_front/back. Otherwise we run into heap errors) and check against those results
6. start a brute force calculation against the remaining passwords. 
the output will tell you which of the mangle stages it is currently in, or the brute force method. Which you can just let run for as long as you want. 
for the password output, we have the number of the password (out of all the ones we're trying to find) the username of the person, the password, the time that we found it in, and the encrypted version of the password. 

(all timings are when ran on the CS machines)

[Test Cases]
[5d.txt simplepass.txt] (testing Brute force algorithm)
Starting first mangle.
Done with first mangle.
Starting second mangle.
Done with second mangle.
Starting third mangle
Done with mangle_third
Beginning Brute Force.
Password 1/2 for user jeremy is: !, at time: 6.573850606 seconds. The encryption is: aaRwjIXbb06bc
(after this we stopped it because we know that the algorithm works and who knows how long it'll take to break the randomly generated string).

[short-dict.txt passwd1.txt]
Password 1/20 for user michael is: michael, at time: 0.02911734 seconds. The encryption is: atbWfKL4etk4U
Password 2/20 for user samantha is: amazing, at time: 0.045448074 seconds. The encryption is: (bUx9LiAcW8As
Password 3/20 for user maria is: Salizar, at time: 0.095551332 seconds. The encryption is: !cI6tOT/9D2r6
Starting first mangle.
Done with first mangle.
Password 4/20 for user abigail is: liagiba, at time: 1.236455884 seconds. The encryption is: &i4KZ5wmac566
Password 5/20 for user tyler is: eeffoc, at time: 1.289783454 seconds. The encryption is: <qt0.GlIrXuKs
Password 6/20 for user alexander is: squadro, at time: 1.546129205 seconds. The encryption is: feohQuHOnMKGE
Password 7/20 for user james is: icious, at time: 1.806430684 seconds. The encryption is: {ztmy9azKzZgU
Password 8/20 for user benjamin is: abort6, at time: 1.807636796 seconds. The encryption is: %xPBzF/TclHvg
Password 9/20 for user morgan is: rdoctor, at time: 1.885813074 seconds. The encryption is: khnVjlJN3Lyh2
Password 10/20 for user jennifer is: doorrood, at time: 1.984584536 seconds. The encryption is: e4DBHapAtnjGk
Password 11/20 for user nicole is: keyskeys, at time: 2.122270287 seconds. The encryption is: 7we09tBSVT76o
Password 12/20 for user evan is: Impact, at time: 2.250197233 seconds. The encryption is: 3dIJJXzELzcRE
Password 13/20 for user jack is: sATCHEL, at time: 2.462328525 seconds. The encryption is: jsQGVbJ.IiEvE
Password 14/20 for user victor is: THIRTY, at time: 2.720714573 seconds. The encryption is: w@EbBlXGLTue6
Password 15/20 for user connor is: enoggone, at time: 3.543013907 seconds. The encryption is: gwjT8yTnSCVQo
Starting second mangle.
Done with second mangle.
Password 16/20 for user caleb is: teserP, at time: 46.570471336 seconds. The encryption is: 8joIBJaXJvTd2
Password 17/20 for user nathan is: sHREWDq, at time: 79.187032316 seconds. The encryption is: nxsr/UAKmKnvo
Password 18/20 for user rachel is: obliqu3, at time: 104.139247895 seconds. The encryption is: KelgNcBOZdHmA
Starting third mangle
Done with mangle_third
Password 19/20 for user dustin is: litpeR, at time: 241.249123393 seconds. The encryption is: 5WW698tSZJE9I
Beginning Brute Force.

[Not Cracked]
paige:T8U5jQaDVv/o2:519:519:Paige Reiser:/home/paige:/bin/bash

[short-dict.txt passwd2.txt]
Password 1/20 for user michael is: tremors, at time: 0.024636792 seconds. The encryption is: atQhiiJLsT6cs
Password 2/20 for user abigail is: Saxon, at time: 0.033710805 seconds. The encryption is: &ileDTgJtzCRo
Starting first mangle.
Done with first mangle.
Password 3/20 for user tyler is: eltneg, at time: 1.536294582 seconds. The encryption is: <qf.L9z1/tZkA
Password 4/20 for user james is: enchant$, at time: 2.003980464 seconds. The encryption is: {zQOjvJcHMs7w
Password 5/20 for user benjamin is: soozzoos, at time: 2.284473716 seconds. The encryption is: %xqFrM5RVA6t6
Password 6/20 for user morgan is: dIAMETER, at time: 2.360049415 seconds. The encryption is: kh/1uC5W6nDKc
Password 7/20 for user jennifer is: ElmerJ, at time: 2.686109037 seconds. The encryption is: e4EyEMhNzYLJU
Password 8/20 for user nicole is: INDIGNITY, at time: 2.819757052 seconds. The encryption is: 7wKTWsgNJj6ac
Password 9/20 for user evan is: ^bribed, at time: 2.858353039 seconds. The encryption is: 3d1OgBYfvEtfg
Password 10/20 for user jack is: ellows, at time: 3.138543949 seconds. The encryption is: js5ctN1leUABo
Password 11/20 for user caleb is: zoossooz, at time: 3.815375502 seconds. The encryption is: 8jGWbU0xbKz06
Password 12/20 for user connor is: nosral, at time: 4.536094464 seconds. The encryption is: gw9oXmw1L08RM
Starting second mangle.
Done with second mangle.
Password 13/20 for user alexander is: Lacque, at time: 95.668127559 seconds. The encryption is: fe8PnYhq6WoOQ
Password 14/20 for user nathan is: uPLIFTr, at time: 189.595728546 seconds. The encryption is: nxr9OOqvZjbGs
Password 15/20 for user dustin is: Swine3, at time: 280.621265905 seconds. The encryption is: 5Wb2Uqxhoyqfg
Starting third mangle
Done with mangle_third
Beginning Brute Force.

[Not Cracked]
victor:w@FxBZv.d0y/U:512:512:Victor Esperanza:/home/victor:
maria:!cSaQELm/EBV.:518:518:Maia Salizar:/home/maria:/bin/zsh
paige:T8U5jQaDVv/o2:519:519:Paige Reiser:/home/paige:/bin/bash
rachel:KenK1CTDGr/7k:516:516:Rachel Saxon:/home/rachel:/bin/bash
samantha:(bt0xiAwCf7nA:502:502:Samantha Connelly:/home/samantha:/bin/bash

