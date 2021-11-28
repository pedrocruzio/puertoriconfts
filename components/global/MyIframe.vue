<template>
  <vue-iframe
    src="https://oncyber.io/prnfts"
    frame-id="my-ifram"
    @load="onLoad"
    name="my-frame"
    width="100vw"
    height="500px"
    scrolling="false"
  />
</template>

<script>
export default {
  name: 'MyIframe',
  data: () => ({
    myIframe: null,
  }),
  methods: {
    onLoad(frame) {
      this.myIframe = frame.contentWindow
    },
  },
}
</script>