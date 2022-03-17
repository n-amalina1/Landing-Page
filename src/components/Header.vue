<template>
  <v-row no-gutters justify="center" @click="showImage">
    <v-img
      lazy-src="https://picsum.photos/id/11/1280/720"
      src="https://bad.src/not/valid"
      height="100vh"
      width="100vw"
    >
      <template v-slot:placeholder>
        <v-container class="grow fill-height d-flex flex-column flex-nowrap">
          <v-row class="shrink"> </v-row>
          <v-row class="shrink">
            <v-col cols="12">
              <v-card
                elevation="2"
                class="pa-3 animate__animated animate__bounce animate__infinite"
                ><h1 class="text-center">Hello</h1>
                <h2 class="text-center">Generation SG</h2></v-card
              >
            </v-col>
          </v-row>
          <v-row class="shrink"> </v-row>
        </v-container>
      </template>
    </v-img>
    <!-- <div id="photo" class="photo slide-in-elliptic-top-fwd" v-if="showPhoto">
      <img class="responsive" src="@/assets/SgUnited2.jpeg" />
    </div> -->
  </v-row>
</template>

<script>
import confetti from "canvas-confetti";

export default {
  name: "Header",
  data: () => ({
    model: 0,
    colors: ["primary", "secondary", "yellow darken-2", "red", "orange"],
    showPhoto: false,
  }),
  mounted: function () {
    this.fireConfetti();
    // this.showImage();
  },
  methods: {
    fireConfetti() {
      var duration = 15 * 1000;
      var animationEnd = Date.now() + duration;
      var defaults = { startVelocity: 30, spread: 360, ticks: 60, zIndex: 0 };

      function randomInRange(min, max) {
        return Math.random() * (max - min) + min;
      }

      var interval = setInterval(function () {
        var timeLeft = animationEnd - Date.now();

        if (timeLeft <= 0) {
          return clearInterval(interval);
        }

        var particleCount = 50 * (timeLeft / duration);
        confetti(
          Object.assign({}, defaults, {
            particleCount,
            origin: { x: randomInRange(0.1, 0.3), y: Math.random() - 0.2 },
          })
        );
        confetti(
          Object.assign({}, defaults, {
            particleCount,
            origin: { x: randomInRange(0.7, 0.9), y: Math.random() - 0.2 },
          })
        );
      }, 250);
    },
    showImage() {
      document.getElementById("header").style.display = "none";
      this.showPhoto = true;
    },
  },
};
</script>

<style scoped>
/* a:focus,
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
.responsive {
  padding-top: 50px;
  width: 75%;
  height: auto;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.scale-in-center {
  -webkit-animation: scale-in-center 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94)
    both;
  animation: scale-in-center 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
}

@-webkit-keyframes scale-in-center {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}
@keyframes scale-in-center {
  0% {
    -webkit-transform: scale(0);
    transform: scale(0);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
}

.jello-horizontal {
  -webkit-animation: jello-horizontal 0.9s both;
  animation: jello-horizontal 0.9s both;
}

@-webkit-keyframes jello-horizontal {
  0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
  30% {
    -webkit-transform: scale3d(1.25, 0.75, 1);
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    -webkit-transform: scale3d(0.75, 1.25, 1);
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    -webkit-transform: scale3d(0.95, 1.05, 1);
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    -webkit-transform: scale3d(1.05, 0.95, 1);
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}
@keyframes jello-horizontal {
  0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
  30% {
    -webkit-transform: scale3d(1.25, 0.75, 1);
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    -webkit-transform: scale3d(0.75, 1.25, 1);
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    -webkit-transform: scale3d(0.95, 1.05, 1);
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    -webkit-transform: scale3d(1.05, 0.95, 1);
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}

.slide-in-elliptic-top-fwd {
  -webkit-animation: slide-in-elliptic-top-fwd 0.7s
    cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
  animation: slide-in-elliptic-top-fwd 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94)
    both;
}

@-webkit-keyframes slide-in-elliptic-top-fwd {
  0% {
    -webkit-transform: translateY(-600px) rotateX(-30deg) scale(0);
    transform: translateY(-600px) rotateX(-30deg) scale(0);
    -webkit-transform-origin: 50% 100%;
    transform-origin: 50% 100%;
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0) rotateX(0) scale(1);
    transform: translateY(0) rotateX(0) scale(1);
    -webkit-transform-origin: 50% 1400px;
    transform-origin: 50% 1400px;
    opacity: 1;
  }
}
@keyframes slide-in-elliptic-top-fwd {
  0% {
    -webkit-transform: translateY(-600px) rotateX(-30deg) scale(0);
    transform: translateY(-600px) rotateX(-30deg) scale(0);
    -webkit-transform-origin: 50% 100%;
    transform-origin: 50% 100%;
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0) rotateX(0) scale(1);
    transform: translateY(0) rotateX(0) scale(1);
    -webkit-transform-origin: 50% 1400px;
    transform-origin: 50% 1400px;
    opacity: 1;
  }
} */
</style>
