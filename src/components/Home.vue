<template>
  <div class="card-section">
    <div class="container">
      <div class="card-block bg-white mb30">
        <div class="row">
          <div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
            <div class="section-title mb-0">
              <h2>Hello</h2>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
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
h1,
h2,
h3,
h4,
h5,
h6 {
  color: #25292a;
  margin: 0px 0px 10px 0px;
  font-family: "Overpass", sans-serif;
  font-weight: 700;
  letter-spacing: -1px;
  line-height: 1;
}
h1 {
  font-size: 34px;
}
h2 {
  font-size: 28px;
  line-height: 38px;
}
h3 {
  font-size: 22px;
  line-height: 32px;
}
h4 {
  font-size: 20px;
}
h5 {
  font-size: 17px;
}
h6 {
  font-size: 12px;
}
p {
  margin: 0 0 20px;
  line-height: 1.7;
}
p:last-child {
  margin: 0px;
}

.card-section {
  position: relative;
  bottom: 60px;
}
.card-block {
  padding: 80px;
}
.section-title {
  margin-bottom: 60px;
}
</style>