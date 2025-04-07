# Algo_Filter3
The best CMD extension to sort all your Rubik's Cube algorithms pulled from all your generators to give you the exact types of algorithms you're looking for. Gone are the days of searching manually—just let this program do its thing and feel really cool.
Basic fundamentals for this program are as follows:
Insert the path to the rubiks cube generator or the txt document you compiled all of your algorithms into, I will be using kubesolver in this case.
--silent -d 13 are just parts of kubesolver to say don't tell me the depths just go down to a length of 13 so the computers memory doesn't get jacked up.
less-than into the txt document.
Next you will need to have StrawberryPerl installed on your computer, pipe to it (you may or may not need to specify the perl before the filter) and that should make the filter work.
Now for some examples:
C:\Users\natha\Documents\Cubing>kubesolver_1.0.5.exe --silent -d 13 <oll2.txt |perl algo_filter3.pl -F-3
This is your main man right here
Filters all of the algorithms straight from the definition file of Kubesolver

C:\Users\natha\Documents\Cubing>type oll3.txt |perl algo_filter3.pl -F-2 -F2-0
Filters all of the algorithms in the txt file of oll3 (useful for mass dump algs from multiple generators to find the perfect among the 3)


Move Limits Basics
Standard Cube Notation
-F equals what move you want to talk about wether F moves, R moves, L moves, U moves it will be -U, -L, -R use the capital, if you are talking about R2 and U2 moves specify with the 2
-+= are how many you want
Example: -F-3 meaning that there will be less than 3 F moves in the algs shows so wether that be 0, 1, or 2 F moves
Example: -F2-3 meaning that there will be less than 3 F2 moves used in the algorithms shown
Example: -F-=2 meaning the F move can be 2 or less times in the algorithm
Example: -F+=2 meaning the F move can be 2 or more times in the algorithm
Example: -F=2 meaning the F move is in the alg 2 times

Note: you have to put the + or - before the = sign

P.s all prime moves are 1's to make code work so F' = F1
Example: -F1=3 meaning that there will be 3 F' in the alg
