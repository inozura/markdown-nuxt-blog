<template>
  <div>
        <vue-typed-js :autoInsertCss="true" :cursorChar="'_'" :typeSpeed="100" :backSpeed="60" :fadeOut="true" :loop="true" :strings="[`I'am Novandra Zulfi Ramadhan`, 'iNozura']">
            <div v-if="big" style="margin-left: auto">
                <h4><span class="typing"></span></h4>
            </div>
            <div v-else style="margin-left: auto">
                <h5><span class="typing"></span></h5>
            </div>
        </vue-typed-js>
  </div>
</template>

<script>
export default {
 props: {
     big: {
         type: Boolean,
         default: true
     }
 }
}
</script>