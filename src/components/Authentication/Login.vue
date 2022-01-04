<template>
  <base-card>
    <h2>Login Here</h2>
    <form>
      <div class="form-control">
        <label for="email">Email</label>
        <input v-model="email" for="email" type="email" class="form-control" placeholder="Email" required> 
      </div>
      <div class="form-control">
        <label for="password">Password</label>
        <input v-model="password" for="password" type="password" class="form-control" placeholder="Password" required> 
      </div>
      <div>
        <base-button type="submit">Login</base-button>
      </div>
    </form>
  </base-card>
</template>

<script>
export default{
    name: 'Login',

     data(){
        return{
            email: undefined,
            password: undefined,
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

