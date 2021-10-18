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
        <div class="options">
          <div class="colors">
            <span>Colors : </span>
            <button v-for="item in 10" :key="item" class="color_button">
              {{ item }}
            </button>
          </div>
        </div>
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
    <div class="middle">
      <img src="~/assets/chair1.png" alt="" srcset="" />
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
  display: flex;
  flex-direction: column;
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

.middle {
  position: absolute;
  left: 35%;
  top: 10%;
}

//////////////////////////////////////////////////////////////////
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

.content {
  display: flex;
  flex-direction: column;
}

.color_button {
  border: 0;
  outline: none;
  width: 35px;
  height: 35px;
  border-radius: 50%;
  background-color: green;
  margin-right: 10px;
  cursor: pointer;
}
</style>
