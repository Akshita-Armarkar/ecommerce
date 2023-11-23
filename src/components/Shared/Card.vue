<script lang="jsx">
    export default {
        props: {
            product: {
                type: Object
            }
        },
        render(){
            return (
                <div class='card'>
                    <img src={ this.product.image } />
                    <div class='footer'>
                        <div class='title'>{ this.product.title }</div>
                    </div>
                </div>
            )
        }
    }
</script>

<style scoped lang="scss">
    .card{
        position: relative;
        & > img{
            width: 100%;
            aspect-ratio: 5/6;
        }
        & > .footer{
            position: absolute;
            inset: auto 0 0 0;
            height: 70px;
            backdrop-filter: blur( 32px );
            .title{
                color: #FFF;
                font-family: Playfair Display;
                font-size: 20px;
                font-weight: 600;
                text-align: center;
                line-height: 70px;
                vertical-align: middle;
            }
        }
    }
</style>