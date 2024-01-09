<template>
    <main>
      <header class="header">
        <div class="web_title font-title">La Flecha</div>
        <nav class="nav">
          <div class="nav-group">
            <ul class="group-list">
              <li><a href="#" class="font-title" >about</a></li>
            </ul>
          </div>
          <div class="nav-absolute"></div>
        </nav>
      </header>
  
      <section class="container grid grid-cols-2 md:grid-cols-5 gap-4 px-4 py-2 md:px-6 md:py-2">
      <div v-for="(item, index) in items" :key="index" class="group">
        <a :href="item.pageLink">
          <img
            :src="item.image"
            :alt="`Image ${index + 1}`"
            class="w-full h-auto object-cover"
            width="200"
            height="200"
          />
          <p class="mt-2 text-gray-600 dark:text-gray-400 group-hover:opacity-100 opacity-0 transition-opacity">
            {{ item.text }}
          </p>
        </a>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { image: '/entries/Dpad/Sega_master_system_d-pad.jpg', text: 'D-pad', pageLink: './art_dpad' },
        { image: '/entries/4_direcciones/GeoDirections.jpg', text: '4_direcciones', pageLink: '' },
        { image: '/entries/Arrow_keys/istockphoto-173938180-612x612.jpg', text: 'Arrow keys', pageLink: './art_arrow_keys' },
        { image: '/entries/bolsa_valores/rebote_forCrop.jpg', text: 'bolsa de valores', pageLink: './art_bolsa_valores' },
        { image: '/entries/cursor/RGBpixels.png', text: 'cursor', pageLink: './art_cursor' },
        { image: '/entries/Download_icon/istockphoto-844294300-612x612.jpg', text: 'icono de descarga', pageLink: '' },
        { image: '/entries/en_billboards/Arrows_in_Okazaki.jpeg', text: 'flechas en carteles de carretera', pageLink: '' },
        { image: '/entries/marca_vial_suelo/Santa_Isabel_Jun_2019_11_21_29_376000.jpeg', text: 'marca vial', pageLink: '' },
        { image: '/entries/panel_direccional/descarga.png', text: 'paneles direccionales', pageLink: '' },
        { image: '/entries/paul_klee/Paul-Klee.jpg', text: 'Paul Klee', pageLink: './art_paul_klee' },
        { image: '/entries/pedro_reinel/Reinel_compass_rose.png', text: 'flor de lis por Pedro Reinel', pageLink: '' },
        { image: '/entries/pioneer/pioneer.jpg', text: 'placa pioneer', pageLink: '' },
        { image: '/entries/Reciclaje/Reciclaje.jpg', text: 'reciclaje', pageLink: '/art_reciclaje' },
        { image: '/entries/this_way_up/HandlingLabelsTWU.png', text: 'this way up', pageLink: '/art_this_way_up' },
        { image: '/entries/trafico_r400/Spain_traffic_signal_r400a.svg.png', text: 'señal vertical de tráfico (es)', pageLink: '' },
        { image: '/entries/U+237B/U+237B.png', text: '⍼ (U+237B)', pageLink: 'art_U237b' },
        { image: '/entries/unicode_block/unicode_bloc.png', text: 'bloque flecha unicode', pageLink: '' },
        { image: '/entries/flecha_wikipedia/230px-Flecha_tesela.svg.png', text: 'entrada en wikipedia', pageLink: '' },
        { image: '/entries/manecilla/Right_Index_1_from_Cincinnati_Type_Foundry_1882.png', text: 'manecilla', pageLink: './art_manecilla' },
        { image: '', text: '', pageLink: '' },
      ],
    };
  },
};
</script>
  
  <style lang="sass">
  .header
    @apply flex w-full h-20 items-center px-4 md:px-6
  
  .web_title
    @apply text-2xl font-bold text-gray-800
  
  .nav
    @apply z-10 max-w-max w-full flex-1 items-center justify-center ml-auto lg:flex
  
  .nav-group
    @apply relative w-full
  
  .group-list
    @apply flex flex-1 list-none items-center justify-center space-x-1
  
  .nav-absolute
    @apply absolute left-0 top-full flex justify-center
  
  .container
    @apply mx-auto
  
  .group
    img
      aspect-ratio: 200/200 
      @apply object-cover
  
    p
      @apply text-gray-600 dark:text-gray-400 transition-opacity
      &:hover
        @apply opacity-100
  
    &.custom-bg
      @apply bg-red-400
  </style>
  