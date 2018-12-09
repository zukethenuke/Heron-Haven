<template>
    <v-container>
        <h1>Join</h1>
        <input
            type="email"
            name="email"
            v-model="email"
            placeholder="email">
        <br>
        <input
            type="password"
            name="password"
            v-model="password"
            placeholder="password">
        <button @click="register">Register</button>
    </v-container>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
    data () {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        async register () {
            const response = await AuthenticationService.register({
                email: this.email,
                password: this.password
            })
            console.log(response.data);
            
        }
    }
}
</script>

<style scoped>

</style>
