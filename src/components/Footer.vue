<template>
    <footer class="footer">
        <p class="footer__item">Расчет себестоимости (vue.js & components)</p>
        <span class="footer__item"><a target="blank" href="https://vk.com/postnov_daniil">Постнов Даниил</a></span>
    </footer>
</template>

<script>
    export default {}
</script>

<style>
/*================================
           Footer
=================================*/

.footer {
    position: fixed;
    bottom: 0;
    width: 80%;
    left: 0;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    background: #f5f5f5;
}

.footer__item {
    flex-basis: 30%;
    text-align: center;
    color: #515151;
}

.footer__item a {
    color: #515151;
    text-decoration: none;
    border-bottom: 1px solid #515151;
    transition: .3s all;
}

.footer__item a:hover {
    text-decoration: none;
    color: #b35d5d;
    border-color: #b35d5d;
}
</style>

