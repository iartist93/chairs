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
            <span>Color : </span>
            <button
              v-for="item in 10"
              :key="item"
              class="color_button"
              @click="changeSelectedColorIndex(item)"
              :style="{ 'background-color': colorMap[item - 1] }"
            ></button>
          </div>
          <div class="sizes">
            <span>Size : </span>
            <button v-for="item in 10" :key="item" class="size_button">
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
      <img
        :src="require(`@/assets/${selectedColorIndex}.jpg`)"
        alt="selected chair"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedColorIndex: 1,
      colorMap: {
        0: "#2C2B30",
        1: "#F3F3FB",
        2: "#DFE0F2",
        3: "#E8E7ED",
        4: "#202022",
        5: "#EEEAE7",
        6: "#F62231",
        7: "#EFB93F",
        8: "#EC6142",
        9: "#77C0CF"
      }
    };
  },
  methods: {
    changeSelectedColorIndex(index) {
      this.selectedColorIndex = parseInt(index);
    }
  }
};
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

.size_button {
  border: 0;
  outline: none;
  margin-right: 10px;

  font-size: 20px;
  font-weight: 500;
  cursor: pointer;

  &::after {
    content: "cm";
  }
}
</style>
