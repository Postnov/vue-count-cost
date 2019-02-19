<template>
    <div class="app">
        <ListItems />
        <SidePanel />
        <Footer />
    </div>
</template>


<script>
import Footer from './Footer.vue';
import SidePanel from './SidePanel.vue';
import ListItems from './ListItems.vue';


export default {
    data() {
        return {
            msg: 'hello'
        }
    },
    components: {
        Footer,
        SidePanel,
        ListItems
    }
}
</script>

<style>

body {
    font: 400 20px/1.5 'Roboto', sans-serif;
    background-color: #f5f5f5;
  }




</style>
