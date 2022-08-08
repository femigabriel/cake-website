<template>
  <div class="main">
    <div class="text-center">
      <h1 class="text">
        Welcome to <strong class="banner-title">Grandma's</strong>
      </h1>
      <span class="btn">Explore</span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.main {
  min-height: calc(100vh - 76px);
  background: linear-gradient(var(--yellowTrans), var(--yellowTrans)),
    url(../images/headerBcg.jpeg) center/cover fixed no-repeat;
  align-items: center;
  justify-content: center;
  display: flex;
  margin-right: -15px;
  margin-left: -15px;
}
@media (max-width: 820px) {
  .main {
    min-height: calc(100vh - 76px);
    align-items: center;
    justify-content: center;
    display: flex;
    margin-right: -15px;
    margin-left: -15px;
  }
}
.text-center {
  color: var(--mainWhite);
  text-align: center;
  justify-items: center;
  padding-right: 15px;
  padding-left: 15px;
}
@media (max-width: 820px) {
  .text-center {
    margin-bottom: 8.5rem;
    margin-right: 1.5rem;
  }
}
h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
  font-family: inherit;
  font-weight: 500;
  line-height: 1.2;
  color: inherit;
}
.banner-title {
  color: var(--mainPink);
  font-size: 4rem;
  font-weight: bolder;
}
span {
  font-size: 1.7rem;
  color: var(--mainBlack);
  text-decoration: none;
}
span:hover {
  background: var(--mainBlack);
  color: var(--mainWhite);
}
.btn {
  /* font-size: .9rem; */
  color: var(--mainBlack);
  border: 0.2rem solid var(--mainBlack);
  text-transform: uppercase;
  display: inline-block;
  font-weight: 400;
  text-align: center;
  padding: 0.375rem 0.75rem;
  line-height: 1.5;
  border-radius: 0.25rem;
  cursor: pointer;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
    border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}
</style>
