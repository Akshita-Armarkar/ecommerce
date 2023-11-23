<template>
    <div class="navbar">
        <div class="content">
            <div class="left">
                <img :src=hamburger alt="" srcset="">
            </div>
            <div class="centre">
                <img src="" alt="LOGO HERE">
            </div>
            <div class="right">
                <img :src=search alt="" srcset="">
                <img :src=wishlist alt="" srcset="">
                <img :src=cart alt="" srcset="">
                <img :src=profile alt="" srcset="">
            </div>
        </div>
    </div>
</template>
<script>
import cart from '../../assets/svg/cart.svg'
import search from '../../assets/svg/search.svg'
import hamburger from '../../assets/svg/hamburger.svg'
import profile from '../../assets/svg/profile.svg'
import wishlist from '../../assets/svg/wishlist.svg'

export default {
    name: 'navbar',
    data() {
        return {
             cart,
             search,
             hamburger,
             profile,
             wishlist
        };
    },
}
</script>
<style scoped lang="scss">
.navbar {
    background: #FFF;
    box-shadow: 0px 8px 21px 0px rgba(0, 0, 0, 0.16);
    padding: 0px 20px;
    & > .content{
        height: 88px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: var( --layout-width );
        margin: 0 auto;
        & > .right {
            display: flex;
            justify-content: space-between;
            gap: 15px;
        }
    }
}
</style>