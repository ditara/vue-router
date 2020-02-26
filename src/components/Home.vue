<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">Dramaboo</h1>
            <h3 class="header-subtitle">The best drama information webpage for you</h3>
        </div>
        <div class="drama" v-for="(data, index) in drama" :value="data" :key="index">
            <div class="drama-item" @click="detaildrama(data.id)">
                <img v-bind:src="data.image" class="img-fluid img-drama" v-bind:alt="data">
            </div>
        </div>
        <div class="footer">
            <h5>MLG 2020 Ⓒ ditara All Rights Reserved</h5>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/Drama/at18.jpg';
import Img2 from '../assets/Drama/cly.jpg';
import Img3 from '../assets/Drama/drkim.jpg';
import Img4 from '../assets/Drama/hotel del luna.jpg';
import Img5 from '../assets/Drama/itaewon.jpg';
import Img6 from '../assets/Drama/love alarm.jpg';
import Img7 from '../assets/Drama/ruler.jpg';
import Img8 from '../assets/Drama/vagabond.jpg';

export default {
  data: () => ({
    drama: [
      { id: 1, image: Img1 },
      { id: 2, image: Img2 },
      { id: 3, image: Img3 },
      { id: 4, image: Img4 },
      { id: 5, image: Img5 },
      { id: 6, image: Img6 },
      { id: 7, image: Img7 },
      { id: 8, image: Img8 },
    ],
  }),
  methods: {
    detaildrama(dramaId) {
      this.$router.push({ name: 'detail', params: { id: dramaId } });
    },
  },
};
</script>
<style scoped>
    .container {
        width: auto;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(50px, auto);
    }
    .header {
        padding: 50px;
        grid-column: 1/5;
        background-color: #03a187;
        color: #fff;
        text-align: left;
    }
    .header-title {
      font-family: monospace;
      font-size: 70px;
      color: #dbcc9a;
    }
    .header-subtitle {
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        font-size: 20px;
        color: #fff;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #003d3f;
        color: #fff;
        text-align: center;
    }
    .drama {
        padding-top: 60px;
        padding-bottom: 60px;
        text-align: center;
        background-color: #ededed;
    }
    .img-drama {
        width: 250px;
        box-shadow: 0 20px 35px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .img-drama:hover{
        box-shadow: 0 40px 45px 0 rgba(0,0,0,0.2);
    }
</style>
