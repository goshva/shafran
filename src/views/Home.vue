<template>
  <div class="home">
    <div class="header">
      <h2 class="title">Hi <b>Vadim!</b></h2>
      <div class="input">
        <input type="text" placeholder="Find what you want... " />
        <div class="icon-input">
          <i class="bx bx-search"></i>
        </div>
      </div>
      <div class="combo-header">
        <div class="text">
          <h3>Free combo</h3>
          <p>Burger + Coca-cola for new users</p>
        </div>
        <div class="img">
          <img
            src="https://images.unsplash.com/photo-1591722937570-370bf646acc7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" class="avatar" v-for="(item, index) in 10">
          <i class="bx bxs-pizza bx-sm"></i>
        </div>
      </div>
    </div>
    <h2>Top Products</h2>
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" v-for="(item, index) in 10" class="top-products">
          <div class="top-products-img">
            <img
              src="https://images.unsplash.com/photo-1547584370-2cc98b8b8dc8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1051&q=80"
              alt=""
            />
          </div>

          <div class="top-products-text">
            <div class="top-products-title">Berry Juice</div>
            <div class="top-products-price">$7.5</div>
          </div>

          <i class="bx bx-plus-medical"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="less">
h2 {
  font-weight: 400;
}
.home {
  
  .scroll-menu-top {
    .scroll-content-top {
      display: flex;
    }
  }
  .top-products {
    background-color: rgba(250, 248, 248);
    padding: 10px;
    border-radius: 10px;
    .top-products-img {
      img {
        width: 100%;
      }
    }
    position: relative;
    i {
      position: absolute;
      right: 0;
      bottom: 0;
      padding: 10px;
      color: white;
      border-radius: 50px;
      background-color: rgba(74, 174, 84);
      margin: 5px;
    }
    min-width: 150px;
    .top-products-text {
      margin-top: 10px;
      .top-products-price {
        color: rgba(255, 131, 62);
      }
      .top-products-title {
        color: rgba(47, 47, 47);
      }
    }
  }
  margin: 20px;
  .scroll-menu {
    margin-top: 10px;
    .scroll-content {
      display: flex;
      overflow-y: auto;
      &::-webkit-scrollbar {
        display: none;
      }
      .avatar {
        background-color: rgba(250, 248, 248);
        padding: 20px;
        border-radius: 10px;
        margin: 2px;
        i {
          color: rgba(255, 131, 62);
        }
      }
    }
  }
}
.header {
  .combo-header {
    background-color: rgba(74, 174, 84);
    color: white;
    padding: 20px;
    border-radius: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 20px;
    .img {
      width: 50%;
      img {
        width: 100%;
        object-fit: cover;
        border-radius: 10px;
      }
    }
    .text {
      width: 50%;
      h3 {
        font-weight: 400;
      }
      p {
        font-weight: 300;
      }
    }
  }
  .input {
    display: flex;
    position: relative;
    align-items: center;
    margin-top: 15px;
    input {
      width: 100%;
      background-color: rgba(250, 248, 248);
      border: 0px;
      outline: none;
      padding: 10px;
      padding-left: 30px;
      border-radius: 10px;
    }
    .icon-input {
      position: absolute;
      margin-left: 10px;
    }
  }
  .title {
    margin-top: 60px;
    font-weight: 350;
  }
}
</style>
