<template>
<div>
  <h2>Vue Formulate</h2>
  <div class="container">
    <FormulateForm v-model="formValues" @submit="handleSubmit">
      <FormulateInput name="name" label="Name" validation="required" />
      <FormulateInput type="email" name="email" label="Email" validation="required|email" />
      <FormulateInput type="password" name="password" label="Password" validation="required" />
      <FormulateInput type="submit" label="Submit" />
    </FormulateForm>
  </div>
  <h3>Values:</h3>
  {{formValues}}
</div>
</template>

<script>
export default {
  data: () => ({
    formValues: {},
  }),
  methods: {
    handleSubmit() {},
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
}
</style>
