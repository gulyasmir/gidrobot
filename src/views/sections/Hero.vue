<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/home-hero.jpg')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .8), rgba(5, 11, 31, .8)"
    >
      <v-container class="fill-height px-4 py-12">
        <v-responsive
          class="d-flex align-center"
          height="100%"
          max-width="700"
          width="100%"
        >
          <base-heading title="Производство гидравлического оборудования" />

          <base-body>
            Компания Гидромашина является признанным во всём мире производителем гидравлического оборудования, средств контроля, измерений и диагностики практически для всех отраслей промышленности. Сегодня продукция Гидромашины с успехом используется на сотнях предприятий во всех регионах России. Гидромашина представляет собой всемирно известную корпорацию, производящую практически все необходимые в гидравлике компоненты – от отдельных принадлежностей до комплектных гидравлических систем и приводов.
          </base-body>

          <div
            :class="$vuetify.breakpoint.smAndDown ? 'flex-column align-start' : 'align-center'"
            class="d-flex flex-wrap"
          />
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
  export default {
    name: 'SectionHero',

    provide: {
      theme: { isDark: true },
    },

    computed: {
      minHeight () {
        const height = this.$vuetify.breakpoint.mdAndUp ? '100vh' : '50vh'

        return `calc(${height} - ${this.$vuetify.application.top}px)`
      },
    },
  }
</script>
