<template>
  <section>
    <div class="fact" v-for="fact in facts">
      <div class="wrapper-text">
        <p class="title">{{ fact.title }}</p>
        <p class="text">{{ fact.text }}</p>
      </div>
      <div class="wrapper-image">
        <img :src="useAsset(fact.urlImg)" alt="">
      </div>

    </div>
  </section>
</template>

<script setup lang="ts">
const facts = [
  {
    title: 'Choose to Reuse',
    text: 'Challenge yourself to use more reusable items, like bags, cups, and lunchboxes, and to take only what you need. Before throwing something away, see if you can find a new use for it—turning trash into treasure!',
    urlImg: 'bernard-hermant.jpg'
  },
  {
    title: 'Beware of Energy Vampires',
    text: 'Even if something is turned off, it can use or “suck” electricity when it’s plugged into the wall. Unplug electronics like video games and chargers when you aren’t using them.',
    urlImg: 'appolinary-kalashnikova.jpg'
  },
  {
    title: 'Be Kind to Wildlife',
    text: 'All wildlife deserves respect—even animals that don’t usually get as much love, like insects, spiders, frogs, and snakes. They have important roles to play in our ecosystems. Make your yard welcoming to all wildlife by planting pollinator-friendly and native plants.',
    urlImg: 'noah-buscher.jpg'
  },
  {
    title: 'Spot Check',
    text: 'Keeping track of animal populations is part of protecting wildlife. Scientists gather this information by using “trail cameras” that take pictures of animals in an area. You can help by identifying wildlife in the images taken by these cameras online. Right now, we need your help identifying burrowing owls in the southwestern United States and wildlife in Kenya.',
    urlImg: 'chris-abney.jpg'
  },
  {
    title: 'Help Slow Climate Change',
    text: 'It takes community-level action to slow climate change, but your choices can help. Challenge your family to make more meatless dinners, or carpool, walk, bike, or use public transportation when you can. These actions reduce carbon emissions that drive climate change.',
    urlImg: 'paul-green.jpg'
  },
  {
    title: 'Be a Responsible Pet Owner',
    text: 'Make sure you do your research and are ready for the large responsibility of caring for an animal its entire life. Keep pets—especially cats—indoors, as they can prey on local wildlife. And remember that wild animals do not make good pets!',
    urlImg: 'arun-anoop.jpg'
  },
  {
    title: 'Leave No Trace',
    text: 'When you explore nature, leave only footprints and take only pictures. Be sure to stay on established trails, and never try to approach, touch, or feed wildlife. Instead, observe wildlife respectfully from a distance using binoculars or a camera. Even just a tiny piece of trash can be harmful to wildlife, so if you can safely pick up litter, place it in the appropriate bin.',
    urlImg: 'evelyn-mostrom.jpg'
  },
  {
    title: 'Snack Sustainably',
    text: 'Some snack foods are made with unsustainable palm oil, whose production takes habitat away from threatened wildlife. Choose snacks that are certified by the Roundtable for Sustainable Palm Oil (RSPO) instead. You can ask an adult to download an app to find RSPO-approved products.',
    urlImg: 'promodhya-abeysekara.jpg'
  },
]

function useAsset(path: String) {
  const assets = import.meta.glob('~/assets/**/*', {
    eager: true,
    import: 'default',
  });
  return assets['/assets/images/main-page/' + path];
}
</script>

<style scoped lang="scss">
section {
  .fact {
    display: flex;
    color: var(--background);
    background: var(--primary-green);

    .wrapper-text {
      width: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 100px;

      .title {
        font-size: 20px;
      }
    }

    .wrapper-image {
      width: 50%;
      max-height: 500px;
      overflow: hidden;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }


    &:nth-child(even) {
      color: var(--primary-green);
      background: var(--background);
      flex-direction: row-reverse;
    }
  }
}
</style>
