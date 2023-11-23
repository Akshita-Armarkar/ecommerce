<template>
    <div class="middle">
    <div class="categories" v-for="category, index in categories" :key="index">
    <img :src=category alt="">
    </div>
    </div>
    <div class="bottom">
    <div class="categFlex" v-for="category, index in catgFlex" :key="index">
    <img :src=category alt="" loading="lazy" >
    </div>
    </div>
</template>
<script>
import image2 from '../assets/png/categories/image2.jpg'
import image3 from '../assets/png/categories/image3.jpg'
import image4 from '../assets/png/categories/image4.jpg'
import image5 from '../assets/png/categories/image5.jpg'
import image6 from '../assets/png/categories/image6.jpg'

export default {
    name: 'frameOne',
    data() {
        return {
            catgFlex : [image2, image3, image4, image5, image6]
        };
    }
}
</script>
<style>
.categories {
 display: inline-flex;
 flex-direction: column;
 justify-content: space-between;
 align-items: center;
 border: 1px white solid;
 border-radius: 170px;
 margin: 10px;
}
.categFlex {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
}

.categFlex img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

@media (max-width: 600px) {
  .categFlex {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>