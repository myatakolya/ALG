package main

import (
    "fmt"
)

func main() {
    var n int
    fmt.Scan(&n)

    heights := make([]int, n)
    for i := 0; i < n; i++ {
        fmt.Scan(&heights[i])
    }

    left, right := 0, n-1
    maxLeft, maxRight := 0, 0
    water := 0

    for left <= right {
        if heights[left] <= heights[right] {
            if heights[left] > maxLeft {
                maxLeft = heights[left]
            } else {
                water += maxLeft - heights[left]
            }
            left++
        } else {
            if heights[right] > maxRight {
                maxRight = heights[right]
            } else {
                water += maxRight - heights[right]
            }
            right--
        }
    }

    fmt.Println(water)
}
