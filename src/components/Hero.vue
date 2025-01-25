<script setup lang="ts">
import HeroImageDesktop from '../assets/images/image-hero-portrait.webp'
import HeroImageMobile from '../assets/images/image-hero-landscape@2x.webp'
import Button from './Button.vue'
</script>

<template>
  <section class="container">
    <div class="grid-layout">
      <div class="grid-layout--content">
        <div class="content--wrapper">
          <h1 class="title-xl-bold">
            <span class="title-xl-regular">A</span> super
            <span class="pattern"> solution</span>
            <span class="title-xl-regular"> for your</span> business.
          </h1>
          <p class="text-body">
            Our marketing and sales automations help you scale your outreach to
            get more leads for your company.
          </p>
          <Button class="btn-hero title-md-bold" />
        </div>
      </div>
      <picture class="grid-layout--image">
        <source
          :srcset="HeroImageMobile"
          media="(max-width: 640px)"
          type="image/webp"
          width="343"
          height="240"
        />
        <img width="350" height="600" :src="HeroImageDesktop" alt="" />
      </picture>

      <ul class="grid-layout--stats">
        <li class="title-lg-bold">
          2K+<span class="stats-span title-sm-bold">companies</span>
        </li>
        <li class="title-lg-bold">
          8<span class="stats-span title-sm-bold">langugages</span>
        </li>
        <li class="title-lg-bold">
          1.2M <span class="stats-span title-sm-bold">leads</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.grid-layout {
  margin-block: 67px 200px;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  place-items: center;
  gap: 88px 28px;

  @media (max-width: 64rem) {
    margin-bottom: 292px;
    grid-template-columns: repeat(6, 1fr);
    row-gap: 88px;
  }

  @media (max-width: 40rem) {
    grid-template-columns: minmax(0, 1fr);
  }

  & .grid-layout--content {
    grid-column: 1 / span 7;
    grid-row: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;

    @media (max-width: 64rem) {
      grid-column: 1 / span 12;
    }

    @media (max-width: 40rem) {
      grid-column: 1 / span 1;
      grid-row: auto;
    }

    & .content--wrapper {
      display: flex;
      flex-direction: column;
      align-items: flex-start;

      gap: 20px;

      @media (max-width: 40rem) {
        gap: 10px;
      }
    }

    & .pattern {
      display: inline-block;
      background-image: url('../assets/images/pattern-curved-line-1.svg');
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center -40px;
      background-origin: content-box;
      padding-top: 40px;

      @media (max-width: 64rem) {
        background-position: center -30px;
        padding-top: 30px;
      }

      @media (max-width: 40rem) {
        background-position: center -20px;
        padding-top: 20px;
      }
    }

    & .text-body {
      margin-block: 20px 32px;
      max-width: 37ch;
      text-wrap: pretty;

      @media (max-width: 64rem) {
        margin-block: 20px 20px;
      }

      @media (max-width: 40rem) {
        max-width: 100%;
      }
    }
  }

  & .grid-layout--image {
    grid-column: 6 / span 4;
    grid-row: 1;
    z-index: -1;

    @media (max-width: 64rem) {
      grid-column: 8 / span 5;
    }

    @media (max-width: 40rem) {
      grid-column: 1 / span 1;
      grid-row: auto;

      & img {
        width: 100%;
        height: auto;
      }
    }
  }

  & .grid-layout--stats {
    color: var(--clr-dark-blue);
    list-style: none;
    padding: 0;
    grid-column: 10 / span 3;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 63px;

    & .stats-span {
      display: block;
      font-weight: var(--fw-regular);
      text-transform: uppercase;
      color: var(--clr-gray);
    }

    @media (max-width: 64rem) {
      width: 100%;
      grid-column: 1 / span 12;
      flex-direction: row;
      justify-content: space-around;
      text-align: center;
    }

    @media (max-width: 40rem) {
      grid-column: 1 / span 1;
      flex-direction: column;
      text-align: center;
    }
  }
}
</style>
