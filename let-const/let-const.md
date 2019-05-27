
# Understanding let and const declerations.

Prior to ES5 varibles were decleared with the keyword var. Which was pretty good but has a down side. 
In Javascript when variables are decleared with the keyword var it places it in the global context with an initial value of undefined, until they are used before it assigns in original value to it.

```

function checkVar(value) {
  console.log(a) // a is available here as undefined

  if (value) {
    var a = 1;
    console.log(a); // outputs the actual value of a ie 1
  }
  else {
    console.log(a); // outputs undefined
  }
}

````

From the above you see that the a variable decleared is available in all scopes.

This down side has been solved with the use of the let and const keyword. This keywords are blocked scoped, that is the variables decleared with it are only available on their own scope.

```

function checkVar(value) {
  console.log(a) // syntax error a is not defined

  if (value) {
    let a = 1;
    console.log(a); // outputs the actual value of a ie 1
  }
  else {
    console.log(a); // syntax error a is not defined
  }
}

```

This is very useful and prevents buggy codes.

## USING THE LET KEYWORD
Now you understand why we need the let keyword but how exactly do we use the them?

Pretty straight forword the let keyword is used the same way as the var but the let does not allow for redeclearation of variables.

```
//Redeclearing the var variable

var number = 4;
console.log(number); // outputs 4;

var number = 5;
console.log(number); // outputs 5;

```


```
//Redeclearing the let variable 

let name = 'Charles';
console.log(name); // outputs Charles

let name = 'John';
console.log(name); //SyntaxError: Identifier 'name' has already been declared

```

As seen above the let variable created an error when we redecleared the name variable with it. Moreover the name variable can be reassigned.

```
//Reassigning the let variable 

let name = 'Charles';
console.log(name); // outputs Charles

name = 'John';
console.log(name); // outputs John

```

## USING THE CONST KEYWORD
The const keyword behaves similarly as the let keyword in that they are not available outside their scope. Just as the name sounds the const keyword are like constansts. Variables decleared with it can not be redecleared or reassigned.

```
// Redeclearing the const variable
const number = 5;
console.log(number);

const numnber = 7;
console.log(number); // SyntaxError: Identifier 'number' has already been      declared
```

```
// Reassigning the const variable
const name = 'Charles';
console.log(name); // outputs Charles

name = 'John';
console.log(name); // TypeError: Assignment to constant variable.
```

