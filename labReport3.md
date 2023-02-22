# Lab Report 3

## Researching Commands
Command: ```grep```
* the following commands were all found [here](https://swcarpentry.github.io/shell-novice/07-find/index.html#:~:text=The%20grep%20command%20searches%20through,%20we're%20searching%20in).

1. ```grep -w``` 
```
$  grep -w no HistoryFrance.txt
at the age of 23, there was no question of a new prime minister
the sun, Louis was to be outshone by no one. Counselors were wholly
reforms that would give them greater opportunity; the peasantry was no
But the middle classes were no longer prepared to tolerate the 
```
The text included words like "nor" which would have shown up with ```grep no HistoryFrance.txt``` but this limits the results to only lines which contain the word "no". This is useful because it lets the user find the specific word they need.
```
$ grep -w men IntroGreek.txt
The men work in the fields or at their boats, with older men at the
```
This text included both men and women. This is useful if the user only cared about the role of men in Greece.

2. ```grep -n```
```
$ grep -n women IntroGreek.txt
60: still lead separate lives, with the women in the home, chatting across
```
This provides the exact line the word "women" shows up on. This is helpful if the user needs to know what specific line they should go to for information about women in Greece.
``` 
$ grep -n island WhatToHawaii.txt
8: islands — Oahu, Maui, Kauai, and the Big Island of Hawaii. Some
11: islands in the chain.
13: (189-sq km) island of Niihau (nee-ee-how) is called “The Forbidden
17: ranching operations for Bruce Robinson, owner of the island; the women
21: school on Kauai. Niihau’s people are free to leave the island, but once
24: island just off the southwest coast of Maui. Once inhabited by ancient
25: Hawaiians, the island has since served as an Alcatraz for criminals, a
27: (1939 to 1990). Now turned back to the state, the island is littered
32: is an atoll comprised of a few tiny islands. Best known as the site of
39: 643-9291; fax (770) 386-3053; <www.midwayisland.com>).
```
Since the word "island" appears many times in the text, it is useful to know specifically which lines it is referenced on.

3. ```grep -i```
```
$ grep -i For WhatToHawaii.txt
(189-sq km) island of Niihau (nee-ee-how) is called “The Forbidden
ranching operations for Bruce Robinson, owner of the island; the women
Hawaiians, the island has since served as an Alcatraz for criminals, a
cattle ranch, and — most recently — a bombing range for the U.S. Navy
for Kahoolawe to become a cultural reserve. Until then, it remains
Wildlife Department as a refuge for the millions of Laysan Albatross
(called gooney birds for their comical awkwardness at takeoff and
Midway. For more information, contact Midway-Phoenix (Tel. (888)
```
Since the grep is by default case-sensative, it might skip out on possible on possible lines. This command results in case-insensativity so that you can find all instances of word, regardless of its case.
```
$ grep -i This IntroJapan.txt 
This is certainly a challenging task, but the rewards for
doing so are the myriad windows and doors into this fascinating country
Everywhere you go, you’re likely to find this constant
permanence, this austere wooden structure is dismantled every 20 years
permeate the natural surroundings — in this case, a beautiful cedar
This strong sense of transience and impermanence has
this is the only way to make an intolerable situation somehow
this might reflect a reduction of social stigma in what remains a
But this does not mean Japanese society has remained
Over this amazing cornucopia presides Emperor Akihito. His
from the daily life of their increasingly beleaguered subjects. This is
criticize, to confirm stereotypes or to note exceptions. This book has
```
Similar to the last example, this allows us to find all uses of "this" without worrying about the case of the word.

4. ```grep -r```
```
$ grep -r Lucayans
./travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
./travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
Instead of having to search multiple directories and files manually, this is a useful command as it lets you recursively search through files for the word you're trying to find.
```
$ grep -r milk       
./HandRJamaica.txt:        and ackee, rice and peas, fish in coconut milk, and Escovitch fish. The
./IntroIsrael.txt:        search of “the land of milk and honey”; Jesus Christ was born, lived,
./WhatToIbiza.txt:        milk flavoured with cinnamon.
./WhatToIbiza.txt:        leche) is half coffee, half hot milk.
./WhatToIbiza.txt:        •beeruna cervezamilkleche
./WhereToIndia.txt:        moment of the day. At dawn, its color changes from milk to silver to
./WhereToIndia.txt:        granite monolith polished by centuries of libations with milk.
./WhereToFrance.txt:        cottages where she and her retinue pretended to be milkmaids and farm
./WhereToFrance.txt:        sausage (figatelli), and ewe’s or goat’s milk cheese (broccio). Be
./WhereToMallorca.txt:        cheese. Made of cow’s milk with a small percentage of sheep’s milk,
./IntroIndia.txt:        and all her products: milk, curd, butter, and dung, the last of which
./WhatToIstanbul.txt:        kebabs, and rounded off with fresh fruit or milk puddings, and cups of
./WhatToIstanbul.txt:        in a köfteci, tripe in an i«kembeci, soup in a çorbacı, and milk
./WhatToIstanbul.txt:        milk- and rice-based desserts like fırın sütlaç (baked rice pudding),
./WhatToIstanbul.txt:        combination of rice, milk, sugar, and chicken breast). A more unusual
./WhatToIstanbul.txt:        its nickname, aslan sütü — lion’s milk). Turkish-made beer is also a
```
Similar to the previous example, this lets you quickly search for the word "milk" instead of doing it manually. This one however works through a single directory instead of multiple.
