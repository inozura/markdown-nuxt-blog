<template>
  <div>
      <ul class="flex flex-wrap justify-center">
      <li
        v-for="sos of sosmed"
        :key="sos.slug"
        class="sm:w-full md:w-1/2 px-2 xs:mb-6 md:mb-12 article-card h-300"
      >
        <a
          :href="sos.url"
          target="_blank"
          class="flex transition-shadow duration-150 ease-in-out shadow-md hover:shadow-lg xxlmax:flex-col p-5"
        >
          <img
            v-if="sos.img"
            class="h-24 xxlmin:w-1/2 xxlmax:w-full object-cover mt-6"
            :src="sos.img"
          />
          <div
            class="p-6 flex flex-col justify-between xxlmin:w-1/2 xxlmax:w-full"
          >
            <h3 class="font-bold">{{ sos.name }}</h3>
            <p class="font-bold text-gray-600 text-sm">
              {{ sos.account }}
            </p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
    props: {
        sosmed: {
          type: Array,
        }
    }
}
</script>

<style>
.article-card {
  border-radius: 8px;
}
.article-card a {
  background-color: #fff;
  border-radius: 8px;
}
.article-card img div {
  border-radius: 8px 0 0 8px;
}
</style>