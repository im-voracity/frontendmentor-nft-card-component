<template>
  <div class="card">
    <a href="#" class="featured">
      <img class="featured-image" :src="productPicture" alt=""/>
      <svg width="48" height="48" xmlns="http://www.w3.org/2000/svg">
        <g fill="none" fill-rule="evenodd">
          <path d="M0 0h48v48H0z"/>
          <path
              d="M24 9C14 9 5.46 15.22 2 24c3.46 8.78 12 15 22 15 10.01 0 18.54-6.22 22-15-3.46-8.78-11.99-15-22-15Zm0 25c-5.52 0-10-4.48-10-10s4.48-10 10-10 10 4.48 10 10-4.48 10-10 10Zm0-16c-3.31 0-6 2.69-6 6s2.69 6 6 6 6-2.69 6-6-2.69-6-6-6Z"
              fill="#FFF" fill-rule="nonzero"/>
        </g>
      </svg>
    </a>
    <a href="#" class="title-link"><h1 class="product-title">{{productName}}</h1></a>
    <p class="product-description">{{productDescription}}</p>
    <div class="bottom">
      <div class="pricing">
        <div class="price">
          <svg width="11" height="18" xmlns="http://www.w3.org/2000/svg">
            <path d="M11 10.216 5.5 18 0 10.216l5.5 3.263 5.5-3.262ZM5.5 0l5.496 9.169L5.5 12.43 0 9.17 5.5 0Z"
                  fill="#00FFF8"/>
          </svg>
          <p>{{price}} {{currency}}</p>
        </div>
        <div class="timer">
          <svg width="17" height="17" xmlns="http://www.w3.org/2000/svg">
            <path
                d="M8.305 2.007a6.667 6.667 0 1 0 0 13.334 6.667 6.667 0 0 0 0-13.334Zm2.667 7.334H8.305a.667.667 0 0 1-.667-.667V6.007a.667.667 0 0 1 1.334 0v2h2a.667.667 0 0 1 0 1.334Z"
                fill="#8BACD9"/>
          </svg>
          <p>{{daysLeft}} days left</p>
        </div>
      </div>
      <div class="bar"></div>
      <div class="owner">
        <img class="owner-picture" :src="ownerPicture" alt=""/>
        <p>Creation of <span>{{owner}}</span></p>
      </div>
    </div>
  </div>
</template>

<script>
import productPic from '../assets/image-equilibrium.jpg'
import ownerPic from '../assets/image-avatar.png'


export default {
  name: "NftCard",
  data() {
    return {
      owner: 'Jules Wyvern',
      productName: 'Equilibrium #3429',
      productDescription: 'Our Equilibrium collection promotes balance and calm.',
      price: '0.041',
      currency: 'ETH',
      daysLeft: '3',
      ownerPicture: ownerPic,
      productPicture: productPic
    }
  }
};
</script>

<style scoped>
.card {
  height: 543px;
  width: 327px;
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  background-color: hsla(216, 51%, 16%, 1);
  box-shadow: 0 25px 50px 0 hsla(0, 0%, 0%, 0.1);
  border-radius: 15px;
}

.featured {
  width: 278px;
  height: 278px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 9px;
  position: relative;
  background-color: transparent;
  margin-bottom: 24px;
}

.featured:hover {
  cursor: pointer;
  background-color: hsla(178, 100%, 50%, 1);
}

.featured-image {
  width: 100%;
  height: 100%;
  border-radius: 8px;
  position: absolute;
  transition: 0.3s;
}

.featured:hover .featured-image {
  opacity: 0.5;
}

.featured svg {
  opacity: 0;
  position: absolute;
  transition: 0.3s;
}

.featured:hover svg {
  opacity: 1;
}

.product-title {
  width: 100%;
  font-family: 'Outfit', sans-serif;
  font-size: 22px;
  font-weight: 600;
  line-height: 28px;
  color: white;
  margin-bottom: 12px;
  text-align: left;
}

.product-title:hover {
  color: hsla(178, 100%, 50%, 1);
  cursor: pointer;
}

.title-link {
  width: 100%;
}

.product-description {
  font-family: 'Outfit', sans-serif;
  font-weight: 300;
  font-size: 18px;
  line-height: 26px;
  color: hsla(215, 51%, 70%, 1);
  text-align: left;
  margin-bottom: 16px;
}

.bottom {
  width: 100%;
}

.pricing {
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.price, .timer {
  display: flex;
  justify-content: space-between;
  gap: 6.5px;
}

.price p {
  font-family: 'Outfit', sans-serif;
  font-weight: 600;
  font-size: 15px;
  line-height: 19px;
  color: hsla(178, 100%, 50%, 1);
}

.timer p {
  font-family: 'Outfit', sans-serif;
  font-weight: 600;
  font-size: 15px;
  line-height: 19px;
  color: hsla(215, 51%, 70%, 1);
}

.bar {
  margin: 16px 0;
  height: 1px;
  width: 100%;
  background-color: hsla(216, 32%, 27%, 1);
}

.owner {
  display: flex;
  align-items: center;
  gap: 16px;
  color: hsla(215, 51%, 70%, 1);
}

.owner p {
  font-family: 'Outfit', sans-serif;
  font-weight: 400;
  font-size: 15px;
  line-height: 19px;
  color: hsla(215, 51%, 70%, 1);
}

.owner p span {
  color: white;
}

.owner p span:hover {
  cursor: pointer;
  color: hsla(178, 100%, 50%, 1);
}

.owner-picture {
  width: 33px;
  height: 33px;
}

@media screen and (min-width: 650px) {
  .card {
    width: 350px;
    height: 596px;
    padding: 24px 24px 32px 24px;
  }

  .featured {
    height: 302px;
    width: 302px;
  }

  .product-title {
    margin-bottom: 16px;
  }

  .product-description {
    margin-bottom: 24px;
  }

  .bar {
    margin: 24px 0 16px 0;
  }
}

</style>