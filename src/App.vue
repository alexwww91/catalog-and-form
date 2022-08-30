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
        <div v-for="breadcrumb in breadcrumbs" :key="breadcrumb.id" class="breadcrumb">{{ breadcrumb.name }}</div>
      </div>
      <h1>{{ pageName }}</h1>
      <div class="category-list">
        <div v-for="(item, index) in items" :key="item.id" class="category-item" :class="`item-${index}`">
          <img :src="require(`./img/categories/${item.imgName}`)" alt="" class="category-item__img">
          <div class="category-item__overlay"></div>
          <p class="category-item__name">{{ item.name }}</p>
        </div>
      </div>
    </div>
  </section>

</template>

<script>
  export default {
    data() {
      return {
        pageName: 'Каталог',
        breadcrumbs: [
          {id: 1, name: 'Главная'},
          {id: 2, name: 'Каталог'}
        ],
        items: [
          {id: 1, name: 'Молоко, сыр, яйцо', imgName: 'milk.png'},
          {id: 2, name: 'Хлеб', imgName: 'bread.png'},
          {id: 3, name: 'Фрукты и овощи', imgName: 'fruit.png'},
          {id: 4, name: 'Бакалея', imgName: 'grocery.png'},
          {id: 5, name: 'Здоровое питание', imgName: 'helty.png'},
          {id: 6, name: 'Зоотовары', imgName: 'zoo.png'},
          {id: 7, name: 'Детское питание', imgName: 'kids.png'},
          {id: 8, name: 'Мясо, птица, колбаса', imgName: 'meat.png'},
          {id: 9, name: 'Непродовольственные товары', imgName: 'goods.png'},
        ]
      }
    }
  }
</script>

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
  display: flex;
}

.breadcrumb {
 margin: 0 28px;
 position: relative;
 cursor: pointer;
}

.breadcrumb:first-child {
 margin-left: 0;
}

.breadcrumb::after {
  content: url(./img/shape.png);
  position: absolute;
  right: -34px;
  top: 0;
  cursor: auto;
}

.breadcrumb:last-child::after {
  content: "";
}

.category-list {
  margin-top: 70px;
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 3%

}

.category-item {
  position: relative;
  height: 200px;
  box-shadow: 1px 2px 4px rgba(112, 192, 91, 0.2);
  border-radius: 4px;
  cursor: pointer;
  margin-bottom: 40px;
}

.item-0 {
grid-row-start: 1;
grid-column-start: 1;

grid-row-end: 2;
grid-column-end: 3;

}
.item-1 {
grid-row-start: 1;
grid-column-start: 3;

grid-row-end: 2;
grid-column-end: 4;

}
.item-2 {
grid-row-start: 1;
grid-column-start: 4;

grid-row-end: 2;
grid-column-end: 5;

}
.item-3 {
grid-row-start: 2;
grid-column-start: 1;

grid-row-end: 3;
grid-column-end: 2;

}
.item-4 {
grid-row-start: 2;
grid-column-start: 2;

grid-row-end: 3;
grid-column-end: 3;

}
.item-5 {
grid-row-start: 2;
grid-column-start: 3;

grid-row-end: 3;
grid-column-end: 5;

}
.item-6 {
grid-row-start: 3;
grid-column-start: 1;

grid-row-end: 4;
grid-column-end: 2;

}
.item-7 {
grid-row-start: 3;
grid-column-start: 2;

grid-row-end: 4;
grid-column-end: 4;

}
.item-8 {
grid-row-start: 3;
grid-column-start: 4;

grid-row-end: 4;
grid-column-end: 5;

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
