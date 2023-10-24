package main

import (
	"fmt"
)

func main() {
	var n int
	fmt.Scan(&n)

	numbers := make([]int64, n)
	for i := 0; i < n; i++ {
		fmt.Scan(&numbers[i])
	}

	result := int64(0)
	for _, number := range numbers {
		result ^= number
	}

	fmt.Println(result)
}
