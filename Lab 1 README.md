**ECE 13 Lab 1 README**  
“Authors: Akshera Paladhi ([apaladhi@ucsc.edu](mailto:apaladhi@ucsc.edu)), Arthon Greenspan ([agreensp@ucsc.edu](mailto:agreensp@ucsc.edu)), Aanvi Gera ([agera@ucsc.edu](mailto:agera@ucsc.edu))”  
“Collaborators: Akshera Paladhi, Arthon Greenspan, Aanvi Gera”  
Commit IDs-  
Akshera Paladhi: aae316d6950095e722a8f61e932de647d6eef549  
Arthon Greenspan: 272658b24a6744251a2649b120afcd5e2aad3be4  
Aanvi Gera: 40f30ba82015be02dc099db010208a41cef59597

Part 0 (Hello World) \-

Local:  
\-Akshera Paladhi’s output

Serial:  
\-Akshera Paladhi’s output

Part 1 \-  
\[45, 207, 70, 41, 4\]  
\[45, 207, 70, 41, 4\]  
\[45, 207, 70, 41, 4\]  
\[45, 70, 207, 41, 4\]  
\[41, 45, 70, 207, 4\]

Last output \- serial \- \[4, 41, 45, 70, 207\]  
\-Akshera Paladhi’s output

Part 2 \-   
\-Akshera Paladhi’s output

Part 3 (Extra Credit) \-  
\-Akshera Paladhi’s output

Reflections \-

Please add some thoughts of your own:   
● Describe how you and your teammates collaborated on this assignment. 

Akshera Paladhi:  
My teammates and I collaborated on this assignment by working on each part individually and asking questions if we needed help. Each of us would try our best to go through each problem by ourselves first before we asked the other person so that we could clearly understand what was going on with our code rather than not trying it out at all and getting all confused. After we finished each problem we would also check each other's work and give advice on how we would further improve our work if needed. In order to meet up, we all contacted each other through email and met up either during lab sections, zoom meetings, or in person on campus. 

Aanvi Gera:  
We collaborated on this assignment by meeting up over zoom meetings and in person meetings to discuss our issues and to assist each other when needed. We all attempted the problems and instructions ourselves first and then helped each other when we asked. We wanted to understand the code ourselves first before we collaborated and then stayed in contact over online communication to continue helping each other. 

Arthon Greenspan:  
While we all wrote our code individually, we collaborated by helping each other setup ssh keys, solve bugs, and ensure that we were following the instructions correctly. We met on zoom as well as in person both through the labs, and on our own time in the C9 lounge. 

● What mistakes did you make, and how did you identify and solve them?  
   
Akshera Paladhi:  
The mistakes I made was for Part 0, I was unable to print hello world on the local server because I did not realize that the \<COMMON\_PATH\> the document was referring to was an actual document and it took me sometime to realize what the ../../Common meant and I realized that is I would tell the terminal to go from where it currently is to another folder. Another mistake I made was that I realized for Lab01 Part 1, the reason I could not debug my code properly was because my STM32 was not plugged in properly to my device so I was unable to find the numbers and move forward. However, once I plugged in and uploaded and built my code, it finally worked. I also made another mistake where instead of pressing the pause and continue button to find all my different arrays, I kept pressing restart instead, but then as I was talking to one of the Lab TAs, they told me that I needed to just press the pause and continue button. The third mistake I made was not understanding what a serial output was because I thought I had to code out this serial output, but then I found out from a peer that it is just the symbol that looks like a charger and that will give me all my serial outputs. 

Aanvi Gera:  
I made a couple mistakes with the formatting with the code and the platformio.ini file. This caused many issues when compiling and uploading. I fixed these by copy and pasting the given code from the given instructions rather than typing it myself to rid of any spelling errors. For formatting, I searched up the proper formatting for C programs and worked from there.

Arthon Greenspan:  
The main mistake I made was not checking the capitalization of the Common header files as the platformio compiler was looking for “dma.h,” while the file in Common was named “Dma.h.” At first, I tried to fix this by updating my includepath in vscode, as that had solved other \#include related errors I had earlier in the lab. However, I eventually realized that Common was already in the includepath, which led me to look at other potential reasons as to why the file would not exist. Eventually, with the help of a TA, I was able to find the capitalization error and fix it.   
   
● Do you have any feedback for us about this lab?

Akshera Paladhi:  
The feedback I have for this lab is that it would be nice if we could go over the terminal or Linux syntax concepts in class or lab sections through slides, because my peers and I were struggling and many of us were confused. I know there were readings, but explanations through slides could have been helpful because some of the instructions on the lab made it seem like many knew how to do these concepts, but not a lot of people came into this class knowing these topics. 

Aanvi Gera:   
I do have to agree with my teammate, there is a lot of implied instructions given that I didn’t exactly know how to do because of lack of experience and was thinking that we would fill in the gaps in class. It did help that there are a lot of lab sections and TAs to help because I asked a lot of questions during that time. The readings and explanations become really heavy to read sometimes and don’t make a lot of sense without someone walking you through it. 

Arthon Greenspan:  
One piece of feedback I would give is to capitalize the D in \#include “dma.h” on line 22 of the Dma.c file because while platformio seems to ignore the difference for many people’s machines, for some machines, such as mine, it threw an error due to the difference in capitalization. Changing the capitalization would allow it to compile successfully by default on all machines. 