package main

import (
	"encoding/json"
	"fmt"
	"io/ioutil"
)

type Task struct {
	UserID    int    `json:"user_id"`
	ID        int    `json:"id"`
	Title     string `json:"title"`
	Completed bool   `json:"completed"`
}

type Project struct {
	ProjectID int    `json:"project_id"`
	Tasks     []Task `json:"tasks"`
}

func main() {
	var userID int
	fmt.Scan(&userID)

	file, _ := ioutil.ReadFile("data.json")

	var projects []Project
	json.Unmarshal(file, &projects)

	var completedTasks int
	for _, project := range projects {
		for _, task := range project.Tasks {
			if task.UserID == userID && task.Completed {
				completedTasks++
			}
		}
	}

	fmt.Println(completedTasks)
}