<script>
  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {
    name: 'FourOhFour',

    metaInfo: { title: 'Oops! Страница не найдена!' },

    extends: View,

    mixins: [
      LoadSections([
        '404',
        'newsletter',
        'info-alt',
      ]),
    ],

    props: {
      id: {
        type: String,
        default: 'about',
      },
    },
  }
</script>
