<template>
  <div class="store">
    <div class="container">
      <div class="row">
        <header>
          <h1>
            Our
            <strong class="banner-title">store</strong>
          </h1>
        </header>
      </div>
    </div>
    <div class="row">
      <div class="store-items">
        <a href="#" class="btn" data-filter="all"> all</a>
        <a href="#" class="btn" data-filter="cakes">cakes</a>
        <a href="#" class="btn" data-filter="cupcakes">cupcakes</a>
        <a href="#" class="btn" data-filter="sweets">sweets</a>
        <a href="#" class="btn" data-filter="doughnuts">doughnuts</a>
      </div>
    </div>
    <StoreSearch />
    <FoodStore />
  </div>
</template>

<script>
import StoreSearch from "./StoreSearch.vue";
import FoodStore from "./FoodStore.vue";
export default {
  components: {
    StoreSearch,
    FoodStore,
  },
};
</script>

<style scoped>
.store {
  background: var(--mainGrey);
  padding-bottom: 3rem;
  padding-top: 3rem;
  margin-right: -105px;
  /* margin-left: -45px; */
  display: block;
}
.container {
  width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}
.row {
  display: flex;
  margin-right: -15px;
  margin-left: -15px;
}
header {
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  position: relative;
  width: 100%;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
  margin-bottom: 1.7rem;
}
@media (max-width: 820px){
  header{
    margin-right: 65px;
  }
}
@media (max-width: 420px){
  header{
    margin-left: -45px;
  }
}
header h1 {
  padding-right: 25px;
  text-align: center;
  margin-bottom: 0.5rem;
  font-family: inherit;
  font-weight: 500;
  line-height: 1.2;
  font-size: 30px;
  text-transform: capitalize;
}
.store-items {
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 1rem;
  margin-top: 0.5rem!;
  justify-content: space-around;
  display: flex;
  width: 620px;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
}
@media (max-width: 820px) {
  .store-items {
    margin-left: 60px;
    padding-bottom: 10px;
      width: 720px;
  margin-right: auto;
  }
}
@media (max-width: 420px){
   .store-items {
    margin-left: 20px;
    padding-bottom: 10px;
      width: 400px;
  
  }
}
.btn {
  text-transform: uppercase;
  display: inline-block;
  font-weight: 400;
  text-align: center;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: 0.25rem;
  color: var(--mainBlack);
  border-color: var(--mainBlack);
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
   border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}
.btn:hover {
  color: var(--mainPink);
}
</style>
