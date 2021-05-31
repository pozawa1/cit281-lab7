# Objectives
1. Create your own GitHub organization for the CIT Minor
2. Create your first GitHub repository

# Technologies Used
- GitHub
- Terminal
- VSCode

# Part 1
Create your own GitHub organization for the CIT Minor. 

# Part 2
Create your first GitHub repository.

# Part 3
Clone your GitHub repository to your local system.

# Part 4
Create a new, empty file called lab-07.js in the cit281/p6/cit281-lab7 folder.

# Part 5
Update lab-07.js with the following:
- CustomError class that inherits from Error, where the class name property is "CustomError"
- Function throwGenericError() that uses throw to create a generic Error error, with the custom message of "Generic error"
- Function throwCustomError() that uses throw to create a custom CustomError error, with the custom message of "Custom error"
- A try..catch..finally block that forces the generic error by calling throwGenericError(), with console.log() debug statements
- A try..catch..finally block that forces the custom error by calling throwCustomError(), with console.log() debug statements

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

Output:

![lab7-07](https://user-images.githubusercontent.com/83732149/120248360-b7ebd380-c22b-11eb-9830-524d0ad54880.png)

# Part 6
Push your changes to GitHub.

![Screen Shot 2021-05-13 at 1 21 52 PM](https://user-images.githubusercontent.com/83732149/120248579-a0f9b100-c22c-11eb-9300-544e28ee4038.png)


