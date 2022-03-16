<template>
  <div class="page-header" id="header">
    <div class="row">
      <div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
        <div class="page-caption">
          <h1
            class="
              page-title
              animate__animated animate__bounce animate__infinite
            "
          >
            Welcome
          </h1>
          <h2
            class="
              page-title2
              animate__animated animate__bounce animate__infinite
            "
          >
            SGUnited
          </h2>
          <button
            @click="showImage"
            type="button"
            class="btn btn-outline-light"
          >
            Enter
          </button>
        </div>
      </div>
    </div>
  </div>
  <div id="photo" class="photo" v-if="showPhoto" >
    <img class="responsive" :src="image"/>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      showPhoto: false,
      image: require("@/assets/SgUnited2.jpeg"),
    };
  },
  methods: {
    showImage() {
      document.getElementById("header").style.display = "none";
      this.showPhoto = true;
    },
  },
};
</script>

<style scoped>
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
  text-align: center;
}
.page-title {
  font-size: 10vw;
  line-height: 1;
  color: #fff;
  font-weight: 600;
  text-align: center;
}
.page-title2 {
  font-size: 5vw;
  line-height: 1;
  color: #fff;
  font-weight: 600;
  text-align: center;
}

.btn {
  line-height: 40px;
  font-size: 20px;
  padding: 0 30px;
  margin-top: 20px;
}
.responsive{
  padding-top: 50px;
  width: 75%;
  height: auto;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.responsive:hover{
  width: 90%;
}

</style>