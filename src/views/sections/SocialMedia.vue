<template>
  <v-theme-provider dark>
    <base-section
      id="social"
      class="accent text-center"
      space="56"
    >
      <base-icon class="mb-8">
        mdi-twitter
      </base-icon>

      <base-section-heading
        color="transparent"
        title="Гидроборт"
      >
        В управлении гидроборт настолько прост, что водитель автомобиля справляется с разгрузкой в одиночку и ему не требуется привлечение ни дополнительных сил, ни другой техники.
      </base-section-heading>

      <a
        class="d-inline-block mb-8"
        href="https://gulyasmir.ru"
        style="text-decoration: none;"
        target="_blank"
      >
        https://gulyasmir.ru
      </a>

      <div class="py-4" />

      <v-btn
        class="font-weight-bold"
        color="white"
        href="https://gulyasmir.ru"
        light
        min-width="168"
        target="_blank"
        x-large
      >
        вперед

        <v-icon right>
          mdi-open-in-new
        </v-icon>
      </v-btn>
    </base-section>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'SectionNews',

    provide: {
      heading: { align: 'center' },
    },
  }
</script>
