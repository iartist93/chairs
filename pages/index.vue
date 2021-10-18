<template>
  <div class="container">
    <div class="side left">
      <div class="header">
        <div class="account">
          <div class="avatar_wrapper">
            <img class="avatar" src="~/assets/avatar.jpg" alt="avatar" />
          </div>
        </div>
      </div>
      <div class="content">
        <div class="options"></div>
        <div class="info"></div>
        <div class="actions"></div>
      </div>
    </div>
    <div class="side right">
      <div class="header"></div>
      <div class="content">
        <div class="review"></div>
        <div class="actions"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.avatar_wrapper {
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
</style>
