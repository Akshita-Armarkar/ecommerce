<script lang="jsx">
    import { defineComponent } from 'vue';
    import Bar from './bar.vue';
    import NavBar from './navbar.vue';
    export default defineComponent( {
        render(){
            return (
                <header>
                <Bar />
                <NavBar />
                </header>
            )
        }
    } )
</script>
<style scoped>
    header{
        position: sticky;
        top: 0;
        z-index: 10;
    }
</style>