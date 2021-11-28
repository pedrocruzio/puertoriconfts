<template>
  <main>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Artists Directory</h1>
      <posts post-type="artists" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('artists').fetch()
    } catch (e) {
      error({ message: 'artists not found' })
    }
    return { posts }
  },
}
</script>
