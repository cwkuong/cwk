## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/cwkuong/cwk/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
<!-- The core Firebase JS SDK is always required and must be listed first -->
<script src="https://www.gstatic.com/firebasejs/8.1.1/firebase-app.js"></script>

<!-- TODO: Add SDKs for Firebase products that you want to use
     https://firebase.google.com/docs/web/setup#available-libraries -->
<script src="https://www.gstatic.com/firebasejs/8.1.1/firebase-analytics.js"></script>

<script>
  // Your web app's Firebase configuration
  // For Firebase JS SDK v7.20.0 and later, measurementId is optional
  var firebaseConfig = {
    apiKey: "AIzaSyCHQoEswTK8iScog1zSB1TJZY2qzhCAetM",
    authDomain: "abc-machining-dept-ddf69.firebaseapp.com",
    databaseURL: "https://abc-machining-dept-ddf69.firebaseio.com",
    projectId: "abc-machining-dept-ddf69",
    storageBucket: "abc-machining-dept-ddf69.appspot.com",
    messagingSenderId: "112366304898",
    appId: "1:112366304898:web:5b0559937536079e153e9b",
    measurementId: "G-H3TMYZ29VV"
  };
  // Initialize Firebase
  firebase.initializeApp(firebaseConfig);
  firebase.analytics();
</script>

// https://medium.com/firebase-developers/using-firebase-to-control-your-arduino-project-over-the-web-ba94569d172c
// Write data to Firebase
//var mac = '30:AE:A4:1B:58:A0';
//// Get a reference to the Firebase database entry at the given key.
//var dbRef = firebase.database().ref('config/' + mac);
//// The config object we want to write.
//var config = {
  //name: 'Device name',
  //red: 100,
  //green: 0,
  //blue: 100,
  //brightness: 50,
//};
//// Write the config to the database.
//dbRef
  //.set(config)
  //.then(function() {
    //console.log('Success!');
  //})
  //.catch(function(error) {
    //console.log('Error: ' + error.message);
  //});

// Read data from Firebase
// Get a database reference to all config/ keys.
dbRef = firebase.database().ref('config/');   
// Set callback to be invoked when a child node is added or changes.
dbRef.on('child_added', configChanged, dbErrorCallback);    
dbRef.on('child_changed', configChanged, dbErrorCallback);
// Callback invoked when database entry is added or changed.
function configChanged(snapshot) {
  var key = snapshot.key;
  var newValue = snapshot.val();
  console.log('Database entry ' + key + ' changed, new value: ' +
    newValue);
}
// Callback invoked on error.
function dbErrorCallback(err) {
  console.log('Error reading database: ' + err.message);
}

```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/cwkuong/cwk/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
