## Задача 3
Напишите программу для перевода метров в футы

```
package main

import "fmt"

func main() {
	fmt.Print("Enter a number of meters: ")
	var input float64
	var metersinfoot float64
	metersinfoot = 0.3048
	fmt.Scanf("%f", &input)

	output := input / metersinfoot

	fmt.Println(output)
}
```

Напишите программу, которая найдет наименьший элемент в любом заданном списке
```
package main

func main() {
	var x = []int{48, 96, 86, 68, 57, 82, 63, 70, 37, 34, 83, 27, 19, 97, 9, 17}
	var y int
	y = x[0]
	for _, z := range x {
		if y > z {
			y = z
		}
	}
	println("Minimal element: ", y)
}
```
Напишите программу, которая выводит числа от 1 до 100, которые делятся на 3. То есть
```
package main

import "os"

func main() {
	var start int
	var sum int
	var end int
	var multiplier int
	start = 0
	end = 100
	multiplier = 3
	if multiplier == 0 {
		println("Multiplier can't be 0")
		os.Exit(2)
	}
	sum = start % multiplier
	if (multiplier < 0) && (end > (start + sum)) {
		println("Incorrect input data")
		os.Exit(2)
	}
	if (multiplier > 0) && (end < (start + sum)) {
		println("Incorrect input data")
		os.Exit(2)
	}

	print("Numbers in range from ", start, " to ", end, " which can be devided by ", multiplier, ":")
	if (multiplier * start) < 0 {
		start = start - multiplier
	}
	if multiplier > 0 {
		for i := (start - sum + multiplier); i < end; i += multiplier {
			print(" ", i)
		}
	}
	if multiplier < 0 {
		for i := (start - sum + multiplier); i > end; i += multiplier {
			print(" ", i)
		}
	}
}
```
