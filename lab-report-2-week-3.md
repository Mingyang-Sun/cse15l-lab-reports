# Lab Report 2 - Week 3 Lab Report

## Part 1 Search Engine:

### The code for the Simplest “Search Engine”
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler
{
    ArrayList<String> list = new ArrayList<>();

    public String handleRequest(URI url)
    {
        if (url.getPath().equals("/"))
        {
            return "No action";
        } 
        else
        {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) 
            {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s"))
                {
                    list.add(parameters[1]);
                    return String.format("%s has been added", parameters[1]);
                }
            }
            else if (url.getPath().contains("/search"))
            {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s"))
                {
                  String empty = "";  
                  for (String e : list)
                  {
                    if (e.contains(parameters[1]))
                    {
                      empty += e;
                      empty += " ";
                    }
                  }
                  return empty;
                }
            }
            return "404 Not Found!";
        }
    }
}

class SearchEngine
{
    public static void main(String[] args) throws IOException
    {
        if(args.length == 0)
        {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

### 1. Adding an apple
![Image](images/Lab%20Report%202%201.1.png)
The method in my code that has been called is the public String handleRequest(URI url) method.

The relevant argument for this method is the url that passed as an input. The value of the url will be decided by the users. At this point, the value of url would be “/add?s=apple”.

The relevant fields of the class are an ArrayList called list that keeps track of input strings, a string array called parameters that stores the values split from the input query, and a string called empty that would keep track of outputs if a search operation has been requested.
At this point, the list field would be empty but later will be added with the string “apple”, and the parameters field would be assigned with string “s” at index 0 and string “apple” at index 1. The empty field would remain empty since no search operation has been requested.

By the time request is done processing, the values of the relevant fields of the class would remain what has been assigned during the request. However, if another request has been called, those values would be changed based on new inputs and requests.

### 2. Adding a pineapple
![Image](images/Lab%20Report%202%201.2.png)
The method in my code that has been called is the public String handleRequest(URI url) method.

The relevant argument for this method is the url that passed as an input. The value of the url will be decided by the users. At this point, the value of url would be “/add?s=pineapple”.

The relevant fields of the class are an ArrayList called list that keeps track of input strings, a string array called parameters that stores the values split from the input query, and a string called empty that would keep track of outputs if a search operation has been requested.
At this point, the list field would have one string “apple” stored and later will be added with the string “pineapple”, and the parameters field would be assigned with string “s” at index 0 and string “pineapple” at index 1. The empty field would still remain empty since no search operation has been requested yet.

By the time request is done processing, the values of the relevant fields of the class would remain what has been assigned during this request. However, if another request has been called, those values would be changed based on new inputs and requests.

### 3. Searching/Querying for substring "app"
![Image](images/Lab%20Report%202%201.3.png)
The method in my code that has been called is the public String handleRequest(URI url) method.

The relevant argument for this method is the url that passed as an input. The value of the url will be decided by the users. At this point, the value of url would be “/search?s=app”.

The relevant fields of the class are an ArrayList called list that keeps track of input strings, a string array called parameters that stores the values split from the input query, and a string called empty that would keep track of outputs if a search operation has been requested.
At this point, the list field would have two strings “apple” and “pineapple” stored, and the parameters field would be assigned with string “s” at index 0 and string “app” at index 1. The empty field would remain empty for now but later added with the values of string “apple” and “pineapple”.

By the time request is done processing, the values of the relevant fields of the class would remain what has been assigned during this request. However, if another request has been called, those values would be changed based on new inputs and requests.

## Part 2 Bugs and Symptoms:
