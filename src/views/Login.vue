<template>
    <div class="login">
        <form class="form" @submit.prevent="login">
            <h1>Login</h1>
            <label for="username">Username</label>
            <input v-model="usernmae" name="username" type="text" clas="input">
            <label for="password">Password</label>
            <input v-model="password" name="password" type="text" clas="input">
            <button class="btn">Login</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            username: '',
            password: ''
        }
    },
    methods: {
        login() {
            // Auth user againt API
            window.user = this.username
            this.$router.push({{name: 'protected'}})
        }
    },
}
</script>