# ES6 Data Manipulation
**JavaScript ES6**

This project contains tasks for learning to manipulate data in ECMAScript 2015 (ES6).

## RESOURCES
+ [x] [Array](https://intranet.alxswe.com/rltoken/bcXqK1IaIHtrZ45sv0RxsQ)
+ [x] [Typed Array](https://intranet.alxswe.com/rltoken/YZ5RtzAPTaWtF00MYbXuVw)
+ [x] [Set Data Structure](https://intranet.alxswe.com/rltoken/Ch8vq39y9QnlTMr8CymgEg)
+ [x] [Map Data structure](https://intranet.alxswe.com/rltoken/W29MV3f8Ii4HmeJSALNIpw)
+ [x] [Weakmap](https://intranet.alxswe.com/rltoken/pSetFVFeIR660GPE0flPdg)  

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

* How to use map, filter and reduce on arrays
* Typed arrays
* The Set, Map, and Weak link data structures

## Requirements
* All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
* Allowed editors: vi, vim, emacs, Visual Studio Code
* All your files should end with a new line
* A README.md file, at the root of the folder of the project, is mandatory
* Your code should use the js extension
* Your code will be tested using Jest and the command npm run test
* Your code will be verified against lint using ESLint
* Your code needs to pass all the tests and lint. You can verify the entire project running npm run full-test
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
Install Jest, Babel, and ESLint
in your project directory, install Jest, Babel and ESList by using the supplied `package.json` and `run npm install`.

### Configuration files
Add the files below to your project directory

`package.json`
Click to show/hide file contents
`babel.config.js`
Click to show/hide file contents
`.eslintrc.js`
Click to show/hide file contents
### and…
Don’t forget to run `$ npm install` when you have the `package.json`

## Tasks

+ [x] 0. **Basic list of objects**<br/>[0-get_list_students.js](0-get_list_students.js) contains a script that exports a function named `getListStudents` with the following requirements:
  + Returns an array of objects.
  + Each object should have three attributes: `id` (Number), `firstName` (String), and `location` (String).
  + The array contains the following students in the order they're listed:
    + `Guillaume`, id: `1`, in `San Francisco`.
    + `James`, id: `2`, in `Columbia`.
    + `Serena`, id: `5`, in `San Francisco`.

+ [x] 1. **More mapping**<br/>[1-get_list_student_ids.js](1-get_list_student_ids.js) contains a script that exports a function named `getListStudentIds` with the following requirements:
  + Returns an array of ids from a list of object.
  + This function is taking one argument which is an array of objects - and this array is in the same format as the return value of `getListStudents` from the previous task.
  + If the argument is not an array, the function returns an empty array.
  + You must use the map function on the array.

+ [x] 2. **Filter**<br/>[2-get_students_by_loc.js](2-get_students_by_loc.js) contains a script that exports a function named `getStudentsByLocation` with the following requirements:
  + Returns an array of objects who are located in a specific city.
  + It should accept a list of students (from `getListStudents`) and a `city` (string) as parameters.
  + You must use the `filter` function on the array.

+ [x] 3. **Reduce**<br/>[3-get_ids_sum.js](3-get_ids_sum.js) contains a script that exports a function named `getStudentIdsSum` with the following requirements:
  + Returns the sum of all the student ids.
  + It should accept a list of students (from `getListStudents`) as a parameter.
  + You must use the `reduce` function on the array.

+ [x] 4. **Combine**<br/>[4-update_grade_by_city.js](4-update_grade_by_city.js) contains a script that exports a function named `updateStudentGradeByCity` with the following requirements:
  + Returns an array of students for a specific city with their new grade.
  + It should accept a list of students (from `getListStudents`), a `city` (String), and `newGrades` (Array of “grade” objects) as parameters.
  + `newGrades` is an array of objects with this format:
    ```js
    {
      studentId: Number,
      grade: Number,
    }
    ```

+ [x] 5. **Typed Arrays**<br/>[5-typed_arrays.js](5-typed_arrays.js) contains a script that exports a function named `createInt8TypedArray` with the following requirements:
  + Returns a new `ArrayBuffer` with an `Int8` value at a specific position.
  + It should accept three arguments: `length` (Number), `position` (Number), and `value` (Number).
  + If adding the value is not possible the error `Position outside range` should be thrown.

+ [x] 6. **Set data structure**<br/>[6-set.js](6-set.js) contains a script that exports a function named `setFromArray` with the following requirements:
  + Returns a `Set` from an array.
  + It accepts an argument (Array, of any kind of element).

+ [x] 7. **More set data structure**<br/>[7-has_array_values.js](7-has_array_values.js) contains a script that exports a function named `hasValuesFromArray` with the following requirements:
  + Returns a boolean if all the elements in the array exist within the set.
  + It accepts two arguments: a `set` (Set) and an `array` (Array).

+ [x] 8. **Clean set**<br/>[8-clean_set.js](8-clean_set.js) contains a script that exports a function named `cleanSet` with the following requirements:
  + Returns a string of all the set values that start with a specific string (`startString`).
  + It accepts two arguments: a `set` (Set) and a `startString` (String).
  + When a value starts with `startString` you only append the rest of the string. The string contains all the values of the set separated by `-`.

+ [x] 9. **Map data structure**<br/>[9-groceries_list.js](9-groceries_list.js) contains a script that exports a function named `groceriesList` with the following requirements:
  + Returns a map of groceries with the following items (name, quantity):
    ```cs
    "Apples", 10
    "Tomatoes", 10
    "Pasta", 1
    "Rice", 1
    "Banana", 5
    ```

+ [x] 10. **More map data structure**<br/>[10-update_uniq_items.js](10-update_uniq_items.js) contains a script that exports a function named `updateUniqueItems` with the following requirements:
  + Returns an updated map for all items with initial quantity at 1.
  + It should accept a map as an argument. The map it accepts for argument is similar to the map you create in the previous task.
  + For each entry of the map where the quantity is 1, update the quantity to 100. If updating the quantity is not possible (argument is not a map) the error `Cannot process` should be thrown.

+ [x] 11. **Weak link data structure**<br/>[100-weak.js](100-weak.js) contains a script that meets the following requirements:
  + Export a `const` instance of `WeakMap` and name it `weakMap`.
  + Export a new function named `queryAPI`. It should accept an endpoint argument like so:
    ```js
    {
      protocol: 'http',
      name: 'getUsers',
    }
    ```
  + Track within the `weakMap` the number of times `queryAPI` is called for each endpoint.
  + When the number of queries is >= 5 throw an error with the message `Endpoint load is high`.
