# Part 1 - Debugging Scenario
## Error in Code from Lab
### Anonymous<br>
Hi, there seems to be a strange error in my bash script for the grading script and I am struggling to find the source of it. I believe the error seems to stem from jUnit itself as that is what the error message seems to state but messing with the lib folder or even rewriting the jUnit access command doesn't seem to work. It also seems to affect the grading area
as even when tests are supposed to fail they are passing. In the screenshots below of the tests the first one works fine however the error still appears, but the one under it also shows the error, but it should say "Test failed. F." rather than "Test passed. A.". I have also provided the grade.sh script can someone help?

![](lab5images/error_output.png)<br>
<br>grade.sh script <br>
![](lab5images/gradeshvim.png)<br><br>
### Response from TA <br>
Hello, There are actually multiple errors in your grade.sh script. From the looks of it you seem to be working from a Macbook remember that for Windows paths for directories use ";" while for Mac they use ":". This error has nothing to do with the grading area however, it is not recursively copying the file, I would recommend looking up the differnt options for 
the cp command.<br><br>
### Output from Student's fixed code <br>
![](lab5images/fixedCode.png)<br>
The result of the fix the TA recommended. The bug was that for the path to the jUnit library the bash script used ";" which was for Windows terminal command. The problem here is that since this script is running on Mac it needs ":" in the filepath which is why the jUnit error was appearing. The next bug in the script is from line `cp -r lib grading-area`. In order
for the file to recursively copy it needs a capital R rather than the lowercase r, so the correct version would be `cp -R lib grading-area`. For this type of file I had the wrong cp option. <br><br>

---

The directory needed to access this file is:
`/Users/pedroarias/lab9/list-examples-grader`
<br> And the Files inside are: 
`GradeServer.java`        `Server.java`             `TestListExamples.java`   `grade.sh`                `grading-area`            `lib`                     `student-submission`

# Reflection 
Something I learned from my lab expirence is that I found out how to work using vim and shortcuts within vim. While I had some knowledge of how to use a command terminal for running commands I had no idea I could actually look inside of them and edit them all within the command line itself. I found this to be cool as while sure it is harder to edit files in vim, if there ever was a case where I needed to do it well now I know how to do it and I find that amazing. Overall I thoroughly enjoyed the labs of this class.
