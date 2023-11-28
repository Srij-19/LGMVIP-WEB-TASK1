document.addEventListener('DOMContentLoaded', function () {
  const form = document.getElementById('todo-form');
  const input = document.getElementById('todo-input');
  const todoList = document.getElementById('todo-list');

  form.addEventListener('submit', function (event) {
    event.preventDefault();
    const task = input.value.trim();

    if (task !== '') {
      const listItem = document.createElement('li');
      listItem.className = 'todo-item';
      listItem.innerHTML = `
        <span>${task}</span>
        <button class="delete-button">Delete</button>
      `;

      todoList.appendChild(listItem);
      input.value = '';
    }
  });

  todoList.addEventListener('click', function (event) {
    if (event.target.classList.contains('delete-button')) {
      const listItem = event.target.parentElement;
      todoList.removeChild(listItem);
    }
  });
});
