# Todo App

A simple, modern Todo application built with plain HTML, CSS, and JavaScript.

## 📸 Screenshots

<table>
  <tr>
    <td align="center">
      <img src="./Screenshot%202026-05-13%20000814.png" width="400"/><br>
      <b>Home Page</b>
    </td>
    <td align="center">
      <img src="./Screenshot%202026-05-13%20000848.png" width="400"/><br>
      <b>Adding Tasks</b>
    </td>
  </tr>

  <tr>
    <td align="center">
      <img src="./Screenshot%202026-05-13%20001008.png" width="400"/><br>
      <b>Task Completion</b>
    </td>
    <td align="center">
      <img src="./Screenshot%202026-05-13%20001159.png" width="400"/><br>
      <b>Progress Tracking</b>
    </td>
  </tr>

  <tr>
    <td align="center" colspan="2">
      <img src="./Screenshot%202026-05-13%20001402.png" width="500"/><br>
      <b>Confetti Celebration</b>
    </td>
  </tr>
</table>

## What this project includes

- Add new tasks
- Mark tasks complete with a checkbox
- Delete tasks
- Persist tasks in browser `localStorage`
- Progress bar that updates as tasks are completed
- Visual completion celebration using a confetti effect

## localStorage support

- Tasks are saved in browser `localStorage` so they persist across page reloads.
- Each task is stored as part of a serialized array under the key `tasks`.
- This allows the app to restore state automatically when reopening the page.

## CRUD operations

This app supports the core CRUD operations:

- **Create**: Add new tasks using the input field and submit button.
- **Read**: Load and display saved tasks from browser `localStorage` on page load.
- **Update**: Mark tasks complete or edit the task text to change its content.
- **Delete**: Remove tasks with the delete button.

## Technologies used

- HTML5
- CSS3
- JavaScript (ES6)
- Browser `localStorage`
- `tsparticles` Confetti bundle via CDN

## How it works

1. **Task entry**
   - The user types a task into the input field and submits the form.
   - The JavaScript `addTask()` function adds the task object to the `tasks` array.
   - The task list is re-rendered and the app state is saved to `localStorage`.

2. **Task persistence**
   - On page load, the app reads stored tasks from `localStorage`.
   - If tasks exist, they are loaded into the app and displayed automatically.
   - Updated tasks are saved back to `localStorage` whenever tasks are added, edited, completed, or deleted.

3. **Task completion**
   - Each task has a checkbox that toggles its completed status.
   - When the checkbox state changes, the UI updates and the task is saved again.

4. **Progress UI**
   - The progress bar is calculated from completed tasks versus total tasks.
   - The text counter shows the current completed/total ratio.

5. **Confetti celebration**
   - When all remaining tasks are completed, a confetti animation is triggered.
   - The confetti effect is loaded from the `tsparticles` CDN and activated by the `blaskConfetti()` function.

## Files in the project

- `index.html` — main HTML file with app markup
- `style.css` — app styling and layout
- `app.js` — app logic, task handling, progress updates, and confetti trigger

## How to run

1. Open `index.html` in your browser.
2. Or, open the project in VS Code and use Live Server to view it locally.
3. Add tasks, mark them complete, and watch the progress bar update.

## Notes

- The app uses only client-side code.
- Tasks are stored in the browser, so data persists across page reloads on the same device.
- No backend or database is required.
