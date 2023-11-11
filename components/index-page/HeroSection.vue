<template>
  <section>
    <div class="wrapper-main-text">
      <h1>Buy NFT - Help animals</h1>
      <p>All proceeds from the sale of NFTs will go to help animals.</p>
    </div>

    <p>Calling all animal fans: This page is where we share ideas of ways you can help animals no matter where you live.
      Things you do in your everyday life have an effect on wildlife and their habitats. Be part of our team and help
      save animals!
    </p>

    <div class="monstera-leave">
      <img class="monstera-3" src="~/assets/images/monstera-3.png" alt="">
    </div>
  </section>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
section {
  position: relative;
  padding: 0 0 100px 100px;

  .wrapper-main-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    max-width: 80vw;
    height: calc(100vh - 100px);

    h1 {
      max-width: 1200px;
      color: var(--white);
      font-size: 11vw;
      margin-bottom: 40px;
      z-index: 2;
      text-shadow: 8px 8px 10px rgba(0, 0, 0, 0.6);
    }

    p {
      width: 600px;
      color: var(--gray);
      font-size: 40px;
      font-weight: 600;

    }
  }

  p {
    position: relative;
    width: 85%;
    color: var(--white);
    font-size: 22px;
    font-weight: 500;
    text-shadow: 8px 8px 10px rgba(0, 0, 0, 0.6);
    z-index: 2;
  }

  .monstera-leave {
    position: absolute;
    height: 100vh;
    max-width: 90vw;
    right: -35vw;
    top: 0;
    transform: rotate(-71deg);
    z-index: 0;

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      opacity: 0.9;
    }
  }
}

@media screen and (min-width: 1600px) {
  section {


    .wrapper-main-text {


      h1 {
        font-size: 170px;
      }

      p {

      }
    }

    p {

    }

    .monstera-leave {
      right: -30vw;

      img {

      }
    }
  }

}
</style>
