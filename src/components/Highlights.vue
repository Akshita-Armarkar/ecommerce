<script lang="jsx">
import image2 from '../assets/png/categories/image2.jpg'
import image3 from '../assets/png/categories/image3.jpg'
import image4 from '../assets/png/categories/image4.jpg'
import image5 from '../assets/png/categories/image5.jpg'
import image6 from '../assets/png/categories/image6.jpg'

export default {
    name: 'frameOne',
    data() {
        return {
            highlights : [image2, image3, image4, image5, image6].map( ( image, id ) => ( { image, id } ) )
        };
    },
    render(){

        return (
            <div class='highlights'>
                {
                    this.highlights.map( item => (
                        <div class='highlight'>
                            <img src={ item.image } alt='highlight' loading="lazy"  />
                        </div>
                    ) )
                }
            </div>
        )
    }
}
</script>
<style scoped lang='scss'>
    .highlights{
        width: 100%;
        max-width: var( --layout-width );
        margin: 68px auto 0;
        display: grid;
        grid-template-columns: repeat( 6, 1fr );
        grid-template-areas:
          "one one one two two two"
          "three three four four five five";
        column-gap: 20px;
        row-gap: 16px;
        & > div:nth-child( 1 ){
            grid-area: one;
        }  
        & > div:nth-child( 2 ){
            grid-area: two;
        }  
        & > div:nth-child( 3 ){
            grid-area: three;
        }  
        & > div:nth-child( 4 ){
            grid-area: four;
        }  
        & > div:nth-child( 5 ){
            grid-area: five;
        }  
    }
</style>