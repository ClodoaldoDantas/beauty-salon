<template>
  <section class="our-services">
    <div class="container">
      <h2 class="our-services__title">Serviços</h2>
      <p class="our-services__text">
        Com mais de 10 anos no mercado, o <a href="#">Beautysalon</a> já
        conquistou clientes de inúmeros países com seus tratamentos exclusivos e
        totalmente naturais.
      </p>

      <ul class="our-services__list">
        <li class="our-services__item">
          <img src="@/assets/images/woman-hair.svg" alt="" />
          <h3>Terapia capilar</h3>
          <p>
            Terapia completa para couro cabeludo e fios, protegendo todos os
            tipos de cabelos, inclusive os longos e finos.
          </p>
        </li>

        <li class="our-services__item">
          <img src="@/assets/images/trim.svg" alt="" />
          <h3>Cortes</h3>
          <p>
            A nossa equipe é repleta de profissionais renomados, famosos por
            lançarem tendências com cortes diferenciados e clássicos.
          </p>
        </li>

        <li class="our-services__item">
          <img src="@/assets/images/cosmetic.svg" alt="" />
          <h3>Tratamentos</h3>
          <p>
            O beautysalon conta com diversos tratamentos naturais e totalmente
            veganos, para qualquer tipo de cabelo.
          </p>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';

.our-services {
  padding-top: 5rem;

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
    margin-bottom: 1rem;

    @include medium {
      text-align: center;
    }
  }

  &__text {
    font-size: 1rem;
    line-height: 1.625rem;
    color: var(--green-900);
    margin-bottom: 4rem;

    @include medium {
      text-align: center;
      max-width: 520px;
      margin: 0 auto 4rem;
    }

    a {
      color: var(--green-500);
      font-weight: 700;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &__list {
    display: grid;
    gap: 1.5rem;

    @include medium {
      grid-template-columns: repeat(2, 1fr);
    }

    @include large {
      grid-template-columns: repeat(3, 1fr);
    }
  }

  &__item {
    padding: 3.75rem 2rem;
    background: var(--gray-300);
    box-shadow: 0px 0px 12px rgba(0, 0, 0, 0.08);
    border-bottom: 4px solid var(--green-500);
    text-align: center;

    img {
      margin-bottom: 1.5rem;
    }

    h3 {
      font-size: 1.5rem;
      line-height: 2.25rem;
      margin-bottom: 0.75rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.625rem;
    }
  }
}
</style>
