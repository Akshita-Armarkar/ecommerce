<template>
    <div class="top-bar">
        <div class="content">
            <p>Welcome to Our Store Hiscraves</p>
            <div class="right">
                <img :src=phone alt="tel-phone" loading="lazy" >
                <span>Call Us: 1234567890</span>
            </div>
        </div>
    </div>
</template>
<script>
import phone from '../../assets/svg/phone.svg'
export default {
    name: 'TopNavbar',
    data() {
        return {
            phone
        };
    }
}
</script>
<style scoped lang="scss">
.top-bar{
    background-color: #1F1F1F;
    color: #FFF;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    padding: 0px 20px;
    & > .content{
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 48px;
        max-width: var( --layout-width );
        margin: auto;
        & > .right{
            display: flex;
            align-items: center;
            justify-content: space-around;
            gap: 10px;
        }
    }
}
</style>