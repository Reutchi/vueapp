<template>
  <section id="header">
      <div class="hamburger-menu">
        <input id="menu__toggle" type="checkbox" />
        <label class="menu__btn" for="menu__toggle">
        <span></span>
        </label>

        <ul class="menu__box">
            <li v-for="item in menu">
            <router-link class="menu__item" :to="item.path">{{item.name}}</router-link>
            </li>
        </ul>
      </div>
            
            <div class="navigation">
              <a href="/"><img src="../assets/logo.svg" alt="logo"></a>
            
              <ul>
                  <li v-for="item in menu">
                    <router-link :to="item.path">{{item.name}}</router-link>
                  </li>
              </ul>
            </div>
  </section>
</template>

<script>
export default {
  name:'HeaderNav',
  data(){
    return {
      menu:[
        {
          name:'Home',
          path:'/'
        },
         {
          name:'About',
          path:'/about'
        },
         {
          name:'Contact',
          path:'/contact'
        }
      ]
    }
  }

}
</script>

<style lang="scss" scoped>
@media only screen and (min-width: 0) {
.menu{
  display: none;
}
/* Hamb menu */
#menu__toggle {
  opacity: 0;
}
#menu__toggle:checked + .menu__btn > span {
  transform: rotate(45deg);
}
#menu__toggle:checked + .menu__btn > span::before {
  top: 0;
  transform: rotate(0deg);
}
#menu__toggle:checked + .menu__btn > span::after {
  top: 0;
  transform: rotate(90deg);
}
#menu__toggle:checked ~ .menu__box {
  left: 0 !important;
}
.menu__btn {
 position: fixed;
    z-index: 100;
    top: 3rem;
    right: 3rem;
    padding: 10px;
    background: transparent;
    cursor: pointer;
}
.menu__btn > span,
.menu__btn > span::before,
.menu__btn > span::after {
  display: block;
  position: absolute;
  width: 100%;
  height: 2px;
  background-color: #616161;
  transition-duration: .25s;
}
.menu__btn > span::before {
  content: '';
  top: -8px;
}
.menu__btn > span::after {
  content: '';
  top: 8px;
}
.menu__box {
  display: block;
  position: fixed;
  top: 0;
  left: -100%;
  width: 300px;
  height: 100%;
  margin: 0;
  padding: 80px 0;
  list-style: none;
  background-color: #ECEFF1;
  box-shadow: 2px 2px 6px rgba(0, 0, 0, .4);
  transition-duration: .25s;
}
.menu__item {
  display: block;
  padding: 12px 24px;
  color: #333;
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  font-weight: 600;
  text-decoration: none;
  transition-duration: .25s;
}
.menu__item:hover {
  background-color: #CFD8DC;




}
/* Hamb Finish */



.navigation{
  ul{
    display: none;
  }
}
}
@media only screen and (min-width: 750px){
.navigation{
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
  ul{
    display: flex;
    li{
      margin-right: 15px;
      a{
        color: #808080;
        transition: 1s ease;
      }
      a:hover{
        color: #000000;
      }
    }
  }
}
.hamburger-menu{
  display: none;
}
}




</style>
