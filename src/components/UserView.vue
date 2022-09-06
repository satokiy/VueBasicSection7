<template>
  <div>
    User info<br />
    <router-link to="profile">User Profile</router-link> |
    <router-link to="post">User Post</router-link>

    <div class="green-b">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.green-b{
  border: 1px green solid;
}

</style>
