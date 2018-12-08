How to setup and initialize a new Firebase
`<script src="https://www.gstatic.com/firebasejs/4.12.0/firebase.js"></script>`
```<script>
    // Initialize Firebase
    // This is the code we copied and pasted from our app page
    var config = {
      apiKey: "AIzaSyAJS4YQWU5DmESeYueG1qH1NGkjv3DncEY",
      authDomain: "fir-click-counter-7cdb9.firebaseapp.com",
      databaseURL: "https://fir-click-counter-7cdb9.firebaseio.com",
      storageBucket: "fir-click-counter-7cdb9.appspot.com"
    };

    firebase.initializeApp(config);

    // Variables
    // ================================================================================

    // Get a reference to the database service
    var database = firebase.database();```
.set({})
.on("value")
