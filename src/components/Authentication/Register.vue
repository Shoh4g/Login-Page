<template>
  <base-card>
    <h2>Register Here</h2>
<form @submit="checkPassword($event)">

<div class="form-control">
  <label for="email">Email address</label>
  <input v-model="email" for="email" type="email" class="form-control" placeholder="Enter email" required>
</div>

<div class="form-control">
  <label for="name">Name</label>
  <input v-model="name" for="name" type="text" class="form-control" placeholder="Name" required>
</div>

<div class="form-control">
  <label for="password">Password</label>
  <input v-model="password" type="password" class="form-control" for="password" placeholder="Password" required>
</div>

<div class="form-control">
  <label for="Confirm">Confirm Password</label>
  <input v-model="confirmPassword" type="password" class="form-control" for="Confirm" placeholder="Confirm Password" required>
</div>
      <div>
        <base-button type="submit">Register</base-button>
      </div>
    </form>
  </base-card>
</template>

<script>
export default {
  name: "Login",

    data(){
        return{
            email: undefined,
            password: undefined,
            confirmPassword: undefined,
            name: undefined
        }
    },
    methods:{
        checkPassword(event){
            if( this.password!=this.confirmPassword){
                event.preventDefault()
                alert("Passwords must match!")
            }
        }
    }

};
</script>

<style scoped>
input {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}
input:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}
.form-control {
  margin: 1rem 0;
}
</style>