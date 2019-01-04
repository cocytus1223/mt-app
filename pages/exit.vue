<template>
  <div class="" />
</template>

<script>
export default {
  layout: 'blank',
  middleware: async ctx => {
    let { status, data } = await ctx.$axios.get(
      'http://127.0.0.1:3000/users/exit'
    )
    if (status === 200 && data && data.code === 0) {
      window.location.href = '/'
    }
  }
}
</script>
