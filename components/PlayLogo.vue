<template>
    <v-container>
        <img @mouseenter="hover = true" @mouseleave="hover = false" :class="{'heart' : hover}" class="pointer" alt="Vector Logo" src="/Vector.png"  @click="dialog = true" >
        <v-dialog v-model="dialog" width="500" >
            <video ref="video" src="../static/Video.mp4" controls></video>
        </v-dialog>
    </v-container>
</template>


<script>
export default {
    data(){
        return{
            dialog: false,
            hover:false
        }
    },
    watch:{
        "dialog"(value){
            setTimeout(()=> {
                let video = this.$refs.video
                if(value === true) video.play()
                else video.pause()
             },300)
        }
    }
}
</script>


<style scoped>
.heart{
	animation: beat .50s infinite alternate;
	transform-origin: center;
}

/* Heart beat animation */
@keyframes beat{
	to { transform: scale(1.1); }
}

</style>