<template>
  <div class="header">
    <header>
      <div class="logo">
        <img src="../images/logo.svg" alt="logo" />
        <Nav v-show="current == true" />
      </div>
      <div class="menu-icon">
        <i class="las la-bars" @click="showItem"> </i>
      </div>
    </header>
  </div>
</template>

<script>
import Nav from "./Nav.vue";
export default {
  name: "Header",
  props: {
    msg: String,
  },
  components: {
    Nav,
  },
  data() {
    return {
      current: false,
    };
  },
  methods: {
    showItem() {
      console.log()
      if (this.current == true) {
        this.current = false;
      } else {
        this.current = true;
      }
    },
  },
};
</script>

<style scoped>
header {
  display: flex;
  background: #fff;
  padding-left: 1.5rem;
  padding-right: 1.5rem;
}
@media (max-width: 820px) {
  header {
    max-width: 720;
  }
}
.logo {
  display: flex;
  padding-top: 0.3125rem;
  padding-bottom: 0.3125rem;
  margin-right: 1rem;
  font-size: 1.25rem;
  line-height: inherit;
  white-space: nowrap;
}
.logo img {
  margin: -10px 40px;
  width: 80px;
}
.menu-icon {
}
@media (max-width: 820px) {
  .logo {
    padding-top: 1.5125rem;
    padding-bottom: 1.5125rem;
    
  }
}
@media (max-width: 420px) {
  .las {
    display: inline-block;
    margin-left: 50px;
  }
}
@media (max-width: 820px) {
  .las {
    display: inline;
    margin: 20px 40px;
  }
}
@media (max-width: 920px){
.las{
   display: inline-block;
 margin: 50px 120px;
}
}
.las {
 display: none;
  font-style: 36px;
  font-weight: 900;
  font-size: 3.5rem;
  color: var(--mainPink);
 
}
</style>
