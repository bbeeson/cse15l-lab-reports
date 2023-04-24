# **Week 3 Lab Report**

## Servers and Bugs

## Part 1

### Code Screenshots
![Image](screenshots/Screenshot(393).png)
![Image](screenshots/Screenshot(394).png)

### /add-message screenshots
![Image](screenshots/Screenshot(395).png)
![Image](screenshots/Screenshot(396).png)

- Which methods in your code are called?
The methods 'main' and 'handleRequest' both get called in my code. I used the base from lab2 to make for the Stringserver section. This means that 'main' will start a server using the port number that was an input for when we are running and then 'handleRequest' will take the argument from the url for when we are using '/add-message'.

- What are the relevant arguments to those methods, and the values of any relevant fields of the class?
The relevant arguments to those methods are the port number choosen by the user, which for me was 8060, and the actual url of the server. The value of the field 'message' will update whenever our user changes the url with "/add-messages". I use handleRequest to get the path of the url then check if '/add-message' is present. When present the values of the 'parameters' var gets set by using the query split command which will basically set parameter to be to be an array that will hold two variables. If 'parameter[0]' is 's' , the left side of the '=' sign then it will add 'parameters[1]' to message.

- How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
'message' value will change whenever there's a message, whereas 'parameters' only changes if the element after our '=' gets changed. 

## Part 2

## Part 3
- Something I learned in lab 2 is actually running a server from vscode on your local machine. I knew of it but didn't know how to properly get the code to work. So it was very interesting to see it in action and play around with it. 