<script>
  // Extensions
  import View from '@/views/View'

  // Mixins
  import LoadSections from '@/mixins/load-sections'

  export default {
    name: 'Pro',

    metaInfo: { title: 'Resources' },

    extends: View,

    mixins: [
      LoadSections([
        'hero-alt',
        'resource',
      ]),
    ],

    props: {
      id: {
        type: String,
        default: 'pro',
      },
    },
  }
</script>
