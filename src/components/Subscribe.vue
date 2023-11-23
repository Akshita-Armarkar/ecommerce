<script lang="jsx">
    import returnIcon from '../assets/svg/return.svg';
    import qualityIcon from '../assets/svg/quality.svg';
    import paymentIcon from '../assets/svg/payment.svg';
    import helplineIcon from '../assets/svg/helpline.svg';
    import shade1 from '../assets/svg/shade1.svg'
    import shade2 from '../assets/svg/shade2.svg'

    const benefits = [
        { image: returnIcon, title: '7 Days Return' },
        { image: qualityIcon, title: 'Quality Products' },
        { image: paymentIcon, title: 'Safe Payment' },
        { image: helplineIcon, title: '24x7 Helpline' },
    ]

    export default {
        render(){
            return (
                <div class="subscribe">
                    <div class="benefits">
                        {
                            benefits.map( ( { image, title } ) => (
                                <div class='benefit'>
                                    <img src={ image } alt='benefit'/>
                                    <div class='title'>{ title }</div>
                                </div>
                            ))
                        }
                    </div>
                    <div class='modal'>
                        <div class='title'>Subscribe to get updates on exciting offers & deals</div>
                        <div class='form'>
                            <input placeholder='Enter your email' />
                            <button>Subscribe</button>
                        </div>
                        <img src={ shade1 } alt='shade' class='shade1' />
                        <img src={ shade2 } alt='shade' class='shade2' />
                    </div>
                </div>
            )
        }
    }
</script>

<style scoped lang="scss">
    .subscribe{
        margin-top: 68px;
        & > .benefits{
            width: 100%;
            position: relative;
            display: flex;
            flex-flow: row nowrap;
            justify-content: center;
            align-items: center;
            background: #F5F4F2;
            padding: 40px 0;

            & > .benefit{
                padding: 0 77px;
                &:not(:last-child){
                    border-right: 1px solid #FFC7D1;
                }
            }
            &:before{
                content: '';
                display: block;
                width: 218px;
                aspect-ratio: 1/1;
                border-radius: 50%;
                background-color: #770015;
                position: absolute;
                top: 0;
                right: 0;
                transform: translate( 50%, -50% );
            }
            &:after{
                content: '';
                display: block;
                width: 218px;
                aspect-ratio: 1/1;
                border-radius: 50%;
                background-color: #770015;
                position: absolute;
                top: 0;
                left: 0;
                transform: translate( -50%, 50% );
            }
        }

        & > .modal{
            position: relative;
            width: 100%;
            max-width: var( --layout-width );
            min-height: 312px;
            margin: 68px auto;
            background: linear-gradient(97deg, #AB001E -6.23%, #770015 105.09%);
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;
            row-gap: 27px;
            & > .title{
                color: #FFF;
                text-align: center;
                font-family: Playfair Display;
                font-size: 36px;
                font-weight: 600;
                max-width: 65%;
            }

            & > .form{
                width: 100%;
                max-width: 60%;
                height: 68px;
                display: flex;
                flex-flow: row nowrap;
                input{
                    border: none;
                    background: rgba(255, 255, 255, 0.32);
                    color: white;
                    flex-grow: 1;
                    &::placeholder{
                        color: #FFF;
                        font-size: 16px;
                        font-weight: 500;
                        padding-left: 28px;
                    }
                }
                button{
                    outline: none;
                    border: none;
                    background-color: #fff;
                    color: #770015;
                    padding: 19px 21px;
                    font-family: Playfair Display;
                    font-size: 22px;
                    font-weight: 600;
                }
            }
            & > .shade1{
                position: absolute;
                top: 0;
                left: 0;
                height: 100%;
                width: auto;
            }

            & > .shade2{
                position: absolute;
                top: 0;
                right: 0;
                height: 100%;
                width: auto;
            }
        }
    }

</style>