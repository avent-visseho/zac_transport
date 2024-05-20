<template>
    <a href="https://wa.me/++22997768739" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

</template>

<style scoped>

.whatsapp-float {
    position: fixed;
    width: 50px;
    height: 50px;
    bottom: 20px;
    right: 20px;
    background-color: #25d366;
    color: #FFF;
    border-radius: 50px;
    text-align: center;
    font-size: 30px;
    box-shadow: 2px 2px 3px #999;
    z-index: 1000;
}

.whatsapp-float i {
    width: 100%;
    display: block;
    margin-top: 10px;
    height: 100%;
    border-radius: 50%;
}

.whatsapp-float:hover {
    background-color: #128c7e;
}
</style>