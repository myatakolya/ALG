import "math"

func shift(array []int, steps int) {
    l := len(array)
    if steps < 0 {
        steps = int( math.Ceil(math.Abs(float64(steps))/10)*10+float64(steps) )
    }
    s := steps%10
    var result []int
    result = append(result, array[l-s:]...)
    result = append(result, array[:l-s]...)
    copy(array, result[:])
}
