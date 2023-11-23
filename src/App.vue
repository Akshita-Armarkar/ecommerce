<script lang="jsx">
import Header from './components/Header';
import Banner from './components/Banner.vue';
import Carousel from './components/Carousel.vue';
import Highlights from './components/Highlights.vue';
import Collection from './components/Collection.vue';
import Cards from './components/Cards.vue';
import Sales from './components/Sales.vue';
import Subscribe from './components/Subscribe.vue';
import Footer from './components/Footer.vue';
import SocialMedia from './components/SocialMedia.vue';

// images:
import banner from './assets/png/banner.png'
import banner2 from './assets/png/banner2.jpg';
import banner3 from './assets/png/banner3.jpeg';

export default {
  name: 'App',
  render(){
    return (
      <>
      <Header />
      <Banner image={ banner } addSpace={ false }/>
      <Carousel />
      <Highlights />
      <Collection title='Trending T-Shirts' initialRows={2}/>
      <Collection title='Featured Products'/>
      <Banner image={ banner2 } />
      <Collection title='New Products'/>
      <Collection title='Best Selling Products'/>
      <Cards/>
      <Banner image={ banner3 } />
      <Sales />
      <Subscribe />
      <SocialMedia/>
      <Footer/>
      </>
    )
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap');
  *{
    box-sizing: border-box;
  }
  body{
    width: 100%;
    margin: 0;
    padding: 0;
    font-family: Montserrat;
    --layout-width: 1120px;
  }
</style>
