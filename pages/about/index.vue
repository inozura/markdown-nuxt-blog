<template>
  <div
    class="flex lg:h-screen w-screen lg:overflow-hidden xs:flex-col lg:flex-row"
  >
    <div class="relative lg:w-1/2 xs:w-full xs:h-auto md:h-full">
      <img
        :src="img"
        :alt="name"
        class="absolute h-full w-full object-cover"
      />
    </div>
    <div class="overlay"></div>
    <div class="absolute top-32 xs:px-6 md:px-6 text-white lg:w-auto w-full">
      <!-- <NuxtLink to="/"><svg-icon /></NuxtLink> -->
      <div class="mt-64 -mb-3 flex flex-col uppercase text-sm">
        <h1 class="text-4xl font-bold">
          {{ name }}
        </h1>
        <p class="mb-4">{{ bio }}</p>
        <p class="inline-block mt-auto">place</p>
      </div>
    </div>
    <div
      class="relative xs:py-8 xs:px-8 lg:py-32 lg:px-16 lg:w-1/2 xs:w-full h-auto lg:overflow-y-scroll markdown-body post-right custom-scroll"
    >
      <NuxtLink to="/"
        ><p class="hover:underline">Back to All Articles</p></NuxtLink
      >
      <h3 class="mb-4 font-bold text-4xl">
        Here are a list of my social media:
      </h3>
      <sosmed-card :sosmed="sosmed" />
    </div>
  </div>
</template>

<script>
import SvgIcon from '../../components/SvgIcon'
export default {
  async asyncData ({app}) {
    const wholeMD = await import(`~/contents/author/nozura.md`)
    const nozura = wholeMD.attributes
    return {
        name: nozura.name,
        img: nozura.img,
        alt: nozura.alt,
        bio: nozura.bio,
        place: nozura.place,
        sosmed: nozura.sosmed
    }
  },
  components: { SvgIcon }
}
</script>
