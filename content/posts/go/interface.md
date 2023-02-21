---
title: "Interface in Go"
date: 2023-02-20T14:07:33-06:00
draft: true
tags: ['Go']
---

### Interface defines a set of methods for a structure to implement. Implementation of an interface would implement the defined methods as per requirement

```
type Car interface{
    start()
    driveForward()
    stop()
}
```

### First implementation - BMW 3 series

```
type BMW3Series struct{
    color string,
    automatic bool,
}

func (b *BMW3Series) start(){
    //push button
}

func (b *BMW3Series) driveForward(){
    //if start
    //if b.automatic move to drive 
    //else push clutch change gear
}

func (b *BMW3Series) stop(){
    //if start
    //push break and push button
}
```

### Second implementation - Corolla 1998

```
type Corolla1998 struct{
    color string,
    automatic bool,
}

func (b *Corolla1998) start(){
    //insert key and twist clockwise
}

func (b *Corolla1998) driveForward(){
    //if start
    //if b.automatic move to drive 
    //else push clutch change gear
}

func (b *Corolla1998) stop(){
    //if start
    //push break and rotate key anti-clockwise
}
```

```
type human struct{
    name string,
    age int,
    car Car,
}


bmw := BMW3Series{color: "black", automatic: "true"}
corolla :=  Corolla1998{color: "silver", automatic: "false"}

maula := human{
    name: "maula jatt",
    age: 45,
    car: bmw,
}

maula.car.start()

jattni := human{
    name: "jattni",
    age: 44,
    car: corolla,
}

jattni.car.start()
jattni.car.driveForward()
```

### As defined above the human has a car. Cars change, so we have the interface in the human struct but the actual definition specifies which car.