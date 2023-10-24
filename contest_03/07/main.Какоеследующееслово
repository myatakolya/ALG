#include <iostream>
#include <fstream>
#include <string>
#include <map>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    string target;
    cin >> target;

    ifstream file("data.txt");

    map<string, map<string, int>> words;
    string back_word = "", word = "";
    while (file >> word) {
        if (!back_word.empty()) {
            words[back_word][word]++;
        }
        back_word = word;
    }

    if (words.count(target) == 0) {
        cout << '-' << endl;
        return 0;
    }

    vector<pair<string, int>> words_vector;
    for (const auto& pair : words[target]) {
        words_vector.push_back(pair);
    }

    sort(words_vector.begin(), words_vector.end(),
              [](const pair<string, int>& a, const pair<string, int>& b) {
                  return a.second > b.second || (a.second == b.second && a.first < b.first);
              }
    );

    for (int i = 0; i < min(3, (int) words_vector.size()); i++) {
        cout << words_vector[i].first << " ";
    }
}