<template>
  <section class="banner">
    <div class="banner__project">
      <h1 class="banner__project__text-h1">Our Project</h1>
      <p class="banner__project__text-p">Home/ Project</p>
    </div>
  </section>
  <section class="tags">
    
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
}
.banner {
  background: url("/src/assets/img/banner_project.png"),
    lightgray 50% / cover no-repeat;
  width: 100%;
  height: 30vh;
  background-size: cover;
  position: relative;
}

.banner__project {
  position: absolute;
  bottom: 0;
  left: 35vw;
  width: 100px;
  height: 17px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 41px 125px 41px 125px;
  border-radius: 37px 37px 0px 0px;
  background: rgb(255, 255, 255);
}

@media(max-width: 600px){
  .banner__project {
    flex-direction: row;
    gap: 20%;
    left: 20vw;
    width: 30px;
    height: 10px;
    padding: 20px 80px;
    border-radius: 22px 22px 0px 0px;
}
.banner__project__text-h1{

  font-size: 15px;
}
.banner__project__text-p{
  font-size: 10px;
}
.banner {
  height: 20vh;
  margin-top: 7px;
}
}
@media(max-width: 280px){
  .banner__project {
    max-width: 1px;
    max-height: 1px;
    padding: 20px 65px;
    border-radius: 14px 14px 0px 0px;
    gap: 5px
}
}
</style>
