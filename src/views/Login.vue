<template>
  <div>
    <!-- Page content -->
    <b-container class="mt--8 pb-5">
      <b-row class="justify-content-center">
        <b-col lg="5" md="7">
          <b-form @submit="onSubmit" >
            <h2 class="text-center">Log in</h2>
            <b-form-group class="row py-sm-3 mb-0">
                <b-input id="input-1" v-model="form.email"
                type="email"
                placeholder="Enter email"
                required
              ></b-input>
            </b-form-group>
            <b-form-group class="row pb-3">
                <b-input
                id="input-2"
                v-model="form.password"
                placeholder="Password"
                type="password"
                required
              ></b-input>
            </b-form-group>
            <div class="row pb-3">
            <b-form-checkbox v-model="form.rememberMe">Remember me</b-form-checkbox>
            </div>
                  <div class="pb-3 text-center">
                    <button type="primary" class="btn btn-primary btn-block" style="width: 100%;">Sign in</button>
                  </div>
            
          </b-form>

          <b-row class="mt-3 text-center">
            <b-col cols="6">
              <router-link to="/dashboard" class=""><small>Forgot password?</small></router-link>
            </b-col>
            <b-col cols="6" class="text-right">
              <router-link to="/register" class=""><small>Create new account</small></router-link>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
  export default{
    data(){
      return{
        form:{
          email: '',
          password: '',
          rememberMe: false
        }
      };
    },
    methods:{
      onSubmit(){
        // this will be called only after form is valid. You can do api call here to login
        alert(JSON.stringify(this.form))
      }
    }
  };
</script>
