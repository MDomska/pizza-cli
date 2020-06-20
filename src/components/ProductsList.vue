<template>
  <div class="product-container">
    <div class="product" v-for="item in products" :key="item.id">
      <ProductItem
        :image="item.image"
        :title="item.title"
        :description="item.description"
        :price="item.price"
      />
    </div>
  </div>
</template>

<script>
import ProductItem from "./ProductItem";

export default {
  name: "ProductList",
  components: {
    ProductItem
  },
  data: function() {
    return {
      products: [
        {
          id: 1,
          title: "Піца La П’єц",
          description:
            "соус томатний, шинка, баварські ковбаски, сир моцарела, ковбаса салямі, прошуто.",
          price: "167 грн",
          image:
            "https://www.lapiec-pizza.com.ua/wp-content/uploads/2018/07/Flamingo-1.jpg"
        },

        {
          id: 2,
          title: "Капрічоза",
          description: "соус томатний, сир моцарела, шинка, свіжі гриби.",
          price: "151 грн",
          image:
            "https://www.lapiec-pizza.com.ua/wp-content/uploads/2018/08/Capricciosa.jpg"
        },
        {
          id: 3,
          title: "Цезаріо",
          description:
            "соус вершковий, помідори, хрусткий салат, пармезан, куряче мясо, сир моцарела, перепелині яйця.",
          price: "192 грн",
          image:
            "https://www.lapiec-pizza.com.ua/wp-content/uploads/2018/08/Cezario.jpg"
        },
        {
          id: 4,
          title: "Кватро формаджі",
          description:
            "соус вершковий, пармезан, сир моцарела, сир рікотта, сир дор блю,  волоський горіх, груша.",
          price: "182 грн",
          image:
            "https://www.lapiec-pizza.com.ua/wp-content/uploads/2018/07/kvatro.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="css">
* {
  padding: 0;
  margin: 0;
  border: 0;
}
*,
*:before,
*:after {
  -box-sizing: border-box;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}

.wpaper {
  width: 80%;
  margin: 0 auto;
}
.product-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.product {
  width: 50%;
  padding: 10px;
}
.product-image {
  min-height: 300px;
  max-width: 100%;
  background-size: cover;
  background-position-y: center;
}
</style>