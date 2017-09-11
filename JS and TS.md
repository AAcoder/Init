Javascript
Typescript - Web can't directly use .ts files, so .ts files need to converted into .js which is done by ts transpiler.

// Transpiler converts code from 1 language to other.
// Compiler converst code to assembly code.

npm - Node Package Manager to install javascript packages like Typescript, Angular etc.
webpack

ajax - JS Interacting with server to get/post data without reloading of page. XMLHttpRequest 

jquery - JS library

JS - https://javascript30.com/

https://github.com/bmorelli25/Become-A-Full-Stack-Web-Developer#learn-javascript

## Starting Typescript project in Visual Studio Code
https://code.visualstudio.com/docs/editor/tasks

1. Create project folder myproject
    mkdir myproject
    cd myproject

2. Run **'tsc --init'** --> This will create **tsconfig.json** file , which tells about details of typescipt against which it will compile

3. Create file **'settings.json'** with below contents in path - myproject/.vscode
{
    "typescript.tsdk": "C:/Users/abhiagg/AppData/Roaming/npm/node_modules/typescript/lib/"
}

4. Add index.ts file.

5. Run the build using **Ctrl+Shift+B** gives option **tsc:build -tsconfig.json** --> Will create the index.js

6. To avoid selecting task, under Tasks tab, configure new defaut task -> which will create **tasks.json**

Tasks.json-  
{  
    // See https://go.microsoft.com/fwlink/?LinkId=733558  
    // for the documentation about the tasks.json format  
    "version": "2.0.0",  
    "tasks": [  
        {  
            "type": "typescript",  
            "tsconfig": "tsconfig.json",  
            "group": {  
                "kind": "build",  
                "isDefault": true  
            }  
        }  
    ]  
}  

### 1. Accessing the dom elements
    const cc = document.querySelector('.mf-section-1');
    const ac = cc.querySelectorAll('dd a');
    #### querySelector, querySelectorAll, getElementsByClassName, getElementById, getElementsByTagName

### 2. Manipulating dom elements
    document.getElementById("abc").style.color = "blue";
    document.getElementById("abc").style.backgroundColor = "blue";
    document.getElementById("abc").innerText = "hello";'
    document.getElementById("abc").innerHTML = "<b>hello</b>";

### 3. Ajax/ Fetching the data over internet
    const cities = [];
    fetch('https://gist.githubusercontent.com/Miserlou/c5cd8364bf9b2420bb29/raw/2bf258763cdddd704f8ffd3ea9a3e81d25e2c6f6/cities.json').
    then(x=> x.json()).
    then(data => cities.push(...data))
    
### 4. Array Object processing

	const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 }, ................. ]
	  
	// Array.prototype.filter()
    #### 1. Filter the list of inventors for those who were born in the 1500's
    const fifteen = inventors.**filter**(inventor => (inventor.year >= 1500 && inventor.year < 1600));

    // Array.prototype.map()
    #### 2. Give us an array of the inventor first and last names
    const fullNames = inventors.**map**(inventor => `${inventor.first} ${inventor.last}`);

    // Array.prototype.sort()
    #### 3. Sort the inventors by birthdate, oldest to youngest
    const ordered = inventors.**sort**((a, b) => a.year > b.year ? 1 : -1);

    // Array.prototype.reduce()
    // 4. How many years did all the inventors live?
    const totalYears = inventors.**reduce**((total, inventor) => {
      return total + (inventor.passed - inventor.year);
    }, 0);

    // 5. Sort the inventors by years lived
    const oldest = inventors.**sort**(function(a, b) {
      const lastInventor = a.passed - a.year;
      const nextInventor = b.passed - b.year;
      return lastInventor > nextInventor ? -1 : 1;
    });

    // 6. create a list of Boulevards in Paris that contain 'de' anywhere in the name
    // https://en.wikipedia.org/wiki/Category:Boulevards_in_Paris

    // const category = document.querySelector('.mw-category');
    // const links = Array.from(category.querySelectorAll('a'));
    // const de = links
    //             .map(link => link.textContent)
    //             .filter(streetName => streetName.includes('de'));

    // 7. sort Exercise
    // Sort the people alphabetically by last name
    const alpha = people.sort((lastOne, nextOne) => {
      const [aLast, aFirst] = lastOne.split(', ');
      const [bLast, bFirst] = nextOne.split(', ');
      return aLast > bLast ? 1 : -1;
    });

    // 8. Reduce Exercise
    // Sum up the instances of each of these
    const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck', 'pogostick'];

    const transportation = data.reduce(function(obj, item) {
      if (!obj[item]) {
        obj[item] = 0;
      }
      obj[item]++;
      return obj;
    }, {});

	9.  // Some and Every Checks
    // Array.prototype.some() // is at least one person 19 or older?
    // Array.prototype.every() // is everyone 19 or older?

	const isAdult = people.**some**(person => ((new Date()).getFullYear()) - person.year >= 19);
	const allAdults = people.**every**(person => ((new Date()).getFullYear()) - person.year >= 19);

    10. // Array.prototype.find()
    // Find is like filter, but instead returns just the one you are looking for
    // find the comment with the ID of 823423

    const comment = comments.**find**(comment => comment.id === 823423);
	
    11. // Array.prototype.**findIndex**()
    // Find the comment with this ID
    // delete the comment with the ID of 823423
    const index = comments.findIndex(comment => comment.id === 823423);
	
	
Typescript

