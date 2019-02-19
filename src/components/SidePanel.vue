<template>
    <aside class="side-panel">
        <div class="side-panel__item ">
            <button
                @click="$emit('addItem')"
                class="add-item">+</button>
        </div>
        <div class="side-panel__item">
            <span>{{ lengthItems }}</span>пунктов
        </div>
        <div class="side-panel__item ">
            <span>{{ costTotal }}</span> руб. на единицу
        </div>
    </aside>
</template>


<script>
export default {
    name: 'Side-panel',
    props: ['costTotal', 'lengthItems']
}
</script>


<style>
.side-panel {
    position: fixed;
    right: 0;
    top: 0;
    height: 100vh;
    width: 20%;
    background-color: #446CB3;

    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}

.side-panel__item {
    width: 100%;
    color: #fff;
    text-align: center;
    max-width: 100%;
    word-break: break-word;
    line-height: 1.1;
}

.side-panel__item > span {
    font-size: 70px;
    font-weight: 100;
    display: block;
}


.add-item {
    border: none;
    color: #fff;
    transition: all .6s;
    cursor: pointer;
    outline: none;
    font-size: 100px;
    line-height: .3;
    font-weight: 100;
    background: transparent;
}
</style>
