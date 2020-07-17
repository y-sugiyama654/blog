<template>
  <div class="font-main flex flex-wrap justify-around border rounded-lg mr-4">
    <div class="w-64 my-6 ml-2">
      <!-- 自己紹介文 -->
      <div>
        <div class="flex">
          <div class="bg-center bg-cover w-16 h-16 mr-2 rounded-full shadow photo"></div>
          <div>
            <h1 class="font-bold">ペチパーSUGIYAMA</h1>
            <p class="text-xs text-justify">WebエンジニアのペチパーSUGIYAMAです。Vue.js, Nuxt.jsが大好きです。Pythonも使います。ご連絡はDMからどうぞ。</p>
          </div>
        </div>
        <div class="flex justify-around mt-5 text-xs">
          <nuxt-link to="/">
            <button>
              <fa-layers full-width class="fa-2x block mx-auto mb-1">
                <fa :icon="faCode" />
              </fa-layers>
              Works
            </button>
          </nuxt-link>
          <a href="http://" target="_blank" rel="noopener noreferrer">
            <button>
              <fa-layers full-width class="fa-2x block mx-auto mb-1">
                <fa :icon="faTwitter" />
              </fa-layers>
              Twitter
            </button>
          </a>
          <a href="https://github.com/si-zerodarkthirty" target="_blank" rel="noopener noreferrer">
            <button>
              <fa-layers full-width class="fa-2x block mx-auto mb-1">
                <fa :icon="faGithub" />
              </fa-layers>
              GitHub
            </button>
          </a>
        </div>
        <input type="text" placeholder="Keywords" class="bg-gray-300 p-2 text-xs rounded w-full mt-5 focus:outline-none" v-model="keyword" @keypress.enter="$router.push('/search/' + keyword)">
      </div>
      <!-- タグ一覧 -->
      <div class="mt-6">
        <hr>
        <div class="bg-gray-300 mt-2">
          <p class="font-bold">タグ一覧</p>
          <div class="bg-white p-3">
            <a class="border border-green-500 p-1 border rounded">Docker</a>
            <a class="border border-green-500 p-1 border rounded">PHP</a>
            <a class="border border-green-500 p-1 border rounded">Laravel</a>
          </div>
        </div>
      </div>
      <!-- カテゴリ一覧 -->
      <div class="mt-6">
        <hr>
        <div class="bg-gray-300 mt-2">
          <p class="font-bold">カテゴリ一覧</p>
          <div class="bg-white p-3">
            <a class="border border-green-500 p-1 border rounded">Web開発</a>
            <a class="border border-green-500 p-1 border rounded">コーディング</a>
          </div>
        </div>
      </div>
      <!-- 最新記事 -->
      <div class="mt-6">
        <hr>
        <div class="bg-gray-300 mt-2">
          <p class="font-bold">最新記事</p>
          <div class="bg-white p-3">
          </div>
        </div>
      </div>
    </div>
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

<style>
  main {
    /*max-width: 550px;*/
  }
  .photo {
    min-width: 4rem;
    min-height: 4rem;
    background-image: url('https://avatars3.githubusercontent.com/u/42257182?s=400&u=70f63f8b73ae0f711f45e7a8340e3424acc4fa98&v=4');
  }
  button:focus {
    outline: none;
  }
</style>
