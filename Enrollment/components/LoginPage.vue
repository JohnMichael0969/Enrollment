<template>
<div class="container-fluid">
    <div class="row no-gutter">
        <!-- The image half -->
        <div class="col-md-6 d-none d-md-flex bg-image"></div>
        <!-- The content half -->
        <div class="col-md-6 bg-light">
          <div class="login d-flex align-items-center py-5">
            

    <b-form @submit="onSubmit">
      <b-form-group
        id="email"
        label="Email address:"
        label-for="input-email"
        description="We'll never share your email with anyone else.">
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          placeholder="Enter email"
          required>
          </b-form-input>
      </b-form-group>

      <b-form-group 
        id="input-password" 
        label="Password:" 
        label-for="input-2">
        <b-form-input
          id="input-password"
          v-model="form.password"
          placeholder="Enter Password"
          type="password"
          required>
        </b-form-input>
      </b-form-group>
<router-link
to="/home">
<b-button type="submit" class="mr-4" variant="primary" >Submit</b-button>
</router-link>
      
      
       </b-form>
   
          </div>
        </div>
    </div>
</div>
</template>



<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          password: '',
         
        }
      }
    }
  }

</script>

<style>
.login,
.image {
  min-height: 100vh;
}

.bg-image {
  background-image: url('https://therichpost.com/wp-content/uploads/2021/02/login-split.jpg');
  background-size: cover;
  background-position: center center;
}
</style>