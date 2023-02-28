<template>
  <section id="depoimentos" class="depositions">
    <div class="container">
      <h2 class="depositions__title">Depoimentos de quem já passou por aqui</h2>

      <client-only>
        <carousel
          :per-page="1"
          :per-page-custom="[[768, 2]]"
          pagination-active-color="#69B99D"
          pagination-color="#E4E4E4"
        >
          <slide v-for="author in authors" :key="author">
            <figure class="testimony">
              <blockquote class="testimony__quote">
                <p>
                  <span>&ldquo;</span>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Ducimus facere culpa adipisci error repudiandae quisquam
                  sapiente praesentium. Corporis at, dolor non deserunt expedita
                  et optio, consequatur explicabo libero illum blanditiis.
                </p>
              </blockquote>

              <figcaption class="testimony__author">
                <img src="@/assets/images/avatar.png" :alt="author" />
                <cite>{{ author }}</cite>
              </figcaption>
            </figure>
          </slide>
        </carousel>
      </client-only>
    </div>
  </section>
</template>

<script>
export default {
  name: 'DepositionsCarousel',
  data() {
    return {
      authors: ['Lais Bressan', 'Marianne Gomes', 'Thaynara Cavalcante'],
    }
  },
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.depositions {
  padding-top: 5rem;
  background-color: var(--white);

  @include large {
    padding-top: 7.5rem;
  }

  @include x-large {
    padding-top: 10rem;
  }

  &::after {
    @include gradientBorder;
  }

  &__title {
    @include title;
    max-width: 260px;
    margin-bottom: 4rem;

    @include medium {
      max-width: 480px;
      text-align: center;
      margin: 0 auto 4rem;
    }
  }
}

.testimony {
  padding: 2rem;

  &__quote {
    margin-bottom: 1.5rem;

    p {
      font-size: 1rem;
      line-height: 1.625rem;
      color: var(--green-900);
      position: relative;

      span {
        font-family: serif;
        font-size: 2.5rem;
        font-weight: bold;
        position: absolute;
        top: -0.375rem;
        left: -1.875rem;
        color: var(--green-500);
      }
    }
  }

  &__author {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    cite {
      font-size: 1rem;
      line-height: 1.75rem;
      font-style: normal;
      color: var(--gray-500);
    }
  }
}
</style>
