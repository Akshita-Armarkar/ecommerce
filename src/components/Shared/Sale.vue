<script lang="jsx">
    export default {
        props: {
            sale: {
                type: Object
            }
        },
        render(){
            return (
                <div class='sale' style={ { background: this.sale.background } }>
                    <img src={ this.sale.image } loading="lazy" />
                    <div class='info'>Hurry Up!</div>
                    <div class='discount'>{ this.sale.discount }% OFF</div>
                    <div class='info'>Sale</div>
                    <button class='action'>shop now</button>
                </div>
            )
        }
    }
</script>

<style scoped lang="scss">
    .sale{
        text-align: center;
        & > img{
            width: 172px;
            aspect-ratio: 1/1;
        }
        & > .info{
            font-family: Playfair Display;
            font-size: 36px;
            font-weight: 600;
        }
        & > .discount{
            font-family: Playfair Display;
            font-size: 84px;
            font-weight: 600;
        }

        & > button.action{
            outline: none;
            border: 1px solid #fff;
            background: transparent;
            color: #FFF;       
            padding: 14px 36px;
            text-transform: uppercase;     
            font-size: 16px;
            font-weight: 500;
            margin-bottom: 54px;
        }

        & > img:first-child{
            margin-top: 54px;
        }
        & > *:nth-child( 2 ){
            margin-top: 48px;
        }
        & > *:nth-child( n + 3 ){
            margin-top: 22px;
        }
        
    }
</style>