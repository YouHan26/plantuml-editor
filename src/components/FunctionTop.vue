<template>
  <div class="row functionTop">
    <div class="col-sm-12">
      <div class="row form-group">
        <div class="col-sm-12">
          <parameters></parameters>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js">
/* @flow */

// components
import Parameters from './Parameters'

export default {
  name: 'FunctionTop',
  components: {
    Parameters
  },
  data(): any {
    return {
      winKey: this.$store.state.plantumlEditor.renderUMLKey.win,
      macKey: this.$store.state.plantumlEditor.renderUMLKey.mac,
      snippetWinKey: this.$store.state.plantumlEditor.snippetKey.win,
      snippetMacKey: this.$store.state.plantumlEditor.snippetKey.mac
    }
  },
  computed: {
    isHTTPS(): boolean {
      return this.$store.state.plantumlEditor.isHTTPS
    },
    url(): string {
      return this.$store.state.plantumlEditor.url
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
