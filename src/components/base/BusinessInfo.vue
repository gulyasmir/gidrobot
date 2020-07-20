<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-info-card
        title="Сохраните себе наши контакты"
        pace="6"
      >
        Лучший автосервис в Рязани, мы делаем надежные гидроборты.
      </base-info-card>

      <base-business-contact dense />
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseBusinessInfo',

    props: { dark: Boolean },

    data: () => ({
      business: [
        {
          icon: 'mdi-map-marker-outline',
          title: 'Адрес',
          text: 'Рязань, Окружная дорога, автосервис Гидроборт',
        },
        {
          icon: 'mdi-cellphone',
          title: 'Телефон',
          text: '+7-(800)-999-99-99',
        },
        {
          icon: 'mdi-email',
          title: 'Email',
          text: 'gulyasmir@yandex.ru',
        },
      ],
    }),
  }
</script>
