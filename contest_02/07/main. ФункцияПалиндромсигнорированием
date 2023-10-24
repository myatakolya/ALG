import "strings"

func Reverse(s string) string {
    runes := []rune(s)
    for i, j := 0, len(runes)-1; i < j; i, j = i+1, j-1 {
        runes[i], runes[j] = runes[j], runes[i]
    }
    return string(runes)
}

func isPalindrome(input string) bool {
    lowinput := strings.ToLower(input)
    for _, v := range []rune("~!@#%^&*() ") {
        lowinput = strings.ReplaceAll(lowinput, string(v), "")
    }

    return lowinput == Reverse(lowinput)
}