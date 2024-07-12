<template>
    <div class="register-container">
        <h2>注册</h2>
        <form @submit.prevent="handleRegister">
            <div class="form-group">
                <label for="username">用户名:</label>
                <input type="text" id="username" v-model="username" required />
            </div>
            <div class="form-group">
                <label for="email">邮箱:</label>
                <input type="email" id="email" v-model="email" required />
            </div>
            <div class="form-group">
                <label for="password">密码:</label>
                <input type="password" id="password" v-model="password" required />
            </div>
            <button type="submit">注册</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            username: '',
            email: '',
            password: '',
        };
    },
    methods: {
        handleRegister() {
            const user = {
                username: this.username,
                email: this.email,
                password: this.password,
            };
            console.log('Registering with', user);
            // 在此处添加API调用逻辑
        },
    },
};
</script>

<style scoped>
.register-container {
    width: 300px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 4px;
    background: #f9f9f9;
}

.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
}

.form-group input {
    width: 100%;
    padding: 8px;
    box-sizing: border-box;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}
</style>