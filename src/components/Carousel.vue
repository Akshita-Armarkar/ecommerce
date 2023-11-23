<script lang="jsx">
import image7 from '../assets/png/categories/image7.jpg'
import image8 from '../assets/png/categories/image8.jpg'
import image9 from '../assets/png/categories/image9.jpg'
import image10 from '../assets/png/categories/image10.jpg'
import image11 from '../assets/png/categories/image11.jpg'
import image12 from '../assets/png/categories/image12.jpg'

const titles = [
    "Men's T-Shirts",
    "Women's Wear",
    "Winter Collections",
    "Hooded T-Shirts",
    "Polo Neck T-Shirts",
    "Full Sleeves T-Shirts"
]

export default {
    data(){
        return {
            categories : [
                image7, image8, image9, image10, image11, image12].map( ( img, index ) => ( {
                    img,
                    title: titles[ index ]
                } ) ),
        }
    },
    render(){
        return (
            <div class="categories">
                {
                    this.categories.map( ( { img, title } ) => ( 
                        <div key={ title } class="category">
                            <img src={ img } alt="category" loading="lazy" />
                            <div class="title">{ title }</div>
                        </div>
                    ))
                }
            </div>
        )
    }
}

</script>

<style scoped lang="scss">
    .categories{
        width: 100%;
        max-width: var( --layout-width );
        margin: 68px auto 0;
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-evenly;
        align-items: center;
        column-gap: 20px;
    }

</style>