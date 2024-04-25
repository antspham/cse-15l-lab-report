Part One
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String messages = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return messages;
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            messages += parameters[1].split("=")[1] + ": " + parameters[0].split("=")[1] + "\n";
            return messages;
        }
            return "404 Not Found!";
    }
}

class MessageServer {
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

![Screenshot (14)](https://github.com/antspham/cse-15l-lab-report/assets/165956921/e32fe4aa-5062-4db2-ba33-3db06fdbf748)
![Screenshot (15)](https://github.com/antspham/cse-15l-lab-report/assets/165956921/2b09949b-7dea-479a-85d9-bd30afcd4cef)
The only method I used is called handleRequest. I took it from the github files provided at lab two and adjusted the code accordingly.
The only relevant argument to handleRequest is the url.
The values that got changed from this specific request is that rather than recording the incrementation of a number from lab two this method now records the messages added by a specific user.

Part Two
![Screenshot (11)](https://github.com/antspham/cse-15l-lab-report/assets/165956921/881b1333-dbf4-427c-808f-5a87c6bd3aa3)
![Screenshot (12)](https://github.com/antspham/cse-15l-lab-report/assets/165956921/5333fe3d-f0a2-403f-ae85-afa7b836c09a)
![Screenshot (13)](https://github.com/antspham/cse-15l-lab-report/assets/165956921/180f0264-7023-4623-a67b-3cf5142bb036)

Part Three
Something I learned from lab in week two was how servers and urls works especially how data can be stored depending on how the url is formatted. Something I learned from lab in week three was how easy it was to connect to a remote server although I am curious on how this can be applied practically. 
