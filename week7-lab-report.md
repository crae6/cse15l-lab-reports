# CSE Labs "Done Quick"

### 1. Log into ieng6
* <img width="794" alt="Screen Shot 2023-02-23 at 11 28 45 AM" src="https://user-images.githubusercontent.com/122562172/221373867-c8757c4d-9ea3-4036-8342-4fb2a76a9545.png">
* `<Ctrl-R> "ssh" <enter>`
* Since we created an SSH key earlier in the lab, we are able to login to ieng6 without typing in our password. 

### 2. Clone your fork of the repository from your Github account
* <img width="566" alt="Screen Shot 2023-02-25 at 10 43 03 AM" src="https://user-images.githubusercontent.com/122562172/221374238-e0cb4acf-2109-4e73-921a-7737e14c5185.png">
* `<Ctrl-R> "git cl" <enter>`
* `<Ctrl-R>` searches our command history for commands containing "git cl". Since we've used git previously for other commands (e.g. "git commit", "git push", etc.) we need to type the "cl" to specify we are looking for the clone command. 
  
### 3. Run the tests, demonstrating that they fail
* <img width="971" alt="Screen Shot 2023-02-25 at 10 59 57 AM" src="https://user-images.githubusercontent.com/122562172/221374915-17d454ad-96d0-481c-aa85-73ce6ac3fda4.png">
* `<Ctrl-R> "javac" <enter>`
* `<Ctrl-R> "java " <enter>`
* `<Ctrl-R>` searches for our previous java commands. We need to specify whether it's "javac" or "java ".

### 4. Edit the code file to fix the failing test
* <img width="920" alt="Screen Shot 2023-02-23 at 11 30 51 AM" src="https://user-images.githubusercontent.com/122562172/221375660-ea0027c0-43c2-4bca-a363-2674a26ae480.png">
* `<Ctrl-R> "nano" <enter>`
* `<Ctrl-Shift> <-> "43, 13" <enter> <delete> "2"`
* `<Ctrl-O> <enter> <Ctrl-X>`
* First, we search using `<Ctrl-R>` to open up nano. Then, using the line and column search command `<Ctrl-Shift> <->` we go to the exact line and column that we need to change. Finally, to exit nano we need to press `<Ctrl-O> <enter> <Ctrl-X>`.

### 5.Run the tests, demonstrating that they now succeed
* <img width="961" alt="Screen Shot 2023-02-23 at 11 29 56 AM" src="https://user-images.githubusercontent.com/122562172/221376085-6630e9ce-f533-4834-94e1-33263fdc3135.png">
* `<Ctrl-R> "javac" <enter>`
* `<Ctrl-R> "java " <enter>`
* Here, we just use the same technique that we did to previously run and check that the tests failed. However, this time the tests passed. 

### 6. Commit and push the resulting change to your Github account
* <img width="502" alt="Screen Shot 2023-02-23 at 11 37 14 AM" src="https://user-images.githubusercontent.com/122562172/221376152-18962e99-3ae5-4a6f-9858-32dede92c044.png">
* `<Ctrl-R> "git a" <enter>`
* `<Ctrl-R> "git co" <enter>`
* `<Ctrl-R> "git p" <enter>`
* Because we have previously called "git add", "git commit", and "git push". We can use `<Ctrl-R>` to search for each one. 
