<template>
  <div>
    <h2>STUDENTS</h2>
    <LogoutButton></LogoutButton>

  </div>
</template>

<script>
import roles from "@/roles";

export default {
  created: function (){
    const role = localStorage.getItem('role')
    if (role !== roles.MENTOR) {
      this.$router.push('/')
    }
  }
}
</script>

<style lang="scss" scoped>
h2 {
  background-color: aqua;
  color: #2c3e50;
}
</style>