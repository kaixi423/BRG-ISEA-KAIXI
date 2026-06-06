Writing Bash Scripts and Using Regular Expressions

(Based on: Bash Coding Lab)

Lab: Bash Scripting – Write simple shell scripts for server automation.

 <img width="769" height="437" alt="image" src="https://github.com/user-attachments/assets/71318307-b3a1-4e95-bdcb-84561c998f1e" />

For the set up, I started the script with #!/bin/bash at the top. I did not understand the meaning of #!/bin/bash so I googled it and found out it is called a “shebang” which is used to tell the ubuntu server that this is a script and needs to use the Bash interpreter to read and run the code/script below it.
For the Echo command, it is similar to the print command where it makes the text inside the “..” show up on the screen so the user knows the script has started running.
I followed it up with a if statement to check if a specific file named testfile.txt exist on the server. I also googled and found out that for decisions (if) programmers who created the bash language back then thought it was a smart idea to use the backward word (fi) to show that the decision has been made. And for loops (for and while) they decided that a loop is a repetitive action that the script is running. So when the loop is finished the script is completed.
“for X in server 1 Server 2 server 3; do” this starts a for loop which takes a list of three text values and tells the computer to loop through each one of them. 
“done” tells the computer that the loop has finished running through the current item and should go back to the top of the list for the next one. Once the list is empty the loop will end.
“COUNT=3” creates a new variable named COUNT and assigns it a starting number value of 3
“while [ $COUNT -gt 0]; do” this starts a while loop which keeps repeating as long as a condition is true, the -gt flag stands for greater than. This line results into looping continuously as long as COUNT is greater than 0.
“COUNT =$((COUNT -1))” takes the current number in COUNT and subtracts 1 and updates the variable with the new number. This line is needed to ensure the loop eventually counts down to 0 and stops.
“done” is similar to the for loop, the word done is the end of the while loop block.


Run scripts using `bash script.sh` or `chmod +x script.sh`. 
After saving the code, I executed the file by typing the command bash simple_script.sh into the terminal. The script executed and printed out the messages successfully.
I learned that using the bash command is a direct and reliable way to execute a script file. 


<img width="705" height="369" alt="image" src="https://github.com/user-attachments/assets/e599fbea-b88d-4494-81ae-26ef239d7d77" />


