# CSE15L Servers and Bugs
### **1. Creating StringServer**

* First, I had to create a web server called StringServer that uses the url to add strings to our StringServer. 

* The StringServer is supposed to work when a user uses the command `/add-message?s=<string>`

* This command adds the user-inputted string to our server and prints out the stored strings with each on a new line. 

* Here is the completed source code for this project: 

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler{
    
    String stringsStored = "";
    int num = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("String Server");
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    if (num == 0) {
                        stringsStored = String.format("%s", parameters[1]);
                    } else {
                        stringsStored = String.format("%s%n%s",stringsStored, parameters[1]);
                    }
                    num++;
                    return stringsStored;
                }
            }        
            return String.format("404 Not found!");
        }
    }
}
    class StringServer {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 to 49151");
                return;
            }
    
            int port = Integer.parseInt(args[0]);
    
            Server.start(port, new Handler());
        }
}
```

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

* `reverseInPlace()` is a method that had a bug. 

* When the following junit test is run, the first half of the array is reversed, however the second half uses the same values as before the reverse. 
  
  ```
  int[] input2 = {3, 5, 9, 13, 1};
  ArrayExamples.reverseInPlace(input2);
  assertArrayEquals(new int[]{1, 13, 9, 5, 3}, input2);
  ```
  
* The array would then be `{1, 13, 9, 13, 1}` as shown below. 

<img width="1019" alt="Screen Shot 2023-01-29 at 5 59 12 PM" src="https://user-images.githubusercontent.com/122562172/215372073-e1b6b9c4-30fd-455a-bc28-ad3d9d52bc5e.png">

* But, we need to be careful when testing, because an input array such as `{1, 3, 3, 1}` would produce the correct output. Even though the code contains a bug. As shown below the test is passed. 

<img width="554" alt="Screen Shot 2023-01-29 at 6 01 40 PM" src="https://user-images.githubusercontent.com/122562172/215372327-22467b5d-a5ed-49ae-8089-d3898e5f7ae4.png">

* Here is the code before while it contains the bug: 

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i++) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```

* In order to fix the method, we need to add a temporary array that will prevent the program from reversing the array while getting values from the array. 

* Here is the fixed program without the bug. 

```
static void reverseInPlace(int[] arr) {
    int[] temp = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      temp[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i++) {
      arr[i] = temp[i];
    }
}
```

### **3. What I've Learned**

* Over the last two weeks of this lab, I'm very happy that I went from having no idea how to make a web server to making them with ease. It's been really cool to apply something from my major to a real-life application. I can easily see how I could use HTML/CSS and Java to make a website on a web server from scratch. 
