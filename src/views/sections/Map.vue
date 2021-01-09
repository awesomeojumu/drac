<template>
  <base-section
    id="map"
    space="0"
  >
    <iframe
      allowfullscreen
      aria-hidden="false"
      frameborder="0"
      height="500"
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.1212286556242!2d7.446154613780571!3d9.052705393504427!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x104e0cc5ca087de3%3A0xe9c43e2eae564be0!2sDisability%20Rights%20Advocacy%20Centre%20(DRAC)%2C%20Abuja.!5e0!3m2!1sen!2sng!4v1610179034621!5m2!1sen!2sng"
      style="border:0; display: block;"
      tabindex="0"
      width="100%"
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
