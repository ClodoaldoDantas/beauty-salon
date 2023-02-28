<template>
  <section id="sobre" class="about-us">
    <div class="container">
      <div class="about-us__banner">
        <picture>
          <source
            srcset="@/assets/images/about-desktop.png"
            media="(min-width: 1200px)"
          />

          <img
            src="@/assets/images/about-mobile.png"
            alt="Três cabeleireiras segurando escova e tesoura"
          />
        </picture>
      </div>

      <div class="about-us__content">
        <h2>Sobre nós</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
          sagittis arcu quis nisi luctus, id accumsan felis tristique. Proin
          quis bibendum diam. Sed consequat nisl laoreet eros ultricies
          pellentesque. Nullam in est porta, pellentesque massa vitae, vehicula
          risus.
        </p>

        <p>
          In placerat, felis vitae sodales dictum, lacus quam pretium mi, ut
          pretium urna turpis eu dui. Vestibulum id ullamcorper nibh. Donec
          luctus, nunc finibus elementum suscipit, tortor augue vulputate
          sapien, vitae feugiat enim augue sed.
        </p>

        <p>
          Quisque id aliquam elit. Suspendisse congue pharetra maximus. Duis
          rutrum velit a leo euismod dictum. Sed sodales est efficitur arcu
          tincidunt tincidunt. Curabitur fringilla, risus at feugiat feugiat,
          nisl nulla tincidunt tellus, elementum elementum lorem nisl eleifend
          dolor. Nullam eget dui at sem ullamcorper luctus.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';
.about-us {
  padding-top: 5rem;
  background-color: var(--white);

  @include large {
    padding-top: 7.5rem;
  }

  @include x-large {
    padding-top: 10rem;
  }

  & > .container {
    @include x-large {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 4rem;
    }
  }

  &::after {
    @include gradientBorder;
  }

  &__banner {
    margin-left: -1.5rem;
    margin-right: -1.5rem;
    text-align: center;

    @include x-large {
      margin-left: 0;
      margin-right: 0;
    }
  }

  &__content {
    @include x-large {
      max-width: 600px;
    }

    h2 {
      @include title;
      margin-top: 2rem;
      margin-bottom: 1rem;

      @include x-large {
        margin-top: 0;
      }
    }

    p {
      font-size: 1rem;
      line-height: 1.625rem;
    }

    p + p {
      margin-top: 1.25rem;
    }
  }
}
</style>
