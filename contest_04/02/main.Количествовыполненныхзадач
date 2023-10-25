#include <iostream>
#include <fstream>
#include "json.hpp"

using json = nlohmann::json;

int main() {
    std::ifstream i("data.json");
    json j;
    i >> j;

    int user_id;
    std::cin >> user_id;

    int completed_tasks = 0;
    for (const auto& project : j) {
        for (const auto& task : project["tasks"]) {
            if (task["user_id"] == user_id && task["completed"] == true) {
                completed_tasks++;
            }
        }
    }

    std::cout << completed_tasks << std::endl;

    return 0;
}
