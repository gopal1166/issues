# issues

### 1) React build fail: Blank screen after build

Sol: 
```
1.use HashRouter instead of BrowserRouter
2."homepage": "." in package.json at the top
3.Make sure used <Link > instead of <a > tag
```

### 2) app not working on ie, edge

in package.json:
```
"development": [
      "ie 11",
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
   ```
   
 Add the below code in index.js in the src folder
 ```
 // These must be the first lines in src/index.js
import 'react-app-polyfill/ie11';
import 'react-app-polyfill/stable';
```

Then delete the node_modules folder and run
```
npm install
```

[Stack Overflow](https://stackoverflow.com/questions/56421417/react-app-not-working-in-internet-explorer-11)


