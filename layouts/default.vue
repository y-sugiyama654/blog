<template>
  <div>
    <nav class="flex justify-between flex-wrap bg-teal-500 p-6">
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg"><path d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"/></svg>
        <span class="font-semibold text-xl tracking-tight">Tailwind CSS</span>
      </div>
      <div>
        <p href="#" class="inline-block text-xl px-4 py-2 leading-none font-black text-white mt-4 lg:mt-0">ペチパーSUGIYAMAの技術ブログ</p>
      </div>
      <div></div>
    </nav>
    <div class="w-full bg-gray-200">
      <div class="bg-white mx-16">
        <div>
          <p class="text-5xl text-center pt-6">ブログ一覧</p>
        </div>
        <div class="flex mb-4">
          <div class="w-3/4 p-2 text-center">
            <main><nuxt /></main>
          </div>
          <div class="w-1/4 p-2 text-center">
            <Sidebar></Sidebar>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Sidebar from "../components/Sidebar";
  export default {
    components: {
      Sidebar,
    },
  }
</script>

