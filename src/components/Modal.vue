<template>
    <div class="modal-container" v-if="toggleModal">
        <div class="overlay" @click="openModal"></div>
        
        <div class="bloc-modal" >
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequuntur quia ex similique earum numquam quam hic exercitationem illum quas! Reiciendis tempore eligendi ab! Illum sapiente voluptates qui dolorum nam odio vero, blanditiis quisquam vitae alias tempore magnam voluptatibus enim repellat error sed voluptas incidunt consectetur eos ipsa velit, vel deserunt?</p>
            <button @click="openModal">Close</button>
        </div>
    </div>
</template>
<script>
export default {
    name : 'modal-component',
    data () {
        return {
           
        }
    },
    props : ['toggleModal','openModal']
}
</script>
<style>

.overlay {
    background-color:rgba(0, 0, 0, 0.5);
    position:fixed;
    width:100%;
    height:100%;
}
.modal-container {
    position:fixed;
    top:0;
    bottom:0;
    left:0;
    right:0;
    width:100%;
    height:100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.bloc-modal {
    background-color: white;
    padding:50px;
    position:fixed;
    width:50%;
    border-radius: 10px;
}


</style>