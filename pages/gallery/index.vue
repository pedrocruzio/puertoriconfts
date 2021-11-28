<template>
  <div>
    <div>
      <header class="bg-white shadow">
        <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
          <h1 class="text-3xl font-bold leading-tight text-gray-900">Virtual Gallery</h1>
        </div>
      </header>
      <main style="height: 80vh" class="p-0">
        <MyIframe />
      </main>
    </div>
  </div>
</template>

<script>
import MyIframe from '~/components/global/MyIframe.vue'

export default {
  components: MyIframe,
}
</script>