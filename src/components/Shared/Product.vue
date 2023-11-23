<script lang="jsx">
import cartIcon from '../../assets/svg/cartRed.svg';
import wishlistIcon from '../../assets/svg/wishlistRed.svg';
import shareIcon from '../../assets/svg/shareRed.svg';
export default {
    props: {
        product: {
            type: Object
        }
    },
    render(){
        const { image, title, discountPrice, actualPrice } = this.product;
        return (
            <div class="product">
                <div class="product-image">
                    <img src={ image } alt="product" />
                    <div class="actions">
                        <button>
                            <img src={ cartIcon } loading="lazy"  />
                        </button>
                        <button>
                            <img src={ wishlistIcon } loading="lazy" />
                        </button>
                        <button>
                            <img src={ shareIcon } loading="lazy" />
                        </button>
                    </div>
                </div>
                <div class="title">{title}</div>
                <div class='prices'>{discountPrice}<span>{actualPrice}</span></div>
                <div class='sizes'>
                    <span>S</span>
                    <span>M</span>
                    <span>L</span>
                    <span>XL</span>
                    <span>XXL</span>
                </div>
            </div>
        )
    }
}

</script>
<style scoped lang="scss">
    .product{

        .product-image{
            overflow: hidden;
            position: relative;
            line-height: 0;
            & .actions{
                position: absolute;
                inset: 0 0 0 0;
                backdrop-filter: blur( 5px );
                background: rgba(31, 31, 31, 0.30);
                display: flex;
                flex-flow: row nowrap;
                justify-content: center;
                align-items: center;
                column-gap: 16px;
                visibility: hidden;
                button{
                    border: none;
                    outline: none;
                    background: none;
                    padding: 0;
                    margin: 0;
                    cursor: pointer;
                }
            }
            &:hover .actions{
                visibility: visible;
            }
        }
        .title {
            color: var(--Primary-Color_1, #1C1C1C);
            text-align: center;
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
            padding: 4px;
        }

        .prices {
            color: #1F1F1F;
            text-align: center;
            padding: 4px;
            font-family: Montserrat;
            font-size: 18px;
            font-style: normal;
            font-weight: 700;
            line-height: 18px;

            span {
                color: #F00;
                font-family: Montserrat;
                font-size: 10px;
                font-style: normal;
                font-weight: 400;
                line-height: 18px;
                text-decoration: line-through;
            }
        }

        .sizes {
            font-size: 14px;
            font-style: normal;
            font-weight: 500;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1em;
            span {
                display: inline-block;
                border: 1px solid #E6E6E6;
                min-width: 36px;
                text-align: center;
                padding: 10px 0;
            }
        }
    }
</style>