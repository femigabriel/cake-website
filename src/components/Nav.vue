<template>
  <nav>
    <div class="navbar">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Store</a>
        </li>
        <li>
          <div class="nav-info">
            <div class="nav-info-items">
              <!-- single info -->
              <div class="nav-numb">
                <div class="flex">
                  <i class="las la-phone"></i>
                  <p class="">+ 123 456 789</p>
                </div>
              </div>

              <div class="nav-prices">
                <div class="flex">
                  <i class="las la-shopping-cart"></i>
                  <p class="">
                    <span id="item-count">2 </span> items - $<span
                      class="item-total"
                      >10.49</span
                    >
                  </p>
                </div>
              </div>
            </div>
            <!-- end of single info -->
          </div>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
/* h3 {
  margin: 40px 0 0;
} */
nav {
  align-items: center;
  justify-items: center;
  display: flex;
}
.navbar {
  /* display: flex; */
  align-items: center;
  justify-content: center;
  margin: 20px 320px;
}
@media (max-width: 920px) {
  .navbar {
    /* display: none; */
    margin: 20px 0px;
  }
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  font-size: 1.5rem;
  padding: 0.5rem 2rem;
  display: inline-block;
  margin: 0 -10px;
  transition: all 0.5s ease-in-out;
}
@media (max-width: 920px) {
  li {
    display: block;
    margin: 0 100px;
  }
}
a {
  color: var(--mainPink);
  text-decoration: none;
  background-color: transparent;
}
a:hover {
  color: var(--mainBlack);
}
@media (max-width: 920px) {
  .nav-info {
    display: flex;
    flex-direction: column;
  }
}

.nav-info-items {
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  display: flex;
  margin: 0px 300px;
}
@media (max-width: 820px) {
  .nav-info-items {
    display: flex;
    flex-direction: column;
    margin: 0px 0px;
  }
}
.flex {
  display: flex;
  padding: 0.5rem 2rem;
  margin: 0px -20px;
}
@media (max-width: 820px) {
  .nav-prices {
    margin-right: -10px;
  }
}
.nav-prices {
  border: 1px solid var(--mainBlack);
  margin: 0px 50px;
  color: var(--mainBlack);
  padding-right: 15px;
}
.nav-prices:hover {
  background: #ef7998;
  color: aliceblue;
  border: 1px solid gray;
}
@media (max-width: 820px) {
  .nav-prices {
    margin: 0px 0px;
    /* padding-right: 15px;   */
  }
}
.nav-numb {
  margin: 0px -20px;
}
.las {
  margin: 2px 8px;
  color: var(--mainBlack);
  font-size: 15px;
}
</style>
