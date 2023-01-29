# CSE15L Servers and Bugs
### **1. Creating StringServer**

* First, I had to create a web server called StringServer that uses the url to add strings to our StringServer. 

* The StringServer is supposed to work when a user uses the command `/add-message?s=<string>`

* This command adds the user-inputted string to our server and prints out the stored strings with each on a new line. 

* Here is the completed source code for this project: 

<img width="845" alt="Screen Shot 2023-01-29 at 11 55 34 AM" src="https://user-images.githubusercontent.com/122562172/215352395-eb0715a9-fe9e-4369-9f76-68d9c3ac40f6.png">

Examples of the server in use: 

<img width="536" alt="Screen Shot 2023-01-29 at 11 49 58 AM" src="https://user-images.githubusercontent.com/122562172/215352288-8f3cebae-2b32-4818-83d3-184c9c5d051d.png">

* In this image, the user inputs `/add-message?s=Server and Bugs`

  * The string `/add-message?s=Servers and Bugs` is then used to call the method `handleRequest(URI url)`
  
  * Since the url contains `/add-message` the program separates the query (`s=<string>`) into the `s` and the `Servers and Bugs`. The `Servers and Bugs` string is then stored into the `parameters` array.
  
  * Finally, the `stringsStored` String is updated to include the new string inputted by the user and the updated string is returned to the Web Server. 

<img width="524" alt="Screen Shot 2023-01-29 at 11 50 42 AM" src="https://user-images.githubusercontent.com/122562172/215352301-915a50ce-f100-4db0-909a-d790b3fb1a04.png">

* In this image, the user inputs `/add-message?s=By Carson Rae`

  * The string `/add-message?s=By Carson Rae` is then used to call the method `handleRequest(URI url)`
  
  * Since the url contains `/add-message` the program separates the query (`s=<string>`) into the `s` and the `By Carson Rae`. The `By Carson Rae` string is then stored into the `parameters` array. 
  
  * Finally, the `stringsStored` String is updated to include the new string inputted by the user and the updated string is returned to the Web Server. 

### **2. Bugs from Lab 3**

* 

### **3. What I've Learned**

* Over the last two weeks of this lab, I'm very happy that I went from having no idea how to make a web server to making them with ease. It's been really cool to apply something from my major to a real-life application. I can easily see how I could use HTML/CSS and Java to make a website on a web server from scratch. 
