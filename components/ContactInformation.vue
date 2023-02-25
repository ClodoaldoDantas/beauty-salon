<template>
  <section class="contact">
    <div class="container">
      <div class="contact__content">
        <h2>Entre em contato com a gente!</h2>

        <p>
          Entre em contato com a Beautysalon, queremos tirar suas dúvidas, ouvir
          suas críticas e sugestões.
        </p>

        <base-button>
          <img src="@/assets/images/whatsapp.svg" alt="" />
          Entrar em contato
        </base-button>
      </div>

      <ul class="contact__list">
        <li class="contact__item">
          <img src="@/assets/images/phone.svg" alt="" />
          11 99845-6754
        </li>

        <li class="contact__item">
          <img src="@/assets/images/map-pin.svg" alt="" />
          R. Amauri Souza, 346
        </li>

        <li class="contact__item">
          <img src="@/assets/images/mail.svg" alt="" />
          contato@beautysalon.com
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/helpers.scss';
.contact {
  padding: 5rem 0;

  @include large {
    padding: 7.5rem 0;
  }

  @include x-large {
    padding: 10rem 0;
  }

  & > .container {
    @include large {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  }

  &__content {
    @include large {
      max-width: 400px;
    }

    h2 {
      @include title;
      margin-bottom: 1rem;
    }

    p {
      font-size: 1rem;
      line-height: 1.625rem;
      color: var(--gray-500);
      margin-bottom: 2rem;

      @include large {
        font-size: 1.125rem;
        line-height: 1.5rem;
      }
    }
  }

  &__list {
    margin-top: 4rem;

    display: flex;
    flex-direction: column;
    gap: 2rem;

    @include large {
      margin-top: 0;
      margin-right: 6rem;
    }
  }

  &__item {
    display: flex;
    align-items: center;
    gap: 0.75rem;

    @include large {
      font-size: 1.125rem;
    }
  }
}
</style>
