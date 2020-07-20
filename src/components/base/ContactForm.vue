<template>
  <div>
    <base-info-card
      :title="title"
      :subtitle="subtitle"
      space="4"
      color="primary"
    />

    <base-text-field label="Имя" />

    <base-text-field label="Email" />

    <base-text-field label="Тема" />

    <base-textarea
      class="mb-6"
      label="Текст письма"
    />

    <base-btn
      :color="!theme.isDark ? 'accent' : 'white'"
      href="mailto:gulyasmir@yandex.ru?subject=vue"
      outlined
      target="_blank"
    >
      Отправить
    </base-btn>
  </div>
</template>

<script>
  export default {
    name: 'BaseContactForm',

    // Injected from the Vuetify Themeable mixin
    inject: ['theme'],

    props: {
      subtitle: String,
      title: {
        type: String,
        default: 'Напишите нам письмо',
      },
    },
  }
</script>
