<template>
  <section class="header">
    <div class="wrap">
      <div class="header-bar">
        <div class="logo">
          <img src="./img/flag_logo.png" alt="logo" class="logo__img">
          <div class="logo__description">ФЛАГ Покупки</div>
        </div>
        <div class="nav">
          <button class="nav__btn">Регистрация</button>
        </div>          
      </div>
    </div>
  </section>
  <section class="body">
    <div class="wrap">
      <div class="breadcrumbs">
        Главная > Каталог
      </div>
      <h1>Каталог</h1>
      <div class="category-list">
        <div class="category-item">
          <img src="./img/categories/img.png" alt="" class="category-item__img">
          <div class="category-item__overlay"></div>
          <p class="category-item__name">Бакалея</p>
        </div>
      </div>
    </div>
  </section>

</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Rubik';
  color: #414141;
  font-weight: 400;
  font-style: normal;
}

body {
  background: #F4F4F2;  
}

button {
  border: none;
  outline: none;
  color: #FFFFFF;
  background: #70C05B;
}

h1 {
  margin-top: 24px;
  padding-top: 15px; 
  font-size: 64px;
  font-weight: 700;
}

.wrap {
  max-width: 1208px;
  margin: 0 auto;
}

.header {
  height: 72px;
  background-color: #FFFFFF;
  box-shadow: 2px 4px 8px rgba(0, 0, 0, 0.1);
}

.header-bar {
  display: flex;
  justify-content: space-between;
  padding-top: 5px;
}

.logo {
  margin-top: 12px;
  display: flex;
  align-items: center;
}

.logo__img {
  margin-right: 19px;
}

.logo__description {
  font-size: 22px;
  font-weight: 600;
}

.nav__btn {
  width: 140px;
  font-size: 16px;
  line-height: 24px;
  border-radius: 4px;
  padding: 8px;
  margin-top: 12px;
}

.breadcrumbs {
  margin-top: 24px;
  padding-top: 5px;
  font-size: 12px;
}

.category-item {
  position: relative;
  width: 272px;
  height: 200px;
  box-shadow: 1px 2px 4px rgba(112, 192, 91, 0.2);
  border-radius: 4px;
  cursor: pointer;
}

.category-item__img {
  border-radius: 4px;
}

.category-item__overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(112, 192, 91, 0) 0%, #70C05B 82.81%);
  border-radius: 0 0 4px 4px;
}

.category-item__overlay:hover {
  background: linear-gradient(180deg, rgba(255, 102, 51, 0) 0%, #FF6633 100%);
}

.category-item__name {
  position: absolute;
  bottom: 10px;
  left: 10px;
  font-size: 18px;
  font-weight: 700;
  color: #FFFFFF;
}
</style>
