<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "1",
                isBlueActive: true,
                isRedActive: false,
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.isBlueActive=!this.isBlueActive;
                this.isRedActive=!this.isRedActive;
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="demo1" class="m-2" v-bind:class="{'redBox':isRedActive, 'blueBox':isBlueActive}">
            div ID : {{demo1}} 
        </div>
        
        <button type="button" v-on:click="changeColor()" v-bind:class="['btn',{'btn-danger':isRedActive, 'btn-secondary':isBlueActive}]">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
