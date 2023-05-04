Download Link: https://assignmentchef.com/product/solved-csc3320-lab-6-part-1-and-2
<br>
<span class="kksr-muted">Rate this product</span>

Lab Assignment 6 – Part 1 – In-Lab

Purpose: Learn how to correct a shell script and write more

complicated shell scripts.

Part 1:

In order to finish the tasks in this lab, you must connect to

snowball server to copy my checkError.sh

$cp /home/yye10/public/checkError.sh checkError.sh

In Lab 5, you may have tried the shell script checkError.sh in part 3. However, there are four errors on four different lines in that shell

script. Please correct all the four errors by writing down the line number, the error and the correction as below:Line #: Error: Correction:

Note: please use cat -n to check the line numbers.

$#/bin/bash/* Check Error Script */

<pre> echo "Try to find out some errors!!!"</pre>

<pre> # Seach for the words which can be matched by regex [^a]*ce</pre>

<pre> # And save the output to file "Result" echo "The regex [^a]*ce can match the string(s):" &gt; Result grep '^[^a]*ce$' &lt;&lt; END &gt;&gt; Result lance</pre>

ace brace

decide piece

-ENDHERE

<pre> # Check the existence of file "Result"</pre>

<pre> # Send the content in "Result" to your emailbox # $1 is replaced by your campusID ls    mail <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4367720330373627262d376d2430366d262736">[email protected]</a> &lt; Result</pre>

# $1 is replaced by your campusIDecho “The result has been sent to ${1}@student.gsu.edu”echo “Congratulations! You have corrected all the errors!”

1

Hints:

<ul>

 <li>  Following is a sample of the output once all the errors are corrected $ ./checkError.sh ylong4Try to find out some errors!!! checkError.sh Result<pre>       The result has been sent to <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="641d080b0a03502417101100010a104a0317114a010011">[email protected]</a>       Congratulations! You have corrected all the errors!</pre></li>

 <li>  You would also receive an email sent from your snowball account once all the errors are corrected.</li>

 <li>  You may need to use CTRL-C to terminate the execution of the command, especially for the script file with errors.Part 2:Write a single shell script hello.sh which can finish the list of tasks as below:</li>

</ul>

<ol>

 <li>Greet user. E.g. Welcome to computer science society.</li>

 <li>Contain a comment section with your name, and email address.</li>

 <li>Printthedate.</li>

 <li>Print the number of directories in /home .</li>

 <li>Print the value of variables PATH, USER and SHELL.</li>

 <li>Print your disk usage (df).</li>

 <li>PrintPlease,couldyouloanme$25.00?</li>

 <li>Print if x = 2, x * x = 4 , x / 2 = 1</li>

 <li>List all the .sh files with c at the beginning of the file name in current working</li>

</ol>

10.

directory.Tell the user Good bye and the current hour (see manual page of date command

refer to the webpage at http://www.thegeekstuff.com/2013/05/date-command-

examples )Include the content of hello.sh in your answer sheet. Besides, please

also upload hello.sh as a separated file.

Upload your answer sheet to the folder named “Lab 6_P1” of the dropbox in the iCollege

system. Name your file in the format of Lab6_P1_FirstnameLastname.pdf/doc

Hints:

<ul>

 <li>  When printing out strings using echo, to escape the special meaning of the meta-character, please use back slash  before the meta-character.</li>

 <li>  To share files between remote server and the host machine, we can use FileZilla – A FREE FTP. The link to download this application is https://filezilla-</li>

</ul>

project.org/download.php

Lab 6 part 2

Purpose: Learn the differences between writing a Bourne shell script and Java program. Learn how to use command argument in a Bourne Shell script. Learn how to compile and run Java and C programs in Unix terminal.

Part A:Please complete the tasks in following table step by step and finish the questions below the table.Step 1: Go to your home directory (cd ~) and create a new file named as foo.sh (vi foo.sh

or nano foo.sh), then include following lines in your foo.sh.

Step 2: Save your file and exit editor.

Step 3: Try following command to make simple.sh executable. $chmod a+x foo.shStep 4: Execute this file by invoking its name.

$./foo.sh

Note: when typing the shell script in your terminal, please be very careful of the spaces.1

Questions:

1) Attach a screenshot of the output in step 4.2) Describe what does the shell script foo.sh do?

Part B:Step 1: Edit your foo.sh and change “ -le 3 ” to “ -le $1 ” .

Step 2: When finished, save the foo.sh and exit editor. Then try executing it again by typing following command.$./foo.sh 5

Question:

Attach a screenshot of the output.

Part C:Step 1: Edit your foo.sh in part B by making following modifications:

<ul>

 <li>  Add two new lines below between line “i=1” and line “while [ $i -le $1 ]” echo please input a numberread num</li>

 <li>  Change “ -le $1 ” to “ -le $num ” .Step 2: When finished, save the foo.sh and exit editor. Then try executing it again by typing following command and type 5 as the input of the number.$./foo.shQuestion:Attach a screenshot of the output.Part D:Write a Java program named foo.java to accomplish the same task as that in foo.sh of PartA.Note: If you want to run your Java program in terminal,

  <ul>

   <li>  to compile foo.java, please try$javac foo.java</li>

   <li>  To execute it, please try $java fooQuestion:</li>

  </ul></li>

</ul>

2

Then put the source code of foo.java in your answer sheet.

Part E:Create and run Kernighan and Ritchie’s famous “hello,world” program.Step 1: Go to your home directory (cd ~) and create a new file named as hello.c (vi hello.c

or nano hello.c), then include following lines in your hello.c . #include &lt;stdio.h&gt;

<pre>int main(void){</pre>

<pre>  printf("Hello,world
");</pre>

return 0; }

Step 2: Save your file and exit editor.Step 3: Compile and link the hello.c program by following command.

$cc hello.c

Note: after this command, a default executable program named as “a.out” will be generated in current directory if there are no errors with your C program. You can use ls to check the existence of a.out .Step 4: Run the executable program a.out

$./a.out Questions:

1) Attach a screenshot of the output in step 4.

2) Try following command to compile and link hello.c again. And tell what new file is generated after this command?$cc -o hello hello.c3) Try command below and attach a screenshot of the output.

$./hello4) Now write a new C program named as myName.c based on hello.c. In this program,

print out your first name and last name instead of “Hello,world”. For example, the output could be “My name is Yuan Long”.Execute your myName.c and attach a screenshot of the output. Then write the source code

of myName.c in your answer sheet and upload your file myName.c to classroom.

3

Submssion:

Note: Please follow the instructions below step by step, and then write a report by answering the questions and upload the report (named as Lab6_FirstNameLastName.pdf or Lab6_FirstNameLastName.doc) to Google Classroom, under the rubric Lab 6 Out-of-lab Assignment.

Please add the lab assignment NUMBER and your NAME at the top of your file sheet.