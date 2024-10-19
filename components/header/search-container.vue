<template>
    <div class="search-container">
        <input type="text" placeholder="Поиск" />
    </div>
</template>


<style>
    .search-container {
        display: flex; /* Используем flex для центрирования */
        justify-content: center; /* Центрируем содержимое */
        height: 100%; /* Задаем высоту 100% родителя */
        flex: 1;
    }

    input {
        padding: 10px; /* Отступы внутри инпута */
        /* border: 1px solid #333; Граница инпута */
        border-radius: 4px; /* Скругление углов */
        background-color: #333;
    }
</style>