<template>
  <base-section
    id="map"
    space="0"
  >
    <iframe
      src="https://yandex.ua/map-widget/v1/?um=constructor%3A856e60b39f3bfddb03fcedd004a31ca47a54e65e3f7b6c12b7a8efcb9535e73e&amp;source=constructor"
      width="100%"
      height="400"
      frameborder="0"
    />
  </base-section>
</template>

<script>
  export default {
    name: 'SectionMap',

    provide: {
      heading: { align: 'center' },
    },
  }
</script>
