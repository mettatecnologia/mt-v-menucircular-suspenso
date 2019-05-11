<template>
  <v-card id="create">

    <v-speed-dial v-model="fab" :top="top" :bottom="bottom" :right="right" :left="left" :direction="direction" :open-on-hover="hover" :transition="transition" style="bottom:40px" >
        <v-btn slot="activator" v-model="fab" color="blue darken-2" dark fab>
            <v-icon>more_vert</v-icon>
            <v-icon>close</v-icon> 
        </v-btn>
        
        <v-btn fab dark small color="green" >
            <v-icon>edit</v-icon>
        </v-btn>
        <v-btn fab dark small color="indigo" >
            <v-icon>add</v-icon>
        </v-btn>
        <v-btn fab dark small color="red" >
            <v-icon>delete</v-icon>
        </v-btn>
    </v-speed-dial>
  </v-card>
</template>

<script>
    export default {
        data: () => ({
            direction: 'top', fab: false, hover: true, 
            top: false, right: true, bottom: true, left: false, 
            transition: 'slide-y-reverse-transition'
        }),
  }
</script>

<style>
  /* This is for documentation purposes and will not be needed in your application */
    #create .v-speed-dial {
        position: absolute;
    }
    #create .v-btn--floating {
        position: relative;
    }
</style>