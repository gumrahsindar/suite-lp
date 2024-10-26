<script setup lang="ts">
import ImageJeremyLarge from '../assets/images/image-jeremy-large.webp'
import ImageJeremySmall from '../assets/images/image-jeremy-small.webp'
import Pattern2 from '../assets/images/pattern-curved-line-2.svg'
import PatternBlur from '../assets/images/pattern-blur.svg'
</script>

<template>
  <section id="testimonial">
    <div class="container">
      <div class="main-layout">
        <picture>
          <source
            :srcset="ImageJeremySmall"
            type="image/webp"
            media="(max-width: 1024px)"
            width="243"
            height="395"
          />
          <img
            class="image-jeremy"
            :src="ImageJeremyLarge"
            alt=""
            width="361"
            height="590"
          />
        </picture>
        <img class="image-pattern" :src="Pattern2" alt="" />
        <img class="blur-pattern" :src="PatternBlur" alt="" />
        <div class="cite">
          <h2 class="title-lg-regular">
            It just <span class="title-lg-bold">works.</span>
          </h2>
          <blockquote>
            <p class="text-quote">
              “I really like how it is an all-in-one solution that handles many
              of the tasks that you would normally need separate tools to do the
              same job. This thing is a miracle worker.”
            </p>
            <footer style="margin-top: 40px">
              <cite class="text-body">Jeremy Robinson</cite>
              <p class="title-sm-bold" style="font-weight: normal">CMO, FYLO</p>
            </footer>
          </blockquote>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.main-layout {
  position: relative;
  margin-bottom: 95px;
  padding: 88px 125px;
  border-radius: 15px;
  background-color: var(--clr-dark-blue);
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 65px;

  @media (max-width: 1024px) {
    padding: 0 58px 64px 58px;
    grid-template-columns: minmax(0, 1fr);
    justify-items: center;
    text-align: center;
    gap: 30px;
  }

  @media (max-width: 640px) {
    padding: 0 24px 64px 24px;
  }

  & .image-jeremy {
    grid-column: auto;
    position: absolute;
    bottom: 0;
    left: 10%;
    z-index: 30;

    @media (max-width: 1024px) {
      position: relative;
      top: -75%;
      left: 0;
      margin-bottom: -160px;
    }
  }

  & .image-pattern {
    grid-column: 7 / span 2;
    grid-row: 1 / auto;
    align-self: center;
    position: absolute;
    top: 15%;
    left: -50%;
    z-index: 20;

    @media (max-width: 1024px) {
      grid-column: 1 / span 1;
      position: static;
      grid-row: auto;
    }
  }

  & .blur-pattern {
    position: absolute;
    top: 20%;
    z-index: 10;

    @media (max-width: 1024px) {
      top: -10%;
      width: 50%;
      height: 50%;
    }
  }

  & .cite {
    color: var(--clr-beige-light);
    grid-column: 8 / span 6;
    grid-row: 1 / auto;
    display: flex;
    flex-direction: column;
    gap: 40px;
    max-width: 40ch;

    & .text-body {
      font-weight: bold;
      font-style: normal;
      text-transform: uppercase;
    }

    @media (max-width: 1024px) {
      grid-column: 1 / span 1;
      grid-row: auto;
      max-width: 100%;
    }
  }
}

.container {
  @media (max-width: 1024px) {
    padding: 0;
  }
}
</style>
