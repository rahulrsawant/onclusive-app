<template>
  <div style="width: 100%;height: 100%;display: flex;justify-content: center;align-items: center;">
    <b-form @submit="onSubmit" v-if="show">
      <img src = "https://forwardplanner.com/Images/Onclusive_ForwardPlanner_Logo.svg" style="width: 200px; height: 100px; object-fit: scale-down;"/>    
      <b-form-group
        id="input-group-1"
        label="Username:"
        label-for="input-1">
        <b-form-input
          id="email"
          v-model="form.email"
          type="email"
          placeholder="Enter email"
          required>
        </b-form-input>
      </b-form-group>
      <b-form-group id="input-group-2" label="Password:" label-for="input-2">
        <b-form-input
          id="password"
           type="password"
          v-model="form.password"
          placeholder="Enter password" 
          required        
        ></b-form-input>
      </b-form-group>
<b-form-group id="input-group-4">
        <b-form-checkbox-group
          v-model="form.checked"
          id="checkboxes-4">
          <b-form-checkbox value="rememberMe">Remember Me</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>
      <b-button type="submit" variant="primary">Login</b-button>
    </b-form>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          password: ''
        },
        show: true
      }
    },
    methods: {
      onSubmit(e) {
        e.preventDefault()
        alert(JSON.stringify(this.form))
    }
    }
  }
</script>
