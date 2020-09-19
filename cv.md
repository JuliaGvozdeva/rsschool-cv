### Curriculum vitae ###
***
1. Julia Gvozdeva.
2. Contacts:
	* Email: yulya.gvozdeva.96@mail.ru
	* [Github](https://github.com/JuliaGvozdeva)
3. I am an information security specialist by profession, but now I work as a tester in the company Mercury development. I want to be a good front-end developer. I made one-page and simple multi-page sites in my student years. The quality and result of my work is very important to me. I hope that thanks to the Rschool courses I will achieve my goal.
4. I have skills: *HTML, CSS, C#, RESTfull API, Ms sql, PostgreSQL, Postman, Fiddler.*
5. Code example: 
```
const formTask = document.querySelector("#newTaskForm");
const taskList = document.querySelector("#taskList");
const cardContainer = document.querySelector("#cardContainer");

formTask.addEventListener("submit", function(event){
    event.preventDefault();

    const taskText = document.querySelector("#addNewTask").value;

    const taskHTML = `<li class="list-group-item d-flex justify-content-between"><span class="task-title">${taskText}</span><button type="button" data-action="delete-task" class="btn btn-light align-self-end">Удалить</button></li>`
    document.querySelector("#addNewTask").value = "";

    taskList.insertAdjacentHTML("beforeend", taskHTML);
    allerts('add', taskText);
});

taskList.addEventListener("click", function(event){
    if (event.target.getAttribute("data-action") == "delete-task"){
        const liElement = event.target.parentElement;
        const taskName = liElement.firstChild.innerHTML;
        liElement.remove();
        allerts('remove', taskName);
    }
});

function allerts(val, taskName){
    if (document.querySelector("#removeAllert")){
        removeAllert.remove();
    }

    let allertsHTML = ""; 
    switch(val){
        case 'add':
            allertsHTML = `<div id="removeAllert" class="alert alert-warning" role="alert">Задача ${taskName} добавлена!</div>`;
            break;
        case 'remove':
            allertsHTML = `<div id="removeAllert" class="alert alert-danger" role="alert">Задача ${taskName} удалена!</div>`;
            break;
        case 'done': 
            allertsHTML = `<div class="alert alert-success" role="alert">Задача ${taskName} выполнена!</div>`;
            break;
    }

    cardContainer.insertAdjacentHTML("beforebegin", allertsHTML);

    setTimeout(() => {
        removeAllert.remove();
    }, 800);
};
```
6. Web QA in the Nemo Travel, Web QA in the Mercury Development. Unfinished external web courses in Epam Saratov.
7. Saratov State University, CSiIT, specialty computer security.
8. English level: A2, started learning B1.