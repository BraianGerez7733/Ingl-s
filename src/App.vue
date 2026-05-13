<template>
  <main class="min-h-screen overflow-hidden bg-[#fff2f8] text-[#4a1230]">
    <section class="relative px-5 py-10 sm:px-8 lg:px-12">
      <div class="absolute inset-0 -z-10 bg-[radial-gradient(circle_at_10%_10%,#ffd1e8_0,transparent_28%),radial-gradient(circle_at_90%_0%,#d8c5ff_0,transparent_30%),radial-gradient(circle_at_55%_95%,#ffe6a7_0,transparent_32%)]"></div>

      <header class="mx-auto max-w-6xl text-center">
        <p class="inline-flex rounded-full bg-white/70 px-4 py-2 text-xs font-bold uppercase tracking-[0.24em] text-[#c02668] shadow-sm ring-1 ring-white/70">
          Recuerdos familiares
        </p>
        <h1 class="mt-6 text-5xl font-black tracking-tight text-[#831843] sm:text-7xl">
          Nuestro muro de momentos
        </h1>
        <p class="mx-auto mt-5 max-w-2xl text-lg leading-8 text-[#9d174d]">
          Fotos, pequeñas historias y recuerdos que guardan lo más importante: amor, juego, compañía y familia.
        </p>
      </header>

      <section class="mx-auto mt-12 grid max-w-7xl gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <button
          v-for="photo in photos"
          :key="photo.id"
          type="button"
          :class="['group relative rounded-[2rem] bg-white p-3 text-left shadow-[0_20px_60px_rgba(190,24,93,0.18)] ring-1 ring-white/80 transition duration-300 hover:-translate-y-2 hover:rotate-0 hover:shadow-[0_24px_70px_rgba(190,24,93,0.28)] active:scale-[0.98]', photo.rotate]"
          @click="selectedPhoto = photo"
        >
          <span class="absolute -top-3 left-7 z-10 rounded-full bg-[#fdf2f8] px-4 py-2 text-2xl shadow-md ring-1 ring-[#fbcfe8]">
            {{ photo.emoji }}
          </span>
          <div class="overflow-hidden rounded-[1.6rem] bg-[#fce7f3]">
            <img
              :src="photo.src"
              :alt="photo.title"
              class="h-80 w-full object-cover transition duration-500 group-hover:scale-105 sm:h-96"
              loading="lazy"
            />
          </div>
          <div class="px-3 pb-4 pt-5">
            <h2 class="text-2xl font-black text-[#831843]">{{ photo.title }}</h2>
            <p class="mt-2 text-sm leading-6 text-[#9d174d]">{{ photo.caption }}</p>
          </div>
        </button>
      </section>
    </section>

    <Transition name="modal-fade">
      <section
        v-if="selectedPhoto"
        class="fixed inset-0 z-50 flex items-center justify-center bg-[#1f0714]/90 p-4 backdrop-blur-md"
        role="dialog"
        aria-modal="true"
        @click="selectedPhoto = null"
      >
        <div class="relative max-h-[94vh] w-full max-w-5xl overflow-hidden rounded-[2rem] bg-white shadow-2xl" @click.stop>
          <button
            type="button"
            class="absolute right-4 top-4 z-20 grid h-12 w-12 place-items-center rounded-full bg-white/90 text-3xl font-light text-[#831843] shadow-lg transition hover:scale-105"
            aria-label="Cerrar foto ampliada"
            @click="selectedPhoto = null"
          >
            ×
          </button>
          <img
            :src="selectedPhoto.src"
            :alt="selectedPhoto.title"
            class="max-h-[72vh] w-full object-contain bg-[#1f0714]"
          />
          <div class="flex items-start gap-4 bg-white p-5 sm:p-7">
            <span class="text-4xl">{{ selectedPhoto.emoji }}</span>
            <div>
              <h3 class="text-3xl font-black text-[#831843]">{{ selectedPhoto.title }}</h3>
              <p class="mt-2 text-base leading-7 text-[#9d174d]">{{ selectedPhoto.caption }}</p>
            </div>
          </div>
        </div>
      </section>
    </Transition>
  </main>
</template>

<script setup>
import { ref } from 'vue'

const selectedPhoto = ref(null)

const photos = [
  {
    id: 'perrito',
    src: '/gallery/perrito-15-anos.jpg',
    title: '15 años juntos',
    caption: 'Una vida de compañía, amor y lealtad. Siempre conmigo.',
    emoji: '🐶',
    rotate: '-rotate-2'
  },
  {
    id: 'princesa-rosa',
    src: '/gallery/princesa-rosa.jpg',
    title: 'Nuestra princesa',
    caption: 'Luz, ternura y alegría en cada sonrisa.',
    emoji: '👑',
    rotate: 'rotate-1'
  },
  {
    id: 'capibaras',
    src: '/gallery/capibaras.jpg',
    title: 'Pequeñas sonrisas',
    caption: 'Detalles simples que hacen más linda la casa.',
    emoji: '🧸',
    rotate: '-rotate-1'
  },
  {
    id: 'antes-presente',
    src: '/gallery/antes-y-presente.jpg',
    title: 'El tiempo pasa',
    caption: 'La esencia permanece y el amor también.',
    emoji: '💖',
    rotate: 'rotate-2'
  },
  {
    id: 'princesa-lila',
    src: '/gallery/princesa-lila.jpg',
    title: 'Magia en casa',
    caption: 'Un recuerdo lleno de imaginación, juego y dulzura.',
    emoji: '✨',
    rotate: '-rotate-2'
  }
]
</script>

<style scoped>
.modal-fade-enter-active,
.modal-fade-leave-active {
  transition: opacity 0.25s ease;
}

.modal-fade-enter-from,
.modal-fade-leave-to {
  opacity: 0;
}
</style>
