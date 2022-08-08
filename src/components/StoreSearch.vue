<template>
  <div class="row">
    <div class="search">
      <form>
        <div class="form-input">
          <div class="input-group">
            <span class="input-icon" id="search-icon"
              ><i class="las la-search"></i
            ></span>
          </div>
          <input
            type="text"
            class="form-control"
            placeholder="item...."
            id="search-item"
            v-model="search"
          />
        </div>
      </form>
    </div>
  </div>
  <div class="food-card">
    <div class="card" v-for="data in filteredData" :key="data">
      <div class="img-container">
        <img :src="data.image" class="card-img-top store-img" alt="" />
        <span class="store-item-icon">
          <i class="las la-shopping-cart"></i>
        </span>
      </div>
      <div class="card-body">
        <div class="card-text">
          <h5 id="store-item-name">{{ data.name }}</h5>
          <h5 class="store-item-value">{{ data.price }}</h5>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: "",
      // filteredData: [],
      datas: [
        {
          name: "Sweet Item",
          price: "$5",
          image: [require("../images/sweets-1.jpeg")],
        },
        {
          name: "Cup Item",
          price: "$5",
          image: [require("../images/cupcake-1.jpeg")],
        },
        {
          name: "Cake Item",
          price: "$5",
          image: [require("../images/cake-1.jpeg")],
        },
        {
          name: "Dougnut Item",
          price: "$5",
          image: [require("../images/doughnut-1.jpeg")],
        },
        {
          name: "Sweet Item",
          price: "$5",
          image: [require("../images/cupcake-2.jpeg")],
        },
        {
          name: "Cupcake Item",
          price: "$5",
          image: [require("../images/sweets-2.jpeg")],
        },
        {
          name: "Cake Item",
          price: "$5",
          image: [require("../images/cake-2.jpeg")],
        },
        {
          name: "Dougnut Item",
          price: "$5",
          image: [require("../images/doughnut-2.jpeg")],
        },
        {
          name: "Sweet Item",
          price: "$10",
          image: [require("../images/sweets-3.jpeg")],
        },
        {
          name: "Cupcake Item",
          price: "$10",
          image: [require("../images/cupcake-3.jpeg")],
        },
        {
          name: "Cake Item",
          price: "$15",
          image: [require("../images/cake-3.jpeg")],
        },
        {
          name: "Dougnut Item",
          price: "$15",
          image: [require("../images/doughnut-3.jpeg")],
        },
      ],
    };
  },
  computed: {
filteredData() {
 return this.datas.filter((data) =>{
return data.name.match(this.search)
 });

}
  },
// mounted() {
//   console.log(this.filteredData.length)
// }
};
</script>

<style scoped>
.row {
  display: flex;
  margin-right: -15px;
  margin-left: -15px;
}
.search {
  margin-left: 680px;
  margin-right: 180px;
  width: 100%;
  max-width: 25%;
  text-align: left;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
}
@media (max-width: 820px){
  .search {
    margin-left: 200px;
    max-width: 50%;
    
  }
}
@media (max-width: 420px){
  .search {
    margin-left: 80px;
    max-width: 50%;
    
  }
}
form {
  display: block;
  margin-top: 0em;
}
.input-group {
  display: flex;
}
.form-input {
  display: flex;
}

.input-icon {
  background: var(--mainPink);
  color: var(--mainBlack);
  margin-right: -1px;
  align-items: center;
  padding: 0.375rem 0.75rem;
  margin-bottom: 0;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  color: #495057;
  text-align: center;
  border: 1px solid #ced4da;
  border-radius: 0.25rem;
}
.las {
  color: var(--mainBlack);
  display: inline-block;
  font-size: 1rem;
  line-height: 1;
  font-weight: 900;
}
.form-control {
  display: block;
  width: 100%;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  color: #495057;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ced4da;
  border-radius: 0.25rem;
  transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.food-card {
  margin-bottom: 2rem;
  margin-top: 3rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  max-width: 75%;
  margin-left: 210px;
}
@media (max-width: 820px) {
  .food-card{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
   max-width: 75%;
   margin-left: 40px;
  }
}
@media (max-width: 420px) {
  .food-card{
  display: grid;
  grid-template-columns: repeat(1, 1fr);
   max-width: 75%;
   margin-left: -6px;
  }

}
.card {
  margin-left: 40px;
  background-color: #fff;
  background-clip: border-box;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.25rem;
  margin-bottom: 30px;
  max-width: 100%;
}
.img-container {
  position: relative;
  overflow: hidden;
  cursor: pointer;
}
.store-img {
  transition: all 1s ease-in-out;
}
.card-img-top {
  width: 100%;
  border-top-left-radius: calc(0.25rem - 1px);
  border-top-right-radius: calc(0.25rem - 1px);
}
img {
  /* width: 50%; */
  vertical-align: middle;
  border-style: none;
}
.store-item-icon {
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 0.75rem;
  background: var(--mainYellow);
  border-top-left-radius: 1rem;
  transition: all 1s ease-in-out;
  transform: translate(100%, 100%);
}
.card-body {
  flex: 1 1 auto;
  padding: 1.25rem;
}
.card-text {
  display: flex;
}
h5{
  font-size: 16px;
}
</style>
