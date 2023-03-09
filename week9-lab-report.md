# Researching Commands Pt. 2
### The `find` Command

#### All of these commands were discovered by asking ChatGPT in this prompt. 
<img width="500" alt="Screen Shot 2023-03-09 at 11 10 44 AM" src="https://user-images.githubusercontent.com/122562172/224130058-19c12c5d-5aaa-4f41-a2d8-9b45f791d588.png">
<img width="500" alt="Screen Shot 2023-03-09 at 12 50 46 PM" src="https://user-images.githubusercontent.com/122562172/224154622-cfaeabbb-82b8-4fc0-94ba-9d6877b9c7ab.png">


#### 1. Finding by name using `-name`
* `find . -name ch1.txt`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 11 19 11 AM" src="https://user-images.githubusercontent.com/122562172/224131757-54f3b071-9897-42f5-b846-888e51f0b55e.png">
  * In this command, `-name` is used to search for the specified name in all directories and subdirectories of the current file. In this instance, there are five ch1.txt's found so all five of them are returned with their file path.  
* `find . -name chZ.txt`
  *  This command returns <img width="900" alt="Screen Shot 2023-03-09 at 11 22 45 AM" src="https://user-images.githubusercontent.com/122562172/224132534-c596264e-aeac-4fa5-a313-c30a0e5d1a31.png">
  *  In this command, `-name` is once again used to search for the file chZ.txt. However, this time there is only one file with the matched name, so only one is returned.
* Researched using ChatGPT

#### 2. Finding files by type using `-type f -name`
* `find . -type f -name "*.class"`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 11 30 42 AM" src="https://user-images.githubusercontent.com/122562172/224134112-fc2a438f-c072-4015-a1d3-4d9c589030a1.png">
  * In this command, `-type` specifies that we are searching for a type, `f` specifies that we only want to search for files, `-name` once again specifies that we are searching by name.
* `find . -type d`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 45 03 PM" src="https://user-images.githubusercontent.com/122562172/224153237-a4f7abaa-0f42-4c18-8486-d0554a16dde3.png">
  * In this command, `-type` is used to specify that we are seaching for a type and `d` specifies that we are searching for directories.
  * Researched using ChatGPT

#### 3. Finding files by size using `-size`
* `find . -type f -size +200k`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 20 41 PM" src="https://user-images.githubusercontent.com/122562172/224146503-d3173e1b-9b34-4d75-a545-01eb1fd28f1f.png">
  * In this command, `-type` is used to specify that we are searching for a type, `f` specifies that we are searching for a file, and `-size` specifies that we are searching for a specific size of a file. Finally, `+200k` specifies that we only want files over 200 kilobytes. 
* `find . -type f -size -1k`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 26 02 PM" src="https://user-images.githubusercontent.com/122562172/224147624-ca38a673-bff8-488e-92eb-6806983d4017.png">
  * In this command, `size` is used once again, but this time we specify the size of the file with a `-1`. This specifies that instead of searching for fiels larger than our specified size, we are now searching for files smaller than the specified size. Since we don't put any parameter after `1`, this time we are only searching for files smaller than one byte. 
* Researched using ChatGPT

#### 4. Finding files by time since last modified using `-mtime`
* `find . -type f -mtime -7`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 32 18 PM" src="https://user-images.githubusercontent.com/122562172/224149584-4ba00a86-b27c-4a2e-aa0c-c32e75c9951a.png">
  * In this command, `-type` is used to specify that we are seaching for a type, `f` specifies that we are once again searching for a file type, `-mtime` specified that we are searching for a file that was modified within the specific time, and `-7` specifies that we are looking for a file modified less than 7 days ago. 
* `find -type f -mtime +1 -mtime -28`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 39 36 PM" src="https://user-images.githubusercontent.com/122562172/224151912-307c9672-a91f-4bd0-b9b6-32f779365ce0.png">
  * In this command, we use `-mtime` twice to specify that we only want files that were modified more than 1 day ago and less than 28 days ago. 
 * Researched using ChatGPT

#### 5. Finding files and executing a command on them using `-exec`
* `find . -name "chZ.txt" -exec cat {} \;`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 12 53 49 PM" src="https://user-images.githubusercontent.com/122562172/224155425-b2b4917a-6fdc-4587-a84c-749e88dfe4bb.png">
  * In this command, `-exec` tells the terminal that we are going to execute a command on the file(s) found. Then, `cat` prints out the contents of the file we have found. 
* `find . -name "chZ.txt" -exec head {} \;`
  * This command returns <img width="900" alt="Screen Shot 2023-03-09 at 1 01 51 PM" src="https://user-images.githubusercontent.com/122562172/224157069-1362c591-016b-41db-9749-dfe944b11f62.png">
  * In this command, `-exec` tells the terminal that we are going to execute a command on the file(s) found. Then, `head` prints out the contents of the first ten lines of the file. 
 * Researched using ChatGPT
