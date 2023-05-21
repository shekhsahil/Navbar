<template>
    <div>
        <h1>Simple Form</h1>
    </div>
    <div class="form-body">
        <form action="">
            <label for="Name"> Name : </label>
            <input type="text" placeholder="Enter Your Name" required v-model="form.name" />
            <br />

            <label for="Email"> Email : </label>
            <input type="email" placeholder="Enter Your Email" required v-model="form.email" />
            <br />

            <label for="tel"> Phone : </label>
            <input type="tel" placeholder="Enter Your Email" required v-model="form.phone" />
            <br />

            <label for="password"> password : </label>
            <input type="password" placeholder="Enter Your Password" required v-model="form.password" />
            <br />

            <button class="button" type="submit" v-on:click="login()">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                name: "",
                email: "",
                phone: "",
                password: "",
            },
        };
    },
    methods: {
        login() {
            console.log("Login Data", this.form);
        },
    },
};
</script>

<style scoped>
.form-body{
    width: 300px;
    height: 300px;
    align-items: center;
    background-color: brown;
    border-radius: 20px;
}
input{
    border-radius: 16px;
}
.button{
  border-radius: 16px;
  color:white;
  background-color: green;
  width:100px;
  height:10px;
}
</style>
