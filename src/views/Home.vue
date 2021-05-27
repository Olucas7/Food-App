<template>
  <div class="home">
    <div class="header">
      <h2 class="title">Hi <b>Oscar!</b></h2>
      <div class="input">
        <input type="text" placeholder="Find what you want..." />
        <div class="icon-input">
          <i class="bx bx-search"></i>
        </div>
      </div>
      <div class="combo-header">
        <div class="text">
          <h3>Free Combo</h3>
          <p>Taco + Coca-Cola for new users</p>
        </div>
        <div class="img">
          <figure>
            <img
              src="https://images.unsplash.com/photo-1613514785291-fbd52e18e13f?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80"
              alt="tacos"
            />
          </figure>
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
    <div>
      <h2>Top Products</h2>
      <div class="scroll-menu">
        <div class="scroll-content">
          <div :key="index" class="top-products" v-for="(items,index) in 10">
            <div class="top-products-img">
              <img
                src="https://e7.pngegg.com/pngimages/125/779/png-clipart-eatsa-fast-food-restaurant-hamburger-choripan-leaf-vegetable-food.png"
                alt="salad"
                width="100%"
              />
            </div>

            <div class="top-products-texts">
              <div class="top-products-title">Salad combo</div>
              <div class="top-products-price">$7.50</div>
            </div>

            <div class="top-products-action">
              <i class="bx bx-plus-medical"></i>
            </div>
          </div>

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
  margin: 20px;
  .top-products {
    background-color: rgba(250,248,248);
    padding: 10px;
    border-radius: 10px;
    .top.products-img {
      img {
        width: 100%;
      }
    }
    position: relative;
    i {
      right: 0;
      bottom: 0;
      position: absolute;
      padding: 10px;
      color: white;
      border-radius: 50px;
      background-color: rgba(74, 174, 84);
      margin: 5px;
    }
    .top-products-action {
      background-color: rgb(74, 174, 84);
    }
    max-width: 150px;
    .top-products-texts {
      margin: 20px;
      .top-products-title {
        color: rgb(47, 47, 47);
      }
      .top-products-price {
        color: rgb(255, 131, 62);
      }
    }
  }
  
}
.header {
  .combo-header {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    background-color: rgb(74, 174, 84);
    color: white;
    padding: 20px;
    border-radius: 20px;
    align-items: center;
    .img {
      width: 50%;
      img {
        border-radius: 7px;
        width: 100%;
        object-fit: cover;
      }
    }
    .text {
      width: 50%;
      h3 {
        font-weight: 800;
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
      background-color: rgb(250, 248, 248);
      border: 0;
      outline: none;
      padding: 10px;
      border-radius: 10px;
      position: relative;
      padding-left: 30px;
    }
  }
  .icon-input {
    position: absolute;
    padding-left: 10px;
  }
  .title {
    font-weight: 350;
  }
}
.scroll-menu {
  margin-top: 7px;
  .scroll-content {
    display: flex;
    overflow-y: auto;
    .avatar {
      border-radius: 10px;
      background-color: rgba(250, 248, 248);
      padding: 20px;
      margin: 2px;
      i {
        color: rgb(255, 131, 62);
      }
    }
  }
}
</style>
