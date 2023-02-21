---
title: "Data Types in Go"
date: 2023-02-20T14:12:55-06:00
draft: true
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
planets := 8

val noOfPlanets int
noOfPlanets = 8

val noOfEyes int8
noOfEyes = 3
```
- uint --- uint8, uint16, uint32, uint64
- uintptr
- float --- float32, float64
- complex --- complex64, complex128
- string
- [] (array)
- map[k]v
- byte == int8
- rune == int32

