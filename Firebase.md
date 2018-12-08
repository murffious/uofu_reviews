#### How to setup and initialize a new Firebase
`<script src="https://www.gstatic.com/firebasejs/4.12.0/firebase.js"></script>` 
* put the line above in the index.html file and the code below in a javascript file (can put all in index.html file but not best practice for anything beyond tiny projects) - make sure to link your javascript file


```
    // Initialize Firebase
    // This is the code we copied and pasted from our app page for now we will use TEST mode when creating a new app
    var config = {
      apiKey: "AIzaSyAJS4YQWU5DmESeYueG1qH1NGkjv3DncEY",
      authDomain: "fir-click-counter-7cdb9.firebaseapp.com",
      databaseURL: "https://fir-click-counter-7cdb9.firebaseio.com",
      // Be sure to double check permissions under RULES tab and set read and write to true to do that click the database URl above
      storageBucket: "fir-click-counter-7cdb9.appspot.com"
    };

    firebase.initializeApp(config);
``` 
#### Commands to get us going - SO this code all goes right below the database initialization above

`var database = firebase.database();` -- so the refrence variable database has all our methods built into it.
`database.ref()` === use this before any of the following functionality and just "chain" on the next method with another `.` it just specifies where the data will be saved

`.set({})` === Save values to the database or send/set data in firebase db, notice we send an object 
`.on("value", function(){})` === effectively creates an "on-change" event so that the moment the page first loads or the moment the database changes, the impact is reflected immediately.
 database.ref().on("value", function(snapshot) {

      // Log everything that's coming out of snapshot
      console.log(snapshot.val());
`.push({})` 
`.on("child_added")`
database.ref().on("child_added", function(childSnapshot) {
  console.log(childSnapshot.val());
database.ref().on("child_added", function(snapshot) {

// 4. Create Firebase event for adding trains to the database and a row in the html when a user adds an entry
trainData.ref().on("child_added", function(childSnapshot, prevChildKey) {
  console.log(childSnapshot.val());
  dataRef.ref().orderByChild("dateAdded").limitToLast(1).on("child_added", function(snapshot) {
  
 #### Advanced for challenge HW
 if you want to do the challenge version RPS homework database.ref("/chat");
var playersRef = database.ref("players");
var currentTurnRef = database.ref("turn");
 
 playerRef.child("choice").set(clickChoice);
 
 `firebase.database.ServerValue.TIMESTAMP,`
 
 
 chatData.orderByChild("time").on("child_added", function(snapshot) {
 
 
 currentPlayers = snapshot.numChildren();

  // Check to see if players exist
  playerOneExists = snapshot.child("1").exists();
  playerTwoExists = snapshot.child("2").exists();

  // Player data objects
  playerOneData = snapshot.child("1").val();
  currentTurnRef.onDisconnect().remove();

    // Send disconnect message to chat with Firebase server generated timestamp and id of '0' to denote system message
    chatDataDisc.onDisconnect().set({
