<template>
  <div 
    class="sidebar" 
    @mouseenter="hover = true" 
    @mouseleave="hover = false"
    :class="{ expanded: hover }"
  >
    <div class="content">
      <div class="circle">
        <img src="123.jpg" width="360" height="200" alt="">
      </div>

      
      <ul>
        <li v-for="(item, index) in menuItems" :key="index" class="menu-item">
          <img :src="item.avatar" alt="Avatar" class="avatar" />
          <span class="menu-text" v-if="hover">{{ item.text }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: false,
      menuItems: [
        { avatar: 'path/to/avatar1.png', text: 'Главная' },
        { avatar: 'path/to/avatar2.png', text: 'Создать форум' },
        { avatar: 'path/to/avatar2.png', text: 'Рейтинг' },
        { avatar: 'path/to/avatar3.png', text: 'Авторы' },
        { avatar: 'path/to/avatar2.png', text: 'О нас' },
      ],
    };
  },
};
</script>

<style scoped>
.sidebar {
  width: 100px;
  height: 100vh;
  background-color: #333;
  color: white;
  position: fixed;
  top: 0;
  left: 0;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: width 0.3s;
}

.sidebar.expanded {
  width: 200px; /* Ширина при наведении */
}

.menu-item {
  display: flex;
  align-items: center;
  padding: 10px;
  width: 100%;
  text-align: left;
  border: 1px solid transparent; /* Граница по умолчанию (прозрачная) */
  border-radius: 5px; /* Закругление углов */
  transition: border-color 0.3s ease;
}

.avatar {
  width: 40px; /* Размер аватара */
  height: 40px;
  border-radius: 50%; /* Круглая форма */
  margin-right: 10px; /* Отступ справа от аватара */
}

.menu-text {
  display: none; /* Скрываем текст по умолчанию */
  transform: translateY(10px)
  
}

.sidebar.expanded .menu-text {
  display: block; /* Показываем текст при наведении */
  transition-delay: 0s;
  transform: translateY(0);
  opacity: 1;
}

.menu-item:hover {
  border-color: white; /* Цвет границы при наведении */
  background-color: rgba(255, 255, 255, 0.1); /* Фоновый цвет при наведении */
}
</style>
