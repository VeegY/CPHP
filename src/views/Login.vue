<template>
    <div id="login-page-container">
        <div class="input-container">
            <input type="text" placeholder="Username" v-model="username"/>
            <input type="password" placeholder="Password" v-model="password"/>
        </div>
        <div class="button-container">
            <button>Login</button>
            <button>Register</button>
        </div>
        <div>
            <p>Username is: {{username}}</p>
            <p>Password is: {{password}}</p>
        </div>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from "vue-property-decorator";

    @Component({})
    export default class Login extends Vue {
        username: string = "";
        password: string = "";
    }
</script>

<style lang="scss">

</style>