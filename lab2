Code for Chat Server

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> chatMessages = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message") && url.getQuery() != null) {
            String[] params = url.getQuery().split("&");
            String user = null;
            String message = null;

            for (String param : params) {
                if (param.startsWith("user=")) {
                    user = param.substring(5);
                } else if (param.startsWith("s=")) {
                    message = param.substring(2);
                }
            }

            if (user != null && message != null) {
                chatMessages.add(user + ": " + message);
                return String.join("\n", chatMessages);
            } else {
                return "Invalid request. Missing user or message.";
            }
        }
        return "404 Not Found";
    }
}

class ChatServer {
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
