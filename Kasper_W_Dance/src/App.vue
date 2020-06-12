<template>
    <v-container fluid fill-height class="container">
        <v-row>
            <v-col cols="12" style="display: flex; justify-content: center">
                <video  autoplay width="100%" height="720px" :src="video"></video>
            </v-col>
            <v-col cols="12" class="flex-md-column" style="display: flex; justify-content: space-around; flex-wrap: wrap">
                <v-btn
                        @click.once="changeSmoothDance"
                        dark
                >
                    Smooth dance
               
                </v-btn>
               
                <v-btn
                        @click.once="changeslavdance"
                        dark
                >
                    {{ slavdance }}
                </v-btn>
                <v-btn
                        @click.once="changeJump"
                        dark
                >
                    {{ Jump }}
                </v-btn>
               <v-btn
                        @click.once="changeSquat"
                        dark
                >
                    {{ Squat }}
                </v-btn>
                
            </v-col>
        </v-row>
    </v-container>
</template>
<script>

    import SmoothDance from '../src/assets/SmoothDance.mp4'

    import slavdance from '../src/assets/slavdance.mp4'
    
    import Jump from '../src/assets/Jump.mp4'
    
    import Squat from '../src/assets/Squat.mp4'

    export default {
        name: 'App',
        data() {
            return {
                video: null,
                slavdance: "Slav dance",
                Squat: "Squat",
                Jump: "Jump",
                
            }
        },
        methods: {
            changeSmoothDance() {
                this.video = SmoothDance
            },
            changeOff() {
                this.video = ""
            },
            changeslavdance() {
                this.video = slavdance
            },
            changeJump() {
                this.video = Jump
            },
            changeSquat() {
               this.video = Squat
            },
          
        }
    }
</script>
<style>
.container {
    background-image: url("../src/assets/background.jpg");
    background-position: center;
    background-size: cover;
    height: 100vh !important;
    font-family: STARWARS,serif !important;
}

</style>