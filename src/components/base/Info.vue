<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-img
        :src="require('@/assets/logo.png')"
        contain
        max-width="128"
        min-height="78"
        width="100%"
      />

      <base-title
        size="body-1"
        space="4"
        title="Автосервис грузовиков"
        weight="regular"
      />

      <base-body>
        Делаем гидроборты на грузовики
      </base-body>

      <base-btn
        class="mb-12"
        color="white"
        outlined
      >
        Больше информации
      </base-btn>
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseInfo',

    props: {
      title: String,
      dark: Boolean,
    },

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
