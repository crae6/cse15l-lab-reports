# Researching Commands Pt. 2
### The `find` Command

#### All of these commands were discovered by asking ChatGPT in this prompt. 
<img width="368" alt="Screen Shot 2023-03-09 at 11 10 44 AM" src="https://user-images.githubusercontent.com/122562172/224130058-19c12c5d-5aaa-4f41-a2d8-9b45f791d588.png">

#### 1. Finding by name using `-name`
* `find . -name ch1.txt`
  * This command returns <img width="427" alt="Screen Shot 2023-03-09 at 11 19 11 AM" src="https://user-images.githubusercontent.com/122562172/224131757-54f3b071-9897-42f5-b846-888e51f0b55e.png">
  * In this command, `-name` is used to search for the specified name in all directories and subdirectories of the current file. In this instance, there are five ch1.txt's found so all five of them are returned with their file path.  
* `find . -name chZ.txt`
  *  This command returns <img width="417" alt="Screen Shot 2023-03-09 at 11 22 45 AM" src="https://user-images.githubusercontent.com/122562172/224132534-c596264e-aeac-4fa5-a313-c30a0e5d1a31.png">
  *  In this command, `-name` is once again used to search for the file chZ.txt. However, this time there is only one file with the matched name, so only one is returned.
* Researched using ChatGPT

#### 2. Searching for multiple patterns using `-e`
* `grep -e fickle -e Compaq non-fiction/OUP/Abernathy/*.txt`
  * This command returns <img width="1114" alt="Screen Shot 2023-02-12 at 11 09 45 AM" src="https://user-images.githubusercontent.com/122562172/218331754-e0e1db84-d594-4c42-9615-0cc6bf21350b.png">
  * In this command, the `-e` allows us to search for multiple patterns with one search. So, here we are searching for the strings "fickle" and "Compaq". When the command-line finds these strings, it returns the file they were found in and the line that it was found on. 
* `grep -e emphasis -e 21-month-old non-fiction/OUP/Berk/*.txt`
  * This command returns <img width="1115" alt="Screen Shot 2023-02-12 at 11 15 48 AM" src="https://user-images.githubusercontent.com/122562172/218332523-8ca29ae9-1db4-44a1-9f2f-527e7f04415a.png">
  * In this command, we are once again using the `-e` command to search for multiple patterns. In this one, we search for the patterns "emphasis" and "21-month-old". The terminal then determines the lines that it finds that pattern on. 
* Researched using ChatGPT

#### 3. Inverting the search results using `-v`
* `grep -v and non-fiction/OUP/Fletcher/ch1.txt`
  * This command returns <img width="1112" alt="Screen Shot 2023-02-12 at 11 52 02 AM" src="https://user-images.githubusercontent.com/122562172/218333707-dac9fd44-52f9-4978-9af0-194a3a19ac4c.png">
  * In this command, `-v` is used so that grep is reversed so that it only shows lines that do not match the pattern. So, the command-line searches through the file and returns the lines that do not contain "and".
* `grep -v . non-fiction/OUP/Fletcher/ch2.txt`
  * This command returns <img width="1105" alt="Screen Shot 2023-02-12 at 11 56 06 AM" src="https://user-images.githubusercontent.com/122562172/218333888-e1fe9cec-ff70-431d-85a1-4486f85b0923.png">
  * In this command, `-v` is used once again, but this time there are no lines within the file that do not contain a ".". So, the terminal just returns a bunch of blank lines. 
* Researched using ChatGPT

#### 4. Only show matched portions using `-o` and `-b`
* `grep -o Investigations non-fiction/OUP/Kauffman/ch1.txt`
  * This command returns <img width="783" alt="Screen Shot 2023-02-12 at 12 04 25 PM" src="https://user-images.githubusercontent.com/122562172/218334291-b346741c-23e0-48b4-ab13-77175f6c857a.png">
  * In this command, `-o` is used to return only the matched portions of the line where a match is found. So, in this file there are 12 matches of "Investigations" and thus, it is returned 12 times. 
* `grep -o -b Investigations non-fiction/OUP/Kauffman/ch1.txt`
  * This command returns <img width="731" alt="Screen Shot 2023-02-12 at 12 07 10 PM" src="https://user-images.githubusercontent.com/122562172/218334456-bd0fdcea-eb08-4202-b02b-a6bb4f2fb2c7.png">
  * In this command, the same command as last time is used, except this time we add `-b` so that we can see the byte offset of each word. So, each word is returned with the ammount of bits that are between it and ths start of the file. 
 * Researched using ChatGPT
