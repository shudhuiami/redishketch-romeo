# Redishketch-romeo (HTTP Request module)

Simple and user friendly request plugin. Based on pure Javascript. 
fast, user-friendly, customisable,

#Vue.js

[Redishketch-romeo](https://www.npmjs.com/package/redishketch-romeo) was created to use in vue.js 2.0 


# Getting started

### Installation

#### Quick Start with GIT with [Documentation](https://github.com/shudhuiami/redishketch-romeo)
```
git clone https://github.com/shudhuiami/redishketch-romeo.git
```


#### Quick Start with NPM
* Install with [NPM](https://www.npmjs.com/package/redishketch-romeo) ```npm install redishketch-romeo```

### Usage

POST method
```
function submitform(event) {
        event.preventDefault();
        var el = event.currentTarget;
        new resources({
            url: "http://localhost/redishketch-romeo/testServer/post.php",
            method: "POST",
            el: el,
            data: {
                user: "amieami",
                pass: "12345"
            },
            onSuccess: function (response) {
                console.log(response);
                document.getElementById('simple_element').innerHTML = response;
            }
        });
    }
```

GET method
```
function submitform(event) {
       new resources({
                   url: "http://localhost/redishketch-romeo/testServer/get.php",
                   method: "GET",
                   onSuccess: function (response) {
                       console.log(response);
                       document.getElementById('getresult_fild').innerHTML = response;
                   }
       });
    }
```

#Vue.js Usage

Import in Project
```
import 'redishketch-romeo'
```

than call under any function 
 ####Example
 ```
 created(){
 new resources({
     url: "API/URL goes here",
     method: "GET",
     onSuccess: function (response) {
                console.log(response);
        }
     });
 }
 ```
 
 ```
 created(){
 var el = 'form/input';
 new resources({
     url: "API/URL goes here",
     method: "POST",
     el: el,
     data: {
        user: "amieami",
        pass: "12345"
     },
     onSuccess: function (response) {
     console.log(response);
     }
 }
 ```


