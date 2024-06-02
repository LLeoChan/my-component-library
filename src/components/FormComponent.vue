<template>
  <form @submit.prevent="onSubmit">
    <div>
      <label for="username">Username:</label>
      <input id="username" v-model="username" />
      <span v-if="errors.username">{{ errors.username }}</span>
    </div>
    <div>
      <label for="email">Email:</label>
      <input id="email" v-model="email" />
      <span v-if="errors.email">{{ errors.email }}</span>
    </div>
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      email: '',
      errors: {},
    };
  },
  methods: {
    validate() {
      const errors = {};
      if (!this.username) {
        errors.username = 'Username is required';
      }
      if (!this.email) {
        errors.email = 'Email is required';
      } else if (!/\S+@\S+\.\S+/.test(this.email)) {
        errors.email = 'Email is invalid';
      }
      this.errors = errors;
      return Object.keys(errors).length === 0;
    },
    onSubmit() {
      if (this.validate()) {
        alert('Form submitted');
      }
    },
  },
};
</script>
