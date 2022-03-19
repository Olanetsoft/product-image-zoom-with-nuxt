<template>
<div class="product-image">
  <p class="text-center text-2xl text-gray-900 font-bold mt-8 pt-8">
    E-commerce product customization page in Nuxt.js
  </p>
  <div
    class="relative flex items-top justify-center min-h-screen sm:items-center pt-2 sm:pt-0"
  >
    <ProductZoomer :base-images="images" :base-zoomer-options="zoomerOptions" />
  </div>
</div>
</template>

<script>
export default {
  name: "ProductImage",
  data() {
    return {
      images: {
        thumbs: [
          {
            id: 1,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647642978/h1-r3.jpg",
          },
          {
            id: 2,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644372/h3-r3.jpg",
          },
          {
            id: 3,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644758/h4-r3.jpg",
          },
        ],
        normal_size: [
          {
            id: 1,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647642886/h1-r2.jpg",
          },
          {
            id: 2,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644372/h3-r2.jpg",
          },
          {
            id: 3,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644758/h4-r2.jpg",
          },
        ],
        large_size: [
          {
            id: 1,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647642886/h1-r1.jpg",
          },
          {
            id: 2,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644372/h3-r1.jpg",
          },
          {
            id: 3,
            url: "https://res.cloudinary.com/olanetsoft/image/upload/v1647644758/h4-r1.jpg",
          },
        ],
      },
      zoomerOptions: {
        zoomFactor: 4, // scale for zoomer
        pane: "pane", // three type of pane ['pane', 'container-round', 'container']
        hoverDelay: 300, // how long after the zoomer take effect
        namespace: "zoomer", // add a namespace for zoomer component, useful when on page have multiple zoomer
        move_by_click: false, // move image by click thumb image or by mouseover
        scroll_items: 5, // thumbs for scroll
        choosed_thumb_border_color: "#bbdefb", // choosed thumb border color
        scroller_button_style: "line",
        scroller_position: "left",
        zoomer_pane_position: "right",
      },
    };
  },
};
</script>
