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
  














