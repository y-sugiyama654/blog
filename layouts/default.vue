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
    <main class="w-full mt-10">
      <nuxt />
    </main>
  </div>
</template>

<script>
  import { faTwitter } from '@fortawesome/free-brands-svg-icons'
  import { faGithub } from '@fortawesome/free-brands-svg-icons'
  import { faCode } from '@fortawesome/free-solid-svg-icons'
  export default {
    data() {
      return {
        keyword: ''
      }
    },
    computed: {
      faTwitter () {
        return faTwitter
      },
      faGithub () {
        return faGithub
      },
      faCode () {
        return faCode
      }
    }
  }
</script>

