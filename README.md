### TypeScript
---
A basic TypeScript project consist in three main files:
* package.json
- tsconfig.json
* src/index.ts

#### <code>package.json</code>
```json
{
    
  "name": "hello-ts",
  "license": "NOLICENSE",
  "devDependencies": {
    "typescript": "^4.3.2" //typescript version
  },
  "scripts": {
    "dev": "tsc --watch --preserveWatchOutput"
}
}
```
> --watch: tells the TypeScript compiler to watch for changes to the .ts file and runs the transpiler on each change
This automatically recompile the code as we make changes to it

> --preserveWatchOutput: preserve the console outputs

<br>

#### <code>tsconfig.json</code>
Typescript compiler settings

```json
{
  "compilerOptions": {
    "outDir": "dist", // where to put the TS files
    "target": "ES3", // which level of JS support to target
    "declaration": true,
    // create two files on the compilation process
    //  inside the "outDir" set
    // - .js: contains all the code that runs
    // - .d.ts: contains all the types information
    "module": "CommonJS",
    // set the type of export modules use by node

    "moduleResolution": "nodenext"
    // to locate all the node_modules that the code needs to compile
  },
  "include": ["src"] // which files to compile
}
```

<br>

### **Variables and Values**
---
Variables are born with their types

TypeScript infers the type of a variable that is declared and initialized

So, age can containt any kind of number 
```ts
let age = 6
// let age: number = 6
```


When we declare a variable using the word <code>const</code>, we are creating a **literal type**


```ts
const number = 6;
```
The const declaration is one that can hold only 6, a specific number

<br>

### **<code>any</code> and type annotations**

TypeScript assigns the type <code>any</code> to a variable that is declared but not initialized yet

So, <code>endTime</code> born with the most flexible type: <code>any</code>
```ts
// between 500 and 1000
const RANDOM_WAIT_TIME =
  Math.round(Math.random() * 500) + 500
 
let startTime = new Date()
let endTime
// let endtime: any
       
setTimeout(() => {
  endTime = 0
  endTime = new Date()
}, RANDOM_WAIT_TIME)
```

<br>

### **Function arguments and return values**
---


<br>

### **Objects**
---


### type Guard
A if statement to analyze if a variable has a certain type  
Connects _buildtime validation_ with _runtime behavior_