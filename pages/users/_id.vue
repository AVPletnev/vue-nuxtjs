<template>
<div>
  <h1>{{user.name}}</h1>
  <hr>
  <strong>{{user.email}}</strong>
</div>
</template>

<script>
export default {
  validate({params}) {
    return /^\d+$/.test(params.id)
  },
  async asyncData({params, error, $axios}) {
    try {
      const user = await $axios.$get(`https://jsonplaceholder.typicode.com/users/${params.id}`) 
      return {user}
    } catch(e) {
      error(e)
    }
    
  }

}
</script>