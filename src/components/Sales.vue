<script lang="jsx">
    import { sales } from '../data/sales';
    import Sale from './Shared/Sale.vue';

    export default {
        data(){
            return {
                sales
            }
        },
        render(){
            return (
                <div class='sales'>
                    {
                        this.sales.map( sale => <Sale sale={ sale } key={ sale.id } /> )
                    }
                </div>
            )
        }
    }
</script>

<style scoped lang="scss">
    .sales{
        width: 100%;
        max-width: var( --layout-width );
        margin: 68px auto 0;
        display: flex;
        flex-flow: row nowrap;
        justify-content: center;
        column-gap: 24px;
        & > *{
            flex-grow: 1;
        }
    }
</style>