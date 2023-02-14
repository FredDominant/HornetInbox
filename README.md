This app simulates a chat inbox.
To do this, a raw resource file has been created that acts as a data source for a service that returns data when a request is made to it. To request a page of data, call the getPage method in the DataFetcher object. Requesting a page of data will return a String with JSON formatting, containing a page number, and an array of Users which represent conversations in the clients inbox. Each page contains 10 User objects, and the data format can be seen in the data.txt file in the res/raw folder.

## Functionalities:
- Creates an app that retrieves inbox information in the form of individual conversations, and displays it in an inbox list. 
- Each conversation in the list is displayed with a profile picture, the user's name, and the last time a message was received.
- The profile picture consists of only an upper case letter that the user's name begins with. Every profile picture is uniquely identifiable, even when two users have the same Initial.
- The conversation data is paginated, and a new page should is only requested when it is going to be viewed by the user.

### To simulate the process of receiving a new message and updating the inbox list:
- A FAB that updates the "last_message_at" value of a random User to the current time is added. This process only needs to be performed for Users already added to the list. No need to fetch every unique User from the DataFetcher.
- The list animates smoothly during this process.
