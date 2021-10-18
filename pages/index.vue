<template>
  <div class="container">
    <div class="side left">
      <div class="header">
        <div class="account">
          <div class="avatar_wrapper">
            <img class="avatar" src="~/assets/avatar.jpg" alt="avatar" />
          </div>
          <div class="account_wrapper">
            <div class="name">Ahmad</div>
            <div class="logout">
              <button class="logout_button">
                logout
              </button>
            </div>
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
*,
html,
div,
p,
span {
  padding: 0;
  margin: 0;
}

.container {
  display: flex;
}

.side {
  height: 100vh;
}

.left {
  width: 54.99%;
  padding: 20px;
  display: flex;
}

.right {
  width: 44.99%;
  background-color: #f0f7f7;
  padding: 20px;
}

.account {
  display: flex;

  .name {
    font-size: 25px;
  }

  .avatar_wrapper {
    margin-right: 20px;

    .avatar {
      width: 60px;
      height: 60px;
      border-radius: 50%;
    }
  }
}

.logout {
  .logout_button {
    outline: none;
    border: none;
    background-color: transparent;
  }
}
</style>
