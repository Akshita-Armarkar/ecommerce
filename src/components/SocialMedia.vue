<script lang="jsx">
import address from '../assets/svg/address.svg'
import telephone from '../assets/svg/telephone.svg'
import email from '../assets/svg/email.svg'
import facebook from '../assets/svg/facebook.svg'
import instagram from '../assets/svg/instagram.svg'
import twitter from '../assets/svg/twitter.svg'
import linkedin from '../assets/svg/linkedin.svg'
import pinterest from '../assets/svg/pinterest.svg'

export default {
    render(){
        return (
            <div class="social">
                <div class='box'>
                    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries....</p>
                    <div><img src={facebook}/><img src={twitter}/><img src={instagram}/><img src={linkedin}/><img src={pinterest}/></div>
                </div>
                <div class='box'>
                    <span>ONLINE SHOPPING</span>
                    <ul>
                        <li>Men’s T-Shirts</li>
                        <li>Women’s Wear</li>
                        <li>Winter Collections</li>
                        <li>Hooded T-Shirts</li>
                        <li>Streetwear Collections</li>
                    </ul>
                </div>
                <div class='box'>
                    <span>CUSTOMER POLICIES</span>
                    <ul>
                    <li>About Us</li>
                    <li>Terms & Conditions</li>
                    <li>Shipping & Returns Policy</li>
                    <li>Cancellation & Refund Policy</li>
                    <li>Contact Us</li>
                    </ul>
                </div>
                <div class='box'>
                    <span>STORE INFORMATION</span>
                    <ul>
                        <li><img src={address}/>Lorem Ipsum is simply dummy text of the printing and typesetting industry. </li>
                        <li><img src={telephone}/>Call Us: 1234567890</li>
                        <li><img src={email}/>Email Us: info@yourmail.com</li>
                       
                    </ul>
                </div>
            </div>
        )
    }
}

</script>

<style scoped lang="scss">
    .social{
        display: grid;
        grid-template-columns: 2fr 1fr 1fr 1fr; 
        width: 100%;
        gap: 4px;
        height: fit-content;
        background-color: #FFF;
        border: solid 1px grey;
        padding: 40px 77px;
        .box {
            align-self: self-start;
            color: var(--Primary-Color_1, #1C1C1C);
            font-family: Montserrat;
            font-size: 14px;
            font-style: normal;
            font-weight: 500;
            line-height: 28px;
            padding: 4px;
            margin: 4px;
            div {
                display: flex;
                align-items: center;
                justify-content: flex-start;
                gap: 8px;
            }
            span{
                color: #770015;
                font-family: Playfair Display;
                font-size: 18px;
                font-style: normal;
                font-weight: 600;
                line-height: normal;
            }
            ul{
                list-style: none;
                color: var(--Primary-Color_1, #1C1C1C);
                font-family: Montserrat;
                font-size: 14px;
                font-style: normal;
                font-weight: 500;
                line-height: 34px;
                padding: 0;
                li{
                    img {
                        vertical-align: middle;
                        padding: 3px;
                    }
                }
            }
        }
    }
</style>