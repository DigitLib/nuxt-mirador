<template>
  <div id="demo"></div>
</template>
<script>
import Mirador from 'mirador/dist/es/src/index'
import { miradorImageToolsPlugin } from 'mirador-image-tools'

export default {
  components: {
  },
  mounted() {
    const manifest = "https://iiif.bodleian.ox.ac.uk/iiif/manifest/e32a277e-91e2-4a6d-8ba6-cc4bad230410.json"
    const config = {
      id: "demo",
      windows: [
        {
          manifestId: manifest,
        },
      ],
    }
    Mirador.viewer(config, [...miradorImageToolsPlugin])
  },
}
</script>
