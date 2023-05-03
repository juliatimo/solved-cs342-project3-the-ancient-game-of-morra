Download Link: https://assignmentchef.com/product/solved-cs342-project3-the-ancient-game-of-morra
<br>
Morra is a hand game that dates back thousands of years. The rules are simple. If a two player game, each player (at the same time) must reveal their hand holding out zero to five fingers; at the same time, they must call out their guess about how many fingers total will be revealed by both players. If a player guesses correctly, they win a point. If both players guess correctly, no points are awarded. If no one guesses correctly, no points are awarded. The total number of points to win is determined before the game starts.

Your implementation will be a two player game where each player is a separate client and the game is run by a server. Your server and clients will use the same machine; with the server choosing a port on the local host and clients knowing the local host and port number (just as was demonstrated in class). Games will be played until one of the players has two points. At the end of each game, each user will be able to play again or quit.

All networking must be done utilizing Java Sockets (as shown in class). <strong>The server must  run on its own thread and handle each client on a separate thread.</strong> <strong>Each client must connect and communicate with the server on a separate thread</strong>. You may not use libraries or classes not included in the standard Java 8 release. <strong>You may work in teams of two but do not have to. </strong>

<strong>Implementation Details:</strong>

You will create two separate programs, each with a GUI created in JavaFX,  one for the server and one for the client. Use the Maven templates provided.

<strong><u>For the server GUI:</u></strong>

<ul>

 <li>A way to chose the port number to listen to- Have a button to turn on the server.</li>

 <li>Display the state of the game(you can display more info, this is the minimum):</li>

 <li>how many clients are connected to the server.</li>

 <li>what each player played.</li>

 <li>how many points each player has.</li>

 <li>if someone won the game.</li>

 <li>are they playing again.</li>

 <li>Any other GUI elements you feel are necessary for your implementation.</li>

</ul>

Notes: Your server GUI must have a minimum of two scenes: an intro screen that allows the user to input the port number and start the server and another that will display the state of the game information. To display the game information, you must incorporate a listView (as seen in class) with any other widgets used. Keep in mind, you can dynamically add items to the listView without using an ArrayList. <strong><u>For the server logic:</u></strong>

<ul>

 <li>It will only allow a game to start if there are two clients connected.</li>

 <li>It will notify a client if they are the only one connected.</li>

 <li>It will keep track of what each player played.</li>

 <li>It will evaluate who won each each round.</li>

 <li>It will evaluate if a client has won the game.</li>

 <li>It will update each client with the above items in time.</li>

 <li>It will do all things necessary to run the game.</li>

</ul>

It is expected that your server code will open, manage and close all resources needed and handle all exceptions in a graceful way. For game play, each client will send the server the number they are playing (0-5) and their total guess. The server will determine who if anybody receives points and then update each client with what the other played, guessed and the resulting state of the game.

If a client has won the hand and has reached two points, the server will send what the other player played and guessed, the resulting state of the game and require each client to make a choice as to play again or quit. If a player quits, the server will end that connection. If one player quits and the other wants to play again, the server will notify the client that they must wait for another person to connect. If both want to play again, the server will start a new game. <strong><u>For the client GUI:</u></strong>

<ul>

 <li>A way for the user to enter the port number and ip address to connect to – A button to connect to the server.</li>

 <li>A way to display the points each player has.</li>

 <li>A way to display what the opponent played each round using images.</li>

 <li>A way to display what the opponent guessed each round.</li>

 <li>Clickable images to choose what to play.</li>

 <li>A way to make a guess on total played.</li>

 <li>A way to display messages from the server.</li>

 <li>Buttons to choose to play again or quit.</li>

 <li>Any other GUI elements you feel are necessary for your implementation.</li>

</ul>

Notes: Your client GUI must have a minimum of three scenes: an intro screen that allows the user to input the port number and ip address to connect to the server,  another that will display the state of the game information and game play and a third of your choice. To display the game information, you must incorporate a listView (as seen in class) with any other widgets used. Keep in mind, you can dynamically add items to the listView without using an ArrayList. Buttons should be disabled when not in use or when waiting for a response from the server.

<strong><u>For the client logic:</u></strong>

After entering the port number and ip address, the user will click to connect to the server. When the server notifies that there is another client to play, the game will start. The user will select what number to play and their total number guess and send to the server. The server will respond with what the opponent played and guessed, who won and what points were distributed. The client GUI will update with this information and allow the user to either keep playing or, if someone has won, chose to either play again or quit. Quit will end the client program. It is expected that your client code will open, manage and close all resources needed and handle all exceptions in a graceful way.

<strong>Passing info between clients and server:</strong>

<strong>You must implement the MorraInfo class. </strong><strong>class MorraInfo implements Serializable{}</strong>

<strong>You will add serializable data members to this class that keep track of the state of the game( i.e. int p1Points, int p2Points, String p1Plays, String p2Plays     , Boolean have2players…..). This class will be used to send information back and forth between the server and two clients. This is the only way you are allowed to send and receive information. </strong>

<strong>Testing Code: </strong>

You are required to include JUnit 5 test cases for your program. Add these to the src/test/java directory of your Maven Project.

<strong>UML Class Diagrams: </strong>

You are required to create a UML Class Diagram for the server and client programs; including all classes, data members and methods of those classes, interfaces and interactions between them. Format these as PDFs.

<strong>Use of templates found on the web:</strong>

You may use ideas from templates( fxml, css or other) for styling your programs found on the web. You may not import those templates and pass them off as your own work. If you use an idea or part of such template, include a reference to that work in the header of the file where used. Failure to do this will result in academic misconduct charges.