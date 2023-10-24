#include <iostream>
#include <set>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    int n, m;
    cin >> n;
    set<string> words_n, words_m, common_words;
    string word;

    for (int i = 0; i < n; ++i) {
        cin >> word;
        words_n.insert(word);
    }

    cin >> m;
    for (int i = 0; i < m; ++i) {
        cin >> word;
        words_m.insert(word);
    }

    set_intersection(words_n.begin(), words_n.end(), words_m.begin(), words_m.end(),
                     inserter(common_words, common_words.begin()));

    if (common_words.empty()) {
        cout << -1;
    } else {
        for (const string &w : common_words) {
            cout << w << " ";
        }
    }

    return 0;
}