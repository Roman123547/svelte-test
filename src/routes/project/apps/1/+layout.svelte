<div class='container'>
    <a href='/project'>Домой</a>
    <slot/>
    </div>
    <style>
    .container {
    margin: 50px auto;
    max-width: 800px;
    padding: 0 20px;
    }
.apps {
display: grid;
grid-template-columns: 1fr 1fr;
grid-gap: 20px;
}
.app {
border: 1px solid #ddd;
padding: 10px;
box-shadow: 0 0 10px #eee;
}
link {
color: rgb(10, 10, 139); }
main {
display: flex;
flex-direction: column;
align-items: center;
min-height: 100%;
padding: 5vmin;
box-sizing: border-box;
background: antiquewhite;
}
form {
width: 100%;
max-width: 500px;
display: flex;
align-items: center;
margin-bottom: 1rem;
}
input {
flex-grow: 1;
width: 0;
border: none;
border-bottom: 1px solid black;
background: transparent;
box-shadow: none;
font-size: 1.2rem;
margin: 0;
outline: none;
}
    </style>
    <script>
        let newItem = "";
let todoList = [];
function add() {
if (newItem !== "") {
todoList = [
... todoList,
{
задача: newItem,
завершено: false,
},
];
newItem = "";
}
}

import { routes } from './routes.js';
    </script>
    <main>
        <form on:submit|preventDefault={add}>
            <input bind:value={newItem} placeholder="Enter to-do" />
            <button class="add-todo" onclick={add}><span>+</span></button>
            </form>
    </main>
    