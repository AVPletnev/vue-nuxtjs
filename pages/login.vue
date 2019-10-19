<template>
  <form class="col-6 pt-5">
    <h1>Login</h1>
    <div class="form-group">
      <input type="text" class="form-control" />
    </div>
    <div class="form-group">
      <input type="password" class="form-control" />
    </div>
     <p>
      <n-link to="/">Home</n-link>
    </p>
    <button class="btn btn-primary">Login</button>
  </form>
</template>

<script>
export default {
   layout: 'empty'
};
</script>

<style>
</style>