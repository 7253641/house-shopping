<template>
  <div>
    <!--navbar-->
    <nav class="navbar">
      <div class="navbar-center">
        <span class="nav-icon">
          <i class="fas fa-bars"></i>
        </span>
        <img src="./images/logo.svg" alt="store logo">
        <div class="card-btn">
          <span class="nav-icon">
            <i class="fas fa-cart-arrow-down"></i>
          </span>
          <div class="cart-items">0</div>
        </div>
      </div>
    </nav>
    <!--end of navbar-->
    <!--hero-->
    <header class="hero">
      <div class="banner">
        <h1 class="banner-title">furniture collection</h1>
        <button class="banner-btn">show now</button>
      </div>
    </header>
    <!--end of hero-->
    <!--products-->
    <section class="products" >
      <div class="section-title">
        <h2>our products</h2>
      </div>
      <div class="products-center container">
        <!--single product-->
        <div class="product row align-items-center">
          <div class="col-xs-12 col-md-4" v-for="item in items">
          <div class="img-container">
            <img :src="'src/images/product-'+item.id+'.jpeg'" alt="product"
            class="product-img">
            <button class="bag-btn" :data-id="item.id">
            <i class="fas fa-shopping-cart"></i>
            add to bag</button>
          </div>
          <h3>{{ item.title }}</h3>
          <h4>{{ item.price }}</h4>
        </div>
      </div>
        <!--end of single product-->
      </div>
    </section>
    <!--end of products-->
    <!--cart-->
    <div class="cart-overlay">
      <div class="cart">
        <span class="close-cart">
          <i class="fas fa-window-close"></i>
        </span>
        <h2>your cart</h2>
        <div class="cart-content">
          <!--cart item-->
          <div class="cart-item">
            <img src="images/product-1.jpeg" alt="product">
            <div>
              <h4>queen bed</h4>
              <h5>$9.00</h5>
              <span class="remove-item">remove</span>
            </div>
            <div>
              <i class="fas fa-chevron-up"></i>
              <p class="item-amount">1</p>
              <i class="fas fa-chevron-down"></i>
            </div>
          </div>
          <!--end of cart item-->
        </div>
        <div class="cart-footer">
          <h3>your total:$ <span class="cart-total">0</span></h3>
          <button class="clear-cart banner-btn">clear cart</button>
        </div>
      </div>
    </div>
    <!--end of cart-->
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      items: [
            {
              id: 1,
              title: 'queen panel bed',
              price: 10.99,

            },
            {
              id: 2,
              title: 'king panel bed',
              price: 12.99,

            },
            {
              id: 3,
              title: 'single panel bed',
              price: 12.99,

            },
            {
                id: 4,
                title: 'twin panel bed',
                price: 22.99,

              },
            {
                id: 5,
                title: 'fridge',
                price: 88.99,

              },
            {
                id: 6,
                title: 'dresser',
                price: 32.99,

                },
            {
                id: 7,
                title: 'couch',
                price: 45.99,

                },
            {
                id: 8,
                title: 'table',
                price: 33.99,

              }
            ]
            }
    }
  }

</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
