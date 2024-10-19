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
  width: 200px; 
}

.menu-item {
  display: flex;
  align-items: center;
  padding: 10px;
  width: 100%;
  text-align: left;
  border: 1px solid transparent;
  border-radius: 5px; 
  transition: border-color 0.3s ease;
}

.avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%; 
  margin-right: 10px; }

.menu-text {
  display: none; 
  transform: translateY(10px)
  
}

.sidebar.expanded .menu-text {
  display: block; 
  transition-delay: 0s;
  transform: translateY(0);
  opacity: 1;
}

.menu-item:hover {
  border-color: white; 
  background-color: rgba(255, 255, 255, 0.1); 
}
</style>
