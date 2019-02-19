<template>
    <ul class="list-items">
        <li>
            <Item />
        </li>
    </ul>
</template>


<script>
import Item from './Item.vue';

export default {
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
