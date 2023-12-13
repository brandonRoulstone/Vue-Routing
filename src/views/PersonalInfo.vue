<template>
    <div>
        <h1 class="personal">Personal info</h1>
        <p>{{job}}</p>
    </div>
</template>

<script>
import axios from "axios";

export default {
    props:['id'],
    data() {
        return {
            job : null 
        }
    },
    mounted(){
        axios.get('http://localhost:3000/jobs/' + this.id)
        .then(res => this.job = res.data)
    }
}
</script>

<style>

</style>