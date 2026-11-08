

### 프로젝트 설명
이 프로젝트는github에서 찾은 React와 JavaScript를 사용하여 만든 웹 애플리케이션이다. 사용자는 할 일을 추가, 수정, 삭제할 수 있고 완료한 일도 확인할 수 있다. 카테고리와 마감일도 설정할 수 있다.
선택 이유: 
이제 처음 막 시작하는 react이기 때문에 복잡한 곳을 하면 코드 분석하기에 어려움이 있을 것 같아 그전까지 계속 과제로 해왔던 비슷한 내용들이라 선택하였다. 
원본: 
https://github.com/Jadec15/react-todo-app
라이센스: 
MIT License

### Installation:
깃헙에서 프로젝트를 clone한다 - 프로젝트에서 요구하는 npm install로 패키지를 설치한다 -  npm run dev로 실행시킨다 

### Source Code Exploration: 

App.jsx
react에서 주요 화면과 기능을 담당하고 있다. 여러 event들과 html 등의 기능이 있다.

App.css
디장인을 담당하는 파일로 여러 스타일의 디자인을 설정한다.

main.jsx
react 앱을 실행하고 화면에 표시하는 파일이다.

index.css
기본 css를 설정하고 있다.

index.html
react 앱이 표시되는 기본 html 파일이다. 

컴포넌트
addTask() - 새로운 할 일을 추가한다
deleteTask() - 기존에 할 일을 삭제한다.
completeTask() - 할 일이 완료 됐다면 완료로 처리를 한다.
saveEdit() - 수정한 할 일을 저장한다

코드 설명
const addTask = () => {
  if (task.trim() !== "") {
    setTasks([...tasks, { text: task, category, dueDate }]);
    setTask("");
    setDueDate("");
  }
}; 
먼저 task.trim을 사용하여 입력 내용이 입력이 됐는지 확인하다. 입력을 했다면 setTask로 기존 할 일을 목록에 내용과 카테고리와 마감일더 작성해 추가한다. setTask와 setDueDate로 입력했던 내용과 마감일을 초기화한다. 그 뒤 추가 버튼을 누르면 목록에 새롭게 추가가된다. 

const addTask = () => {
  if (task.trim() !== "") {
    setTasks([...tasks, { text: task, category, dueDate }]);
    setTask("");
    setDueDate("");
  }
};
tasks[index]로 사용자가 완료한 할 일을 가지고 온다. setCompletedTasks()로 기존에 있던 목록에 해당 할 일을 추가한다. filter로 할일을 목록에서 완료한 항목을 제거한다. 버튼을 누르면 할 일이 진행 중인 목록에서 사라지고 완료 목록으로 이동한다. 

### Customizing:
Text: App.jsx

To-Do List -> 공부할거
Enter your task here->공부할거 입력해라
Add Task -> 추가 Task
Category-> 할거

로 변경해 수정 전에는 영어로 나왔던 것들을 수정 후 한국어 단어 몇개로 나오게 했다

Style: App.css

body의 배경색 변경
.container의 배경색과 크기 설정
h1의 글자 색상 변경
button의 배경색과 테두리 색상 변경
button:hover의 색상 병경

수정 전에는 단조로웠던 디자인을 수정 후 컬러풀하게 변경했다

Ul/ DATA : 

Personal -> 줸장할 과제
Work->과목
Shopping ->안해도 되는 예습 복습
Due ->  마감언제까지 할거야!!!

전에는 쇼핑관련된 페이지를 내용을 바꿔 정말 과제를 하기 싫은 학생 관련 페이지로 변경하였다

### Deployment : https://react-todo-app1-pearl.vercel.app

#### Weekly review: 

1. react 실행방법
react를 실행하기 위해 먼저 깃헙에서 fork를 해야 하고 그 뒤에 주소를 복붙해 clone을 뜨고 npm install로 필요한 페키지를 설치하고 npm run dev로 프로젝트를 실행하는 방법을 배웠다.

2. react로 화면 수정
기존에는 html 파일에서 화면을 구성하고 html안에서 내용을 수정하고나, javaScript로 DOM을 직접 수정하여 화면을 변경했다. 하지만 React에서는 App.jsx와 같은 JavaScript 파일 안에 JSX 문법을 사용하여 html과 비슷한 코드를 작성을 해 수정할 수 있다는 것을 배웠다

3. react 프로젝트 구조
react 프로젝트에서는 index.html은 React 앱이 표시되는 페이지이고 main.jsx는 React 앱을 실행하는 역할을 한다. 또한 App.jsx는 화면을 구성하고 App.css는 디자인을 담당한다는 것처럼 여러 파일들이 각각 다른 연할을 하고 있다는 것을 배웠다.

### ai used
처음 react을 고를 때 너무 많아 ai에게 추천을 받았다. 

어려웠던 점: 
assignment10 저장소에 수정한 프로젝트를 organization으로 remote를 추가해 연결하는 방법을 잘 몰라 물어봤다. 
Git Remote의 origin과 classroom의 차이를 이해하였고, git push classroom master 명령어를 사용하여 수정한 코드를 과제 저장소에 업로드할 수 있었다. 또한 개인 GitHub 저장소와 Classroom 저장소를 각각 관리하는 방법을 배웠다.






# React To-Do List App

A simple and interactive To-Do List built with React! 
Users can add, edit, delete, and mark tasks as completed. Users can mark the type of task and the Due date. Tasks are stored locally and persist after refresh.

---

# Features
- Add tasks with type and due dates
- Mark tasks as completed
- Undo completed tasks
- Edit existing tasks
- Delete tasks
- Data is saved using `localStorage` (persists after refresh)

---

# Installation & Setup

# 1️ Clone the Repository
git clone https://github.com/jadec15/react-todo-app.git
cd react-todo-app

# 2️ Install Dependencies
Install Node.js if you don't already have it installed. Then run the command:
npm install

# 3️ Start the Development Server
npm run dev
The app will open in your browser at http://localhost:5173/.

# Built With
React (Vite)
JavaScript (ES6+)
CSS (Custom Styling)
LocalStorage API (for saving tasks)

# How to Use
Enter a task in the input box and click "Add Task".
Set a category and due date if needed.
Click ✅ to mark a task as completed.
Click ❌ to delete a task.
Click ✏️ to edit a task.
Click "Show Completed Tasks ⬇️" to view completed tasks.
Refresh the page and tasks remain saved

# Customization
Want to modify the project for yourself? Here’s where you can make changes:

App.jsx → Main logic and UI.
App.css → Styling.
localStorage handling → Modify task persistence.

# Contributing
This is a personal project, and contributions are not accepted at this time.

# License
This project is open-source under the MIT License.

# Contact
Have questions? Reach out via: mail: jadecabral96@gmail.com

⭐ If you like this project, give it a star on GitHub! ⭐


