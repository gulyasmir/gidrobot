<template>
  <base-section
    id="features"
    class="secondary"
  >
    <v-responsive
      class="mx-auto"
      max-width="1350"
    >
      <v-container fluid>
        <v-row>
          <v-col
            v-for="card in cards"
            :key="card.title"
            cols="12"
            sm="4"
            md="3"
          >
            <base-info-card
              align="center"
              dark
              v-bind="card"
            />
          </v-col>
        </v-row>
      </v-container>
    </v-responsive>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionFeatures',

    data: () => ({
      cards: [
        {
          icon: 'mdi-keyboard-outline',
          title: 'Качество',
          text: 'Гарантируем качество.',
        },
        {
          icon: 'mdi-camera-outline',
          title: 'Надежность',
          text: 'Делаем надежные гидроборты.',
        },
        {
          icon: 'mdi-pencil-outline',
          title: 'Точность',
          text: 'Все точно по размерам.',
        },
        {
          icon: 'mdi-puzzle-outline',
          title: 'Без выходных',
          text: 'Ждем Вам в автосервисе каждый день.',
        },
      ],
    }),
  }
</script>
