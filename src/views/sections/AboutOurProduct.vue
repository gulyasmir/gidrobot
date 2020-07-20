<template>
  <base-section id="about-our-product">
    <base-section-heading
      color="grey lighten-2"
      icon="mdi-vuetify"
      title="Радиально-поршневые насосы"
    />

    <v-container>
      <v-row>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          md="4"
        >
          <base-info-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAboutOurProduct',

    data: () => ({
      cards: [
        {
          title: 'Электрические свойства ',
          subtitle: 'Экономичность',
          text: 'Для того, чтобы выбрать давление на электродвигателе. Вал насоса должен вращаться налево и направо.',
          callout: '01',
        },
        {
          title: 'Рабочее давление',
          subtitle: 'Точная регулировка',
          text: 'Диаметр входного насоса должна быть одинаковой с маслооткачивающей трубкой.',
          callout: '02',
        },
        {
          title: 'Перемещение фланца',
          subtitle: 'Муфты и фланцы',
          text: 'Радиально-поршневые насосы — перемещение фланца должен быть подключен непосредственно к муфте.',
          callout: '03',
        },
      ],
    }),
  }
</script>
