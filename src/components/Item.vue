<template>
    <div class="item">
        <input
            type="text"
            placeholder="Наименование" />
        <input
            type="number"
            placeholder="Стоимость" />
        <input
            type="number"
            placeholder="Объем" />
        <input
            type="number"
            placeholder="Трата на единицу" />

        <div class="price">
            <span class="item__sum-one">0</span>
            <span> руб.</span>
        </div>

        <div class="icons">
            <svg class="cross" viewBox="0 0 24 24">
                <path xmlns="http://www.w3.org/2000/svg" d="M23.954 21.03l-9.184-9.095 9.092-9.174-2.832-2.807-9.09 9.179-9.176-9.088-2.81 2.81 9.186 9.105-9.095 9.184 2.81 2.81 9.112-9.192 9.18 9.1z"></path>
            </svg>
            <svg class="reset" viewBox="0 0 24 24">
                <path d="M12 0c3.31 0 6.291 1.353 8.459 3.522l2.48-2.48 1.061 7.341-7.437-.966 2.489-2.489c-1.808-1.807-4.299-2.928-7.052-2.928-5.514 0-10 4.486-10 10s4.486 10 10 10c3.872 0 7.229-2.216 8.89-5.443l1.717 1.046c-2.012 3.803-6.005 6.397-10.607 6.397-6.627 0-12-5.373-12-12s5.373-12 12-12z"/>
            </svg>
        </div>
    </div>
</template>


<script>
export default {

}
</script>

<style>
.item{
    position: relative;
    background: #fff;
    padding: 40px 15px;
    min-height: 40px;
    margin: 20px 0 5px 10px;
    box-shadow: 0 1px 6px -1px #999;
    justify-content: space-around;
    border-radius: 4px;
    display: flex;
    align-items: center;
}

input{
    outline: none;
    font-size: 17px;
    max-width: 215px;
    width: 100%;
    margin: 10px;
    padding: 7px;
    text-align: center;
    border: none;
    cursor: pointer;
    box-shadow: inset 0 1px 3px rgba(0,0,0,.3);
    border-radius: 3px;
}

::-webkit-input-placeholder {font-size: 13px;}
::-moz-placeholder          {font-size: 13px;}/* Firefox 19+ */
:-moz-placeholder           {font-size: 13px;}/* Firefox 18- */
:-ms-input-placeholder      {font-size: 13px;}


.price {
    margin: 15px;
    font-size: 17px;
    width: 30%;
    text-align: center;
}


.icons {
    position: absolute;
    top: 10px;
    right: 20px;
}

.cross,
.reset{
    width: 15px;
    height: 15px;
    fill: #666;
}

.cross {
    margin-right: 10px;
}

.cross:hover,
.reset:hover{
    fill:darkred;
    cursor: pointer;
}

</style>
