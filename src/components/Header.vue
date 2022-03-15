<template>
  <div class="page-header">
    <div class="container">
      <div class="row">
        <div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
          <div class="page-caption">
            <h1 class="page-title">SGUnited Traineeship Programmes</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="program-bar">
    <div class="container">
      <div class="text">
        Join Our Programs
        <button type="button" class="btn btn-default">Find Out More</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
body {
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
  font-family: "Overpass", sans-serif;
  letter-spacing: 0px;
  font-size: 17px;
  color: #8d8f90;
  font-weight: 400;
  line-height: 32px;
  background-color: #edefef;
}

a:focus,
a:hover {
  text-decoration: none;
  color: #f85759;
}

.page-header {
  background: url(https://easetemplate.com/free-website-templates/hike/images/pageheader.jpg)
    no-repeat;
  position: relative;
  background-size: cover;
}
.page-caption {
  padding-top: 170px;
  padding-bottom: 174px;
}
.page-title {
  font-size: 46px;
  line-height: 1;
  color: #fff;
  font-weight: 600;
  text-align: center;
}

.program-bar {
  padding: 1.75rem 0;
  font-size: 1.25em;
  background-color: #0074b9 !important;
  color: #fff !important;
  text-align: center;
}

.btn{
    margin-left: 50px;
    background-color: #fff;
    color: #0074b9!important;
    line-height: 40px;
    font-size: 15px;
    padding: 0 30px;
}
</style>