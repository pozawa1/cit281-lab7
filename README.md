# Lab 7

## Objectives
1. Create your own GitHub organization for the CIT Minor
2. Create your first GitHub repository

## Technologies Used
- GitHub
- Terminal
- VSCode

## Source Code
```
class CustomError extends Error {
    constructor(args) {
        super(args);
        this.message = 'CustomError';
    }

    throwGenericError() {
        throw new Error("Generic error")
    }

    throwCustomError() {
        throw new CustomError().message;
    }
}
const myError = new CustomError();

console.log("Force generic error");
try {
    // try block
    console.log("Generic error try block");
    myError.throwGenericError();
} catch {
    console.log("Generic error catch block");
    console.log(myError.throwGenericError());
} finally {
    console.log("Generic error finally block");
}

console.log("Force custom error");
try {
    console.log("Custom error try block");
} catch {
    console.log("Custom error catch block");
    console.log(myError.throwCustomError());
} finally {
    console.log("Custom error finally block");
}
```

