6 Basics
**JavaScript ES6**

## Concepts
For this project, we expect you to look at these concepts:

* [JavaScript programming](https://intranet.alxswe.com/concepts/852 "JavaScript programming")
* [Software Linter](https://intranet.alxswe.com/concepts/542 "Software Linter")

![](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2019/12/08806026ef621f900121.png)

## Resources
**Read or watch:**

* [ECMAScript 6 - ECMAScript 2015](https://www.w3schools.com/js/js_es6.asp "ECMAScript 6 - ECMAScript 2015")
* [Statements and declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements "Statements and declarations")
* [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions "Arrow functions")
* [Default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters "Default parameters")
* [Rest parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters "Rest parameter")
* [Javascript ES6 — Iterables and Iterators](https://towardsdatascience.com/javascript-es6-iterables-and-iterators-de18b54f4d4?gi=05ecd0b930cc "Javascript ES6 — Iterables and Iterators")

### Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

* What ES6 is
* New features introduced in ES6
* The difference between a constant and a variable
* Block-scoped variables
* Arrow functions and function parameters default to them
* Rest and spread function parameters
* String templating in ES6
* Object creation and their properties in ES6
* Iterators and for-of loops

## Requirements
**General**

* All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
* Allowed editors: `vi, vim, emacs, Visual Studio Code`
* All your files should end with a new line
* A `README.md` file, at the root of the folder of the project, is mandatory
* Your code should use the `js` extension
* Your code will be tested using the Jest Testing Framework [Jest Testing Framework](https://jestjs.io/ "Jest Testing Framework")
* Your code will be analyzed using the linter ESLint [ESLint](https://eslint.org/ "ESLint") along with specific rules that we’ll provide
* All of your functions must be exported

## Setup
### Install NodeJS 12.11.x
(in your home directory):
```
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```
```
$ nodejs -v
v12.11.1
$ npm -v
6.11.3
```

### Install Jest, Babel, and ESLint
In your project directory, install Jest, Babel and ESList by using the supplied `package.json` and run `npm install`.

## Configuration files
Add the files below to your project directory

`package.json`
Click here to show/hide file contents
`babel.config.js`
Click here to show/hide file contents
`.eslintrc.js`
Click here to show/hide file contents
**Finally…**
Don’t forget to run `npm install` from the terminal of your project folder to install all necessary project dependencies.

## Tasks

+ [x] 0. **Const or let?**<br/>[0-constants.js](0-constants.js) contains a script that meets the following requirements.
  + For the code below, make the following modifications:
    + function `taskFirst` to instantiate variables using `const`.
    + function `taskNext` to instantiate variables using `let`.
  ```js
  export function taskFirst() {
    var task = 'I prefer const when I can.';
    return task;
  }

  export function getLast() {
    return ' is okay';
  }

  export function taskNext() {
    var combination = 'But sometimes let';
    combination += getLast();

    return combination;
  }
  ```

+ [x] 1. **Block Scope**<br/>[1-block-scoped.js](1-block-scoped.js) contains a script that meets the following requirements.
  + For the code below, modify the variables inside the function `taskBlock` so that the variables aren't overwritten inside the conditional block.
  ```js
  export default function taskBlock(trueOrFalse) {
    var task = false;
    var task2 = true;

    if (trueOrFalse) {
      var task = true;
      var task2 = false;
    }

    return [task, task2];
  }
  ```

+ [x] 2. **Arrow functions**<br/>[2-arrow.js](2-arrow.js) contains a script that meets the following requirements.
  + For the code below, rewrite the following standard function to use ES6's arrow syntax of the function `add`.
  ```js
  export default function getNeighborhoodsList() {
    this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

    const self = this;
    this.addNeighborhood = function add(newNeighborhood) {
      self.sanFranciscoNeighborhoods.push(newNeighborhood);
      return self.sanFranciscoNeighborhoods;
    };
  }
  ```

+ [x] 3. **Parameter defaults**<br/>[3-default-parameter.js](3-default-parameter.js) contains a script that meets the following requirements.
  + For the code below, condense the internals of the following function to 1 line - without changing the name of each function/variable.
  ```js
  export default function getSumOfHoods(initialNumber, expansion1989, expansion2019) {
    if (expansion1989 === undefined) {
      expansion1989 = 89;
    }

    if (expansion2019 === undefined) {
      expansion2019 = 19;
    }
    return initialNumber + expansion1989 + expansion2019;
  }
  ```

+ [x] 4. **Rest parameter syntax for functions**<br/>[4-rest-parameter.js](4-rest-parameter.js) contains a script that meets the following requirements.
  + For the code below, modify the following function to return the number of arguments passed to it using the rest parameter syntax.
  ```js
  export default function returnHowManyArguments() {

  }
  ```

+ [x] 5. **The wonders of spread syntax**<br/>[5-spread-operator.js](5-spread-operator.js) contains a script that meets the following requirements.
  + For the code below, using spread syntax, concatenate 2 arrays and each character of a string by modifying the function below. The function body should be one line long.
  ```js
  export default function concatArrays(array1, array2, string) {
  }
  ```

+ [x] 6. **Take advantage of template literals**<br/>[6-string-interpolation.js](6-string-interpolation.js) contains a script that meets the following requirements.
  + For the code below, rewrite the return statement to use a template literal so you can the substitute the variables you’ve defined.
  ```js
  export default function getSanFranciscoDescription() {
    const year = 2017;
    const budget = {
      income: '$119,868',
      gdp: '$154.2 billion',
      capita: '$178,479',
    };

    return 'As of ' + year + ', it was the seventh-highest income county in the United States' \
          ', with a per capita personal income of ' + budget.income + '. As of 2015, San Francisco' \
          ' proper had a GDP of ' + budget.gdp + ', and a GDP per capita of ' + budget.capita + '.';
  }
  ```

+ [x] 7. **Object property value shorthand syntax**<br/>[7-getBudgetObject.js](7-getBudgetObject.js) contains a script that meets the following requirements.
  + For the code below, modify the following function’s `budget` object to simply use the keyname instead.
  ```js
  export default function getBudgetObject(income, gdp, capita) {
    const budget = {
      income: income,
      gdp: gdp,
      capita: capita,
    };

    return budget;
  }
  ```

+ [x] 8. **No need to create empty objects before adding in properties**<br/>[8-getBudgetCurrentYear.js](8-getBudgetCurrentYear.js) contains a script that meets the following requirements.
  + For the code below, rewrite the `getBudgetForCurrentYear` function to use ES6 computed property names on the `budget` object.
  ```js
  function getCurrentYear() {
    const date = new Date();
    return date.getFullYear();
  }

  export default function getBudgetForCurrentYear(income, gdp, capita) {
    const budget = {};

    budget[`income-${getCurrentYear()}`] = income;
    budget[`gdp-${getCurrentYear()}`] = gdp;
    budget[`capita-${getCurrentYear()}`] = capita;

    return budget;
  }
  ```

+ [x] 9. **ES6 method properties**<br/>[9-getFullBudget.js](9-getFullBudget.js) contains a script that meets the following requirements.
  + For the code below, rewrite `getFullBudgetObject` to use ES6 method properties in the `fullBudget` object.
  ```js
  import getBudgetObject from './7-getBudgetObject.js';

  export default function getFullBudgetObject(income, gdp, capita) {
    const budget = getBudgetObject(income, gdp, capita);
    const fullBudget = {
      ...budget,
      getIncomeInDollars: function (income) {
        return `$${income}`;
      },
      getIncomeInEuros: function (income) {
        return `${income} euros`;
      },
    };

    return fullBudget;
  }
  ```

+ [x] 10. **For...of Loops**<br/>[10-loops.js](10-loops.js) contains a script that meets the following requirements.
  + For the code below, rewrite the function `appendToEachArrayValue` to use ES6’s `for...of` operator. And don’t forget that `var` is not ES6-friendly.
  ```js
  export default function appendToEachArrayValue(array, appendString) {
    for (var idx in array) {
      var value = array[idx];
      array[idx] = appendString + value;
    }

    return array;
  }
  ```

+ [x] 11. **Iterator**<br/>[11-createEmployeesObject.js](11-createEmployeesObject.js) contains a script that meets the following requirements.
  + Write a function named `createEmployeesObject` that will receive two arguments:
    + `departmentName` (String).
    + `employees` (Array of Strings).
    ```js
    export default function createEmployeesObject(departmentName, employees) {

    }
    ```
    The function should return an object with the following format:
    ```php
    {
      $departmentName: [
        $employees,
      ],
    }
    ```

+ [x] 12. **Let's create a report object**<br/>[12-createReportObject.js](12-createReportObject.js) contains a script that meets the following requirements.
  + Write a function named `createReportObject` whose parameter, `employeesList`, is the return value of the previous function `createEmployeesObject`.
    ```js
    export default function createReportObject(employeesList) {

    }
    ```
  + `createReportObject` should return an object containing the key `allEmployees` and a method property called `getNumberOfDepartments`.
  + `allEmployees` is a key that maps to an object containing the department name and a list of all the employees in that department. If you’re having trouble, use the spread syntax.
  + The method property receives employeesList and returns the number of departments.

+ [x] 13. **Iterating through report objects**<br/>[100-createIteratorObject.js](100-createIteratorObject.js) contains a script that meets the following requirements.
  + Write a function named `createIteratorObject`, that will take into argument a report Object created with the previous function `createReportObject`.
    ```js
    export default function createIteratorObject(report) {

    }
    ```
  + This function will return an iterator to go through every employee in every department.

+ [x] 14. **Iterate through object**<br/>[101-iterateThroughObject.js](101-iterateThroughObject.js) contains a script that meets the following requirements.
  + Write a function named `iterateThroughObject`. The function’s parameter `reportWithIterator` is the return value from `createIteratorObject`.
    ```js
    export default function iterateThroughObject(reportWithIterator) {

    }
    ```
  + It should return every employee name in a string, separated by ` | `.
