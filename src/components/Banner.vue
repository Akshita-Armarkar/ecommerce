<script lang="jsx">

export default {
    props: {
        image: String,
        addSpace:{
            type: Boolean,
            default: true
        }
    },
    render(){
        return (
            <div class="banner" style={ { marginTop: this.addSpace ? '68px' : '0'} }>
                <img src={ this.image } alt="" srcset="" loading="lazy" />
            </div>
        )
    }
}

</script>

<style scoped lang="scss">
    .banner{
        width: 100%;
        height: max-content;
        img{
            width: 100%;
            height: auto;
        }
    }
</style>