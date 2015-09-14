# README #

### What it's for ###
Save data from a Contentful space to a local JSON file

### How to use it ###

1. Install with NPM

```
#!javascript

npm install contentful-static --save-dev
```

2. Add Javascript

```
#!javascript

// Include
var contentfulStatic = require('contentful-static');

// Configure
contentfulStatic.config({
    // Destination path to save JSON data in (relative to app root):
    dest: 'src/data/contentful.json',
    // Your Contentful space ID
    space: 'my12space34id',
    // Contentful Access Token
    accessToken: '5fdae8a3myacc3sst0ken573962'
});

// Run
contentfulStatic.sync(function(err) {
    if(err) {
        console.log('contentful-static: data could not be synced');
        return false;
    }
    console.log('contentful-static: data stored successfully!');
});
```