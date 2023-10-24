#include <iostream>
#include <stack>
#include <string>

using namespace std;

bool action(const string& input) {
    stack<char> stk;

    for (char c : input) {
        if (c == '(' || c == '{' || c == '[') {
            stk.push(c);
        } else if (c == ')' || c == '}' || c == ']') {
            if (stk.empty()) {
                return false;
            } else {
                char top = stk.top();
                stk.pop();

                if ((c == ')' && top != '(') ||
                    (c == '}' && top != '{') ||
                    (c == ']' && top != '[')) {

                    return false;
                }
            }
        }
    }

    return stk.empty();
}

int main() {
    string input;
    getline(cin, input, '!');

    if (action(input)) {
        std::cout << "YES" << std::endl;
    } else {
        std::cout << "NO" << std::endl;
    }
}