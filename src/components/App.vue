<template>
    <div class="app">
        <ListItems
            :items="items"
            v-on:updateItem="updateItem"
            v-on:removeItem="removeItem"/>
        <SidePanel
            v-on:addItem="createItem(maxId++)"
            :costTotal="costTotal"
            :lengthItems="items.length"
            />
        <Footer />
    </div>
</template>


<script>
import Footer from './Footer.vue';
import SidePanel from './SidePanel.vue';
import ListItems from './ListItems.vue';


export default {
    name: 'App',
    data() {
        return {
            maxId: 10,
            costTotal: 0,
            items: []
        }
    },
    methods: {
        createItem(id)  {
            this.items.push({
                label: '',
                cost: '',
                value: '',
                costPerClient: '',
                costTotal: '',
                id
            })
        },

        removeItem(id) {
            this.items = this.items.filter((el) => {
                return el.id !== id;
            });

            this.countAll();
        },

        updateItem(newItem) {
            this.items.map((el) => {
                if (el.id == newItem.id) {
                    el.cost = newItem.cost;
                    el.costPerClient = newItem.costPerClient;
                    el.label = newItem.label;
                    el.costTotal = newItem.costTotal;
                    el.value = newItem.value;
                }
            })

            this.countAll();
        },

        countAll() {
            let total = 0;

            this.items.forEach((el) => {
                total += +el.costTotal;
            })

            this.costTotal = total;
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
