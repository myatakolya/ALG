#include <iostream>
#include <string>
#include <stack>
#include <queue>

using namespace std;

int priority(char ch) {
    switch (ch) {
        case '+':
        case '-':
            return 1;
        case '*':
        case '/':
        case '%':
            return 2;
        case '^':
            return 3;
        default:
            return 0;
    }
}

bool operattor(char ch) {
    return ch == '+' || ch == '-' || ch == '*' || ch == '/' || ch == '%' || ch == '^';
}

queue<string> action(string input) {
    stack<char> stkk;
    queue<string> que;
    string operand;

    for (char ch : input) {
        if (isdigit(ch)) {
            operand += ch;
        } else {
            if (!operand.empty()) {
                que.push(operand);
                operand.clear();
            }
            if (ch == '(') {
                stkk.push(ch);
            } else if (ch == ')') {
                while (stkk.top() != '(') {
                    que.push(string(1, stkk.top()));
                    stkk.pop();
                }
                stkk.pop();
            } else if (operattor(ch)) {
                while (!stkk.empty() && priority(stkk.top()) >= priority(ch) && ch != '^') {
                    que.push(string(1, stkk.top()));
                    stkk.pop();
                }
                stkk.push(ch);
            }
        }
    }

    if (!operand.empty()) {
        que.push(operand);
    }

    while (!stkk.empty()) {
        que.push(string(1, stkk.top()));
        stkk.pop();
    }
    return que;
}

int main() {
    string input;
    cin >> input;

    queue<string> que = action(input);

    while (!que.empty()) {
        cout << que.front() << " ";
        que.pop();
    }
}