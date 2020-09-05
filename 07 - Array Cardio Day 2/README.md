# 07 - Array Cardio Day 2

* `some()`: reutrun true when at least one element in the array pass the test provided by function.
```
    const isAdult = people.some((person) => (new Date()).getFullYear() - person.year >= 19)
    console.log(isAdult)
```

* `every()`: return true when all elements in the array pass the test provided by function.
```
    const isAllAdult = people.every((person) => (new Date()).getFullYear() - person.year >= 19)
    console.log(isAllAdult)

```

* `find()`: returns the value of the first element in the provided array that satisfies the provided testing function.
```
    const comment = comments.find((comment) => comment.id === 823423)
    console.log(comment)
```

* `findIndex()`: returns the index of the first element in the array that satisfies the provided testing function. Otherwise, it returns -1, indicating that no element passed the test.
```
    const index = comments.findIndex((comment) => comment.id === 823423)
    console.log(index)
```

* `splice()`: changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
```
    const conmentsSplice = comments.splice(index, 1);
    console.log(comments)
```

* `slice()`: returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. ***The original array will not be modified.***
```
    const newComments = [
      ...comments.slice(0, index),
      ...comments.slice(index + 1)
    ];
    console.log(newComments)
```