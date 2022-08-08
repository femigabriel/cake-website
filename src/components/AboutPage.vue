<template>
  <section class="about-page" id="about">
    <div class="container">
      <div class="row">
        <div class="content">
          <h1 class="text-capitalize">
            About <strong class="banner-title">Us</strong>
          </h1>
          <p class="">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit,
            aliquam voluptas beatae vitae expedita consectetur nesciunt quia
            deserunt asperiores facere fuga dicta fugiat corrupti et omnis porro
            at dolorum! Ad!
          </p>
          <a href="#" class="btn">Explore</a>
        </div>
        <div class="about-image">
          <div class="about-img">
            <img src="../images/sweets-1.jpeg" class="img-fluid" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
section {
  display: block;
}
.about-page {
  padding-bottom: 3rem;
  padding-top: 3rem;
}
.container {
  width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}
@media (max-width: 820px) {
  .container {
    width: 85%;
    margin-left: 5px;
  }
}

@media (max-width: 420px) {
  .container {
    width: 85%;
    margin-left: 15px;
  }
}

.row {
  display: flex;
  margin-right: -15px;
  margin-left: -15px;
}
@media (max-width: 420px){
  .row {
  display: flex;
  flex-direction: column;
  
}
}
.content {
  margin-right: auto;
  padding-right: 15px;
  padding-left: 165px;
  margin-bottom: 3rem;
  margin-top: 3rem;
}
@media (max-width: 820px) {
  .content {
    padding-left: 75px;
  }
}
@media (max-width: 420px){
    .content {
    padding-left: 35px;
  }
}
.content h1 {
  font-size: 30px;
  margin-bottom: 0.5rem;
  font-weight: 500;
  line-height: 1.2;
  color: inherit;
}

.banner-title {
  color: var(--mainPink);
  font-size: 48px;
  font-weight: 700;
}
.content p {
  color: #6c757d;
  margin-bottom: 1.5rem;
  margin-top: 1.5rem;
  width: 38em;
  font-size: 12px;
}
@media (max-width: 820px) {
  .content p {
    width: 20em;
  }
}
@media (max-width: 420px){
  .content p {
     width: 27em;
  }
}
.btn {
  color: #6c757d;
  border: 0.2rem solid var(--mainBlack);
  padding: 0.375rem 0.75rem;
  cursor: pointer;
  font-size: 17px;
  font-weight: 400;
  line-height: 18px;
}
.btn:hover {
  background: var(--mainBlack);
  color: var(--mainPink);
}
a {
  text-decoration: none;
}
.about-image {
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 3rem;
  margin-top: 3rem;
  align-self: center;
  /* width: 100%; */
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
}
.about-img {
  border: 10px solid var(--mainYellow);
}
.about-img img {
  position: relative;
  width: 46em;

  /* width: 120px; */
}
@media (max-width: 820px){
  .about-image{
        max-width: 85%;
  }
  .about-img img{
    max-width: 350px;
  }
}
@media (max-width: 420px){
  .about-image{
        max-width: 100%;
        padding-left: 50px;
      
  }
  .about-img img{
    max-width: 260px;
  }
}
</style>
