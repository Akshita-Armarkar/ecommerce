<script lang="jsx">
import Product from './Shared/Product.vue'
import products from '../data/products';



export default {
    name: 'Collection',
    props: {
        title: String,
        initialRows: {
            type: Number,
            default: 1
        }
    },
    data() {
        return {
            products
        }
    },
    render() {
        return (
            <div class="collection">
                <div class='title'>
                    <h3>{ this.title }</h3>
                </div>
                <div class='products'>
                    {
                        this.products.slice( 0, this.initialRows * 4 ).map((product) => (
                            <Product product={ product } key={ product.id } />
                        ))
                    }
                </div>
                <button class='view-all'>View All</button>
            </div>
        )
    }
}

</script>

<style scoped lang="scss">
.collection {
    width: 100%;
    max-width: var(--layout-width);
    margin: 68px auto 0;
    & > .title{
        display: flex;
        flex-flow: row nowrap;
        justify-content: center;
        align-items: center;
        column-gap: 30px;
        margin-bottom: 48px;
        & > h3{
            font-family: Playfair Display;
            font-size: 36px;
            font-style: normal;
            font-weight: 600;
            line-height: normal;
            margin: 0;
        }

        &:before, &:after{
            content: '';
            display: block;
            background: #FFC7D1;
            height: 1px;
            flex-grow: 1;
        }
    }
    & > .products{
        display: grid;
        grid-template-columns: repeat( 4, minmax( 0, 1fr ) );
        column-gap: 20px;
        row-gap: 48px;
    }

    & > button.view-all{
        display: block;
        outline: none;
        border: none;
        background: #770015;
        color: #fff;
        padding: 14px 45px;
        text-transform: uppercase;
        margin: 48px auto 0;
    }
}
</style>