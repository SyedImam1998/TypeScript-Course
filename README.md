# TypeScript-Course

- Typescript is a super set to Javascript.
- That simply means that it extends javascript.
- It builds up on javascript. And unlike javascript, typescript does not run in the browser. Instead, typescript has to be compiled to javascript so that it runs again.

#### Now, why would we then work with it?

Because typescript gives us as developer a better development experience and certain feature to do code, which only exists during development by which it still helps us write better code and avoid errors.

### Assigning Types:

#### Core Types:

1. Number - 1, 5.3, 10
2. String - "Hi Hello"
3. Boolean - true/false
4. Object - {age:20}
5. Array - [1,2,3]

```javascript
function add(n: number, m: number) {
  return n + m;
}
```

### Type Inference:

- Type inference is nothing but, Typescript will be able to understand what type of data it is And ide will show you all the supported methods or properties that the variable has.

```javascript
const button = document.querySelector("button");
button.addEventListner("click", () => {});

// Here ide will automatically show you the methods that button variable has.
```

### Type casting:

- If we, as developer, know with certainty know that something is of a certain type, we can use the special as keyword, which is added by typescript, to tell typescript that what we select here will be of that type.

```javascript
const num1= document.getElementById('num1')as HTMLINPUTELEMENT;

// before
num1.value /// error

//after
num1.value // No Value

// This was happening because Before typescript was not able to identify whether num1 has a value property or not.
```

### Configure typescript in your project

- Run this command. `tsc --init`

### Union Types:

- Now let's say we actually want to make add a bit more flexible. It should work with numbers, but it should also work with strings.

```javascript
function add(num: number | string, num2: number | string) : number | string  {
    return a+b;
}
```

### Using Object:

```javascript
function printResult(result:{val:number;timestamp:Date}){
    console.log(result.val)
}
```

### Using Arrays:

```javascript
const numArray:number[]=[];
const nameArray:String[]=[];
```
### Type Alias:

- when you have senario where you are using same types for different variables it is tedious task to write.

- Here we can use Type Alias.
```typescript
type NumOrString=number | string;

function addNum(n:NumOrString,n2:NumOrString){
    return n+n2
}
```
### Interfaces:

```typescript
interface ResultObj={
    val:number;
    timestamp:Date;
}

function printResult(result:ResultObj){
    console.log(result.val)
}
```
### What is the difference between types and interfaces



### Genrics:
