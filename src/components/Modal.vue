<template>
    <div class="backdrop" @click="handleClick">
        <img :src="imgURL" />
    </div>
</template>

<script>
    export default {
        props:['imgURL'],
        setup(props, context){
            

            const handleClick=()=>{
                context.emit('kapat', null)
            }
            return { handleClick}
        }
    }
</script>

<style scoped>
.backdrop {
    position: fixed;
    top: 0%;
    left: 0;
    width: 100%;
    height:100%;
    background: rgba(0, 0, 0, 0.5);

}

.backdrop img{
    display: block;
    max-width: 60%;
    max-height:80%;
    margin: 60px auto;
    box-shadow: 3px 5px 7px rgba(0, 0, 0, 0.5);
    position: relative;

}
</style>