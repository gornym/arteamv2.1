<template>
  <body id="carouselProducers">
    <div class="logos">
      <div class="logos-slide">
        <img alt="logo1" src="@/assets/1.webp" />
        <img alt="logo2" src="@/assets/2.webp" />
        <img alt="logo3" src="@/assets/3.webp" />
        <img alt="logo4" src="@/assets/4.webp" />
        <img alt="logo5" src="@/assets/5.webp" />
        <img alt="logo6" src="@/assets/6.webp" />
        <img alt="logo7" src="@/assets/7.webp" />
        <img alt="logo8" src="@/assets/8.webp" />
        <img alt="logo9" src="@/assets/9.webp" />
        <img alt="logo10" src="@/assets/10.webp" />
        <img alt="logo11" src="@/assets/11.webp" />
        <img alt="logo12" src="@/assets/12.webp" />
        <img alt="logo13" src="@/assets/13.webp" />
        <img alt="logo14" src="@/assets/14.webp" />
        <img alt="logo15" src="@/assets/15.webp" />
      </div>
      <div class="logos-slide">
        <img alt="logo1" src="@/assets/1.webp" />
        <img alt="logo2" src="@/assets/2.webp" />
        <img alt="logo3" src="@/assets/3.webp" />
        <img alt="logo4" src="@/assets/4.webp" />
        <img alt="logo5" src="@/assets/5.webp" />
        <img alt="logo6" src="@/assets/6.webp" />
        <img alt="logo7" src="@/assets/7.webp" />
        <img alt="logo8" src="@/assets/8.webp" />
        <img alt="logo9" src="@/assets/9.webp" />
        <img alt="logo10" src="@/assets/10.webp" />
        <img alt="logo11" src="@/assets/11.webp" />
        <img alt="logo12" src="@/assets/12.webp" />
        <img alt="logo13" src="@/assets/13.webp" />
        <img alt="logo14" src="@/assets/14.webp" />
        <img alt="logo15" src="@/assets/15.webp" />
      </div>

      <!-- <div class="logos-slide">
        <img alt="logo1" :src="logo1" />
        <img alt="logo2" :src="logo2" />
        <img alt="logo3" :src="logo3" />
        <img alt="logo4" :src="logo4" />
        <img alt="logo5" :src="logo5" />
        <img alt="logo6" :src="logo6" />
        <img alt="logo7" :src="logo7" />
        <img alt="logo8" :src="logo8" />
        <img alt="logo9" :src="logo9" />
        <img alt="logo10" :src="logo10" />
        <img alt="logo11" :src="logo11" />
        <img alt="logo12" :src="logo12" />
        <img alt="logo13" :src="logo13" />
        <img alt="logo14" :src="logo14" />
        <img alt="logo15" :src="logo15" />
      </div> -->
    </div>
  </body>
</template>

<script>
// import PocketBase from "pocketbase";
// export default {
//   data() {
//     return {
//       pb: new PocketBase("http://127.0.0.1:8090/"),
//       logo1: "",
//       logo2: "",
//       logo3: "",
//       logo4: "",
//       logo5: "",
//       logo6: "",
//       logo7: "",
//       logo8: "",
//       logo9: "",
//       logo10: "",
//       logo11: "",
//       logo12: "",
//       logo13: "",
//       logo14: "",
//       logo15: "",
//     };
//   },
//   methods: {
//     async loadImg(id, target) {
//       try {
//         const record = await this.pb.collection("producers_img").getOne(id, {
//           expand: "relField1,relField2.subRelField",
//         });

//         if (record.isVideo) {
//           this.videoSrc = `http://127.0.0.1:8090/api/files/producers_img/${id}/${record.img}`;
//         } else {
//           this[
//             target
//           ] = `http://127.0.0.1:8090/api/files/producers_img/${id}/${record.img}`;
//         }
//       } catch (error) {
//         console.error(`Błąd podczas ładowania `, error);
//       }
//     },
//     headerAnimationEnd() {
//       this.isHovered = true;
//     },
//   },
//   async mounted() {
//     await this.loadImg("nb9z77rm9vic4w9", "logo1");
//     await this.loadImg("tqkyc122rbpdaoc", "logo2");
//     await this.loadImg("nrmnx2xmcylhw1c", "logo3");
//     await this.loadImg("n7s7oypshl6gysg", "logo4");
//     await this.loadImg("xu6t5c9r8bjdoky", "logo5");
//     await this.loadImg("vpji09y7m9hfi59", "logo6");
//     await this.loadImg("gwsvgj7ouypb18d", "logo7");
//     await this.loadImg("29xvmq50exspg7t", "logo8");
//     await this.loadImg("r9vxkj1uzx3zal9", "logo9");
//     await this.loadImg("ejmj2xn3sf0f0wv", "logo10");
//     await this.loadImg("yk7kmzhoriycai8", "logo11");
//     await this.loadImg("eth45sp348vg5bl", "logo12");
//     await this.loadImg("mua1aywle9ffdfy", "logo13");
//     await this.loadImg("awuyvqk2pg1o04m", "logo14");
//     await this.loadImg("17nkixoxsuwys73", "logo15");
//   },
// };
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#carouselProducers {
  background: #f2f2f200;
}

@keyframes slide {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-100%);
  }
}

.logos {
  overflow: hidden;
  padding: 60px 0;
  background: rgb(96, 96, 96);
  white-space: nowrap;
  position: relative;
}

.logos:before,
.logos:after {
  position: absolute;
  top: 0;
  width: 250px;
  height: 100%;
  content: "";
  z-index: 2;
}

.logos:hover .logos-slide {
  animation-play-state: paused;
}

.logos-slide {
  display: inline-block;
  animation: 35s slide infinite linear;
}

.logos-slide img {
  height: 50px;
  margin: 0 40px;
}
</style>
