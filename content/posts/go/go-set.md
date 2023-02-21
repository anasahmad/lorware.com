---
title: "Hash Set Implementation in Go"
date: 2023-02-19T23:13:16-06:00
draft: true
tags: ['Go']
---

### In logic building, hashsets are an important data structure used for many applications. Go, currently, doesn't have a hashset data type implementation


#### A HashSet can easily be implemented using map by defining the value field as a boolean

```
myset := map[T]bool{} 

//add
myset[value] = true

//contains/exists
valueFromSet, contains := myset[value]
if contains {

}

//remove
delete(myset, value)

//size
len(myset)

```

### Example Problem
#### Common problem - Find if an element exists in a list
##### if list contains apple, don't buy apple

```
fruitsInHouse := []string{"apple", "banana", "orange", "peach"}
// common solution - hint, it's inefficient! - O(n)
for _, fruit := range fruitsInHouse {
    if "apple" == fruit{
        //contains
    }
}
```

### Example Solution
##### Find if something exists in a set

```
fruitsInHouse := map[string]bool{"apple": true, "banana": true, "orange": true, "peach": true}
// this solution is O(1)
fruit, contains := fruitsInHouse["apple"]
```