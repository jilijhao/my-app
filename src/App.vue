<template>
    <div id="app">
        <header>
            <h1>我的应用</h1>
            <nav>
                <ul>
                    <li @click="showLogin">登录</li>
                    <li @click="showRegister">注册</li>
                </ul>
            </nav>
        </header>
        <main>
            <Login v-if="currentView === 'Login'" />
            <Register v-if="currentView === 'Register'" />
        </main>
    </div>
</template>

<script>
import Login from './components/Login.vue';
import Register from './components/Register.vue';

export default {
    components: {
        Login,
        Register,
    },
    data() {
        return {
            currentView: 'Login',
        };
    },
    methods: {
        showLogin() {
            this.currentView = 'Login';
        },
        showRegister() {
            this.currentView = 'Register';
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

header {
    background-color: #35495e;
    padding: 10px 0;
    color: white;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 10px;
    cursor: pointer;
}
</style>