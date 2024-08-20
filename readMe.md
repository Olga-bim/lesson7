Lesson 7
1. Повторение д.з. Супермаркет и игра крестики нолики
# JavaScript Concepts and Tools

## 1. Arrow Function
Arrow functions — это сокращённый синтаксис для создания функций в JavaScript. Они не имеют своего контекста `this` и всегда анонимны.

```javascript
// Arrow Function Example: 
// Функция сложения двух чисел.
const add = (a, b) => a + b;
2. Usage of Arrow Function
Arrow functions используются для сокращения синтаксиса, а также для сохранения контекста this внутри функции.

javascript
Копировать код
// Usage Example: 
// Возведение каждого элемента массива в квадрат.
const numbers = [1, 2, 3, 4];
const squares = numbers.map(n => n * n);
3. By Value / By Reference
В JavaScript примитивные типы данных (например, числа, строки) передаются по значению, тогда как объекты и массивы передаются по ссылке.

javascript
Копировать код
// By Value Example: 
// Изменение копии примитивного типа не влияет на оригинал.
let a = 5;
let b = a;
b = 10;
console.log(a); // 5

// By Reference Example: 
// Изменение копии объекта влияет на оригинал.
let obj1 = { name: 'John' };
let obj2 = obj1;
obj2.name = 'Doe';
console.log(obj1.name); // 'Doe'
4. Spread Operator
Оператор расширения (...) используется для развёртывания элементов массива или свойств объекта.

javascript
Копировать код
// Spread Operator Example with Arrays: 
// Объединение массивов.
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5, 6];
console.log(arr2); // [1, 2, 3, 4, 5, 6]

// Spread Operator Example with Objects: 
// Копирование объекта с добавлением новых свойств.
const obj1 = { name: 'John' };
const obj2 = { ...obj1, age: 30 };
console.log(obj2); // { name: 'John', age: 30 }
5. URL
URL (Uniform Resource Locator) — это строка, указывающая на местоположение ресурса в интернете.

text
Копировать код
// URL Example: 
// Ссылка на веб-страницу.
https://www.example.com/path/to/resource
6. Server
Сервер — это компьютер или программа, которая обрабатывает запросы и отправляет данные по сети.

7. Fake Server JSON Placeholder
JSON Placeholder — это онлайн-ресурс, предоставляющий фейковые данные и сервер для тестирования API.

text
Копировать код
// JSON Placeholder Example: 
// URL для работы с фейковым API.
https://jsonplaceholder.typicode.com/
8. Node.js
Node.js — это среда выполнения JavaScript, позволяющая запускать JavaScript-код на сервере.

bash
Копировать код
// Node.js Example: 
// Запуск JavaScript-кода на сервере.
node app.js
9. Fetch
fetch — это встроенная функция для выполнения HTTP-запросов и получения ответов в формате Promise.

javascript
Копировать код
// Fetch Example: 
// Получение списка постов с сервера.
fetch('https://jsonplaceholder.typicode.com/posts')
    .then(response => response.json())
    .then(data => console.log(data));
10. CRUD
CRUD — это аббревиатура для Create, Read, Update, Delete, описывающая основные операции с данными.

11. API
API (Application Programming Interface) — это набор правил и протоколов, позволяющих взаимодействовать с приложениями или сервисами.

12. POST, PUT, DELETE, GET
Эти методы используются для выполнения различных операций с данными в HTTP-запросах.

javascript
Копировать код
// GET Example: 
// Получение данных с сервера.
fetch('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => response.json())
    .then(data => console.log(data));

// POST Example: 
// Создание нового ресурса на сервере.
fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST',
    body: JSON.stringify({ title: 'foo', body: 'bar', userId: 1 }),
    headers: { 'Content-type': 'application/json; charset=UTF-8' },
})
    .then(response => response.json())
    .then(data => console.log(data));

// PUT Example: 
// Обновление существующего ресурса на сервере.
fetch('https://jsonplaceholder.typicode.com/posts/1', {
    method: 'PUT',
    body: JSON.stringify({ id: 1, title: 'foo', body: 'bar', userId: 1 }),
    headers: { 'Content-type': 'application/json; charset=UTF-8' },
})
    .then(response => response.json())
    .then(data => console.log(data));

// DELETE Example: 
// Удаление ресурса на сервере.
fetch('https://jsonplaceholder.typicode.com/posts/1', {
    method: 'DELETE',
})
    .then(response => console.log('Deleted:', response.ok));
13. npm JSON Server
JSON Server — это инструмент, позволяющий создавать фейковые REST API с использованием JSON-файла.

bash
Копировать код
// JSON Server Example: 
// Установка JSON Server и запуск на основе файла db.json.
npm install -g json-server
json-server --watch db.json
14. HTTP Status Codes
Коды состояния HTTP сообщают о статусе ответа на запрос:

200: OK — Запрос выполнен успешно.
201: Created — Ресурс создан успешно.
400: Bad Request — Неправильный запрос.
401: Unauthorized — Требуется аутентификация.
403: Forbidden — Доступ запрещён.
404: Not Found — Ресурс не найден.
405: Method Not Allowed — Метод не поддерживается.
500: Internal Server Error — Ошибка на сервере.
15. Port
Порт — это числовой идентификатор, используемый для адресации определённых процессов или сетевых сервисов.

text
Копировать код
// Port Example: 
// Локальный сервер работает на порту 3000.
http://localhost:3000
16. Axios
axios — это библиотека для выполнения HTTP-запросов с поддержкой промисов.

javascript
Копировать код
// Axios Example: 
// Получение данных с сервера с использованием библиотеки Axios.
const axios = require('axios');

axios.get('https://jsonplaceholder.typicode.com/posts')
    .then(response => console.log(response.data))
    .catch(error => console.error(error));
17. ID
ID (идентификатор) — уникальный ключ, используемый для идентификации записей в базе данных или других структурах данных.

18. async / await
async и await позволяют писать асинхронный код, который выглядит как синхронный, упрощая работу с промисами.

javascript
Копировать код
// async/await Example: 
// Асинхронная функция для получения данных с сервера.
async function fetchData() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts');
        const data = await response.json();
        console.log(data);
    }
go
Копировать код
catch (error) {
    console.error('Error:', error);
}
}