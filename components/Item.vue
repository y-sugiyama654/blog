<template>
  <div class="w-full bg-white overflow-hidden shadow-lg border rounded-lg mb-3">
    <nuxt-link :to=" '/category/' + work.fields.category.sys.id ">
      <div class="absolute bg-white py-1 px-3 rounded shadow mt-1 ml-1 text-sm">
        {{ work.fields.category.fields.name }}
      </div>
    </nuxt-link>
    <div class="flex justify-between w-full">
      <div
        class="mb-3 w-1/3 h-40 bg-center bg-cover"
        :style=" 'background-image: url(' + work.fields.image.fields.file.url + ')' "
      ></div>

      <div class="w-2/3 border-r border-b border-l border-gray-400 lg:border-l-0 lg:border-t lg:border-gray-400 bg-white rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal">
        <div class="mb-8">
          <div class="my-2">
            <nuxt-link :to=" '/work/' + work.fields.slug ">
              <h3 class="ml-3 font-bold text-2xl">{{ work.fields.title }}</h3>
            </nuxt-link>
          </div>
          <div>
            <p class="text-gray-700 text-base" v-html="summary"></p>
          </div>
        </div>
      </div>

    </div>
    <div class="flex justify-between">
      <div class="ml-4">
        <li
          v-for="tag in work.fields.tag"
          :key="tag.sys.id"
          class="list-none bg-gray-200 rounded-lg cursor-pointer px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-3"
          @click="$router.push('/tag/'+tag.sys.id)">
          {{ tag.fields.name }}
        </li>
      </div>
      <div class="mr-4">
        <p class="text-sm mt-2 text-gray-700">{{ date }} 更新</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['work'],
    data: function() {
      return {
        summary: this.work.fields.content.substr(0, 100),
        date: this.work.fields.date.substr(0, 10)
      }
    }
  }

</script>
