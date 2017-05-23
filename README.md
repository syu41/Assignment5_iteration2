# Assignment5_team_41_iteration2
the function of the program intent to interpreter the Morse Code in to English word and sentence.
The Morse code is detected by a Arduion board with motion sensor.
The server determine the long motion as L, short motion as S, store a sequence of motion in a string, if the string match a English letter in the Morse table.
It will send the letter to html and empty the Morse code string.
The server using the time gap to determine whether a letter end and whether a word end, if a word end, the server will send a space to the HTML, and empty the string.
The client receive letter in sequence, and store the letter in a variable call word, and display the word in real time. 
If client received a space, then the client append the word variable to the sentence variable, and clean the word variable. 
The sentence variable also display in real time.
The new function implemented in the iteration 2 are following: 
1. client able to start/stop data transmission.
2. client able to display morse code for current word
3. server will stop when it received SK.
3. number and punctuation are supported by server.


bugs: null.

structure: this application has following structure, the client(HTML Page) is communicate with Server(app.js that control the Arduion board) via socket.io. the server using johnny-five library to make communication with Arduion board with motion sensor.

project layer:

user layer:HTML Page. 2. server layera node.js server that run app.js. 3. headware layer: Arduion board. 4. Data transmit layer: socket.io How to use: 1. user need to running a command "npm install" to get all necessary modules. 2. in the terminal input command "node app.js" to start running the server. 3. than open browser go to localhost:5000 to start using it. used packages: 1. node.js 2. johnny-five 3. Socket.io How to connect: 1. The LED light connect to pin 13. 2. The motion sensor connect to the pin 6, get power from Pin 5v.
