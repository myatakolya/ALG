#include <iostream>
#include "set"

using namespace std;

auto action(multiset <int> arr, int times){
    for(int i = 0; i < times; i++){
        int j;
        cin >> j;
        arr.insert(j);
    }
    return arr;
}

int main()
{
    multiset <int> answer;
    int n;
    cin >> n;
    answer = action(answer, n);
    cin >> n;
    answer = action(answer, n);

    for(auto x : answer){
        cout << x << " ";
    }
}