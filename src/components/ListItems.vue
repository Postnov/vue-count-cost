<template>
    <ul class="list-items" >
        <li v-for="item in items" :key="item.id" >
            <Item
                :item="item"
                v-on:updateItem="updateItem"
            />
        </li>
    </ul>
</template>


<script>
import Item from './Item.vue';

export default {
    props: ['items'],
    methods: {
        updateItem(newItem) {
            this.$emit('updateItem', newItem)
        }
    },
    components: {
        Item
    }
}
</script>


<style>
.list-items {
    width: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    padding-bottom: 150px;
    padding-left: 0;
    list-style: none;
}
</style>
