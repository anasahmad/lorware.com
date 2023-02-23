---
title: "Data Types in Go"
date: 2023-02-20T14:12:55-06:00
tags: ['Go']
---

- bool
```
isEarthFlat := false

var isEarthFlat bool
isEarthFlat = false
```
- int --- int8, int16, int32, int64
#### Note: number after int refers to the number of bits for that type - e.g int8 means 8 bit int (+/- 2^8 - 1). int type is a signed integer with at least 32 bits size
```
temperature := -10
planets := 8

var noOfPlanets int
noOfPlanets = 8

var noOfEyes int8
noOfEyes = 3
```
- uint --- uint8, uint16, uint32, uint64
```
planets := 8

var noOfPlanets uint
noOfPlanets = 8

var noOfEyes uint8
noOfEyes = 3
```
- uintptr
- float --- float32, float64
#### Note: IEEE-754 floating-point numbers
```
temperature := -10.2

var height float32
height = 6.2042

var size float64
size = 4.23432423423421212312312131232132132132123
```
- complex --- complex64, complex128
#### Note: Set of all complex numbers with float real and imaginary parts
```
// 1 is float32, 2 is imaginary is the example below (1 + 2i)
var comp1 complex64 = complex(1, 2)  

// 4 is float32, -6 is imaginary is the example below (4 - 6i)
var comp2 complex64 = complex(4, -6)  
```
- string
```
empty := ""

fruit := "orange"

var color string
color = "blue"
```
- [] (array)
#### Note: Collection of data types including struct types
```
colors := []string{"black", "blue", "green"}

var num [4]int
num[0] = 123
num[1] = 146
num[2] = 158
num[3] = 368

type human struct{
    name string
    age int
    height float32
}

humans := []human{
    {
        name: "akhtar lava",
        age: 50,
        height: 5.92,
    },
    {
        name: "bruce wayne",
        age: 123,
        height: 6.12,
    }
}

// appending to the array
humans = append(humans, human{name:"donald biden", age:212, height:12})
```
- map[k]v
#### Note: map implementation in Go - Key Value Pairs
```
// map[key]value

m := make(map[string]int)
m["three"] = 3
m["apple] = 5

// you can retrieve the value and if the key exists in the map
value, exists := m["apple"] // exists is true in this case, value is 5

type human struct{
    name string
    age int
    height float32
}

h := make(map[string]human)
h["akhtar"] = human{
    name: "akhtar",
    age: 50,
    height: 5.92,
}

```
- byte == int8
```
var b byte = 56
```
- rune == int32
#### Note: used, by convention, to distinguish character values from integer values
```
alphabets := "abcdefghijklmnopqrstuvwxyz"
for _, r := range alphabets {
    // r is not a letter - it's the unicode value of the letter
    // for a, r == 97
}
```