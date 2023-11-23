<script lang="jsx">
import products from '../data/products2';
import Card from './Shared/Card.vue';

export default {
    data(){
        return {
            products: products.slice( 0, 6 )
        }
    },
    render(){
        return (
            <div class="cards">
                { this.products.map( product => <Card product={ product } key={ product.id } /> ) }
            </div>
        )
    }
}

</script>

<style scoped lang="scss">
    .cards{
        width: 100%;
        max-width: var(--layout-width);
        margin: 68px auto 0;
        display: grid;
        grid-template-columns: repeat( 3, minmax( 0, 1fr ) );
        gap: 20px;
    }
</style>