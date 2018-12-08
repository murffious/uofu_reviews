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
#### Commands to get us going  

  *Get a reference to the database service then use that reference to tap into or use the firebase built in methods to interact with the online db
`var database = firebase.database(); -- so the refrence variable database has all our methods built into it`

`.set({})` === Save values to the database or send/set data in firebase db, notice we send an object 
`.on("value")` === 
