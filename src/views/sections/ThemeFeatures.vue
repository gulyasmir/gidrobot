<template>
  <base-section id="theme-features">
    <base-section-heading title="О компании">
      Компания Гидромашина является признанным во всём мире производителем гидравлического оборудования, средств контроля, измерений и диагностики практически для всех отраслей промышленности.
    </base-section-heading>

    <v-container>
      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <base-avatar-card
            v-bind="feature"
            align="left"
            horizontal
          >
            Сегодня продукция Гидромашины с успехом используется на сотнях предприятий во всех регионах России.
          </base-avatar-card>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionThemeFeatures',

    data: () => ({
      features: [
        {
          title: 'Технические характеристики гидроборта B-HL.A.500',
        },
        {
          title: 'Технические характеристики гидроборта B-HL.A.700',
        },
        {
          color: 'primary',
          dark: true,
          title: 'Технические характеристики гидроборта F-HL.A.500',
        },
        {
          title: 'Технические характеристики гидроборта B-HL.A.550',
        },
        {
          title: 'Технические характеристики гидроборта B-HL.A.900',
        },
        {
          title: 'Технические характеристики гидроборта B-HL.A.300',
        },
      ],
    }),
  }
</script>
