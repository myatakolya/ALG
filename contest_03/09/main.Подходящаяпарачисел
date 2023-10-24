package main

import (
	"fmt"
	"sort"
)

func main() {
	var n, x int
	fmt.Scan(&n, &x)

	numbers := make([]int, n)
	for i := 0; i < n; i++ {
		fmt.Scan(&numbers[i])
	}

	sort.Ints(numbers)

	i, j := 0, n-1
	for i < j {
		if numbers[i]+numbers[j] == x {
			fmt.Println(numbers[i], numbers[j])
			return
		} else if numbers[i]+numbers[j] < x {
			i++
		} else {
			j--
		}
	}

	fmt.Println(0, 0)
}
