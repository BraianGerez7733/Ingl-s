<template>
  <main class="min-h-screen bg-white text-[#0d253d] antialiased selection:bg-[#b9b9f9] selection:text-[#1c1e54]">
    <section class="relative overflow-hidden">
      <div class="absolute inset-x-0 top-0 -z-10 h-[56rem]">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_8%_16%,#f5e9d4_0,transparent_28%),radial-gradient(circle_at_31%_9%,#f7a66d_0,transparent_30%),radial-gradient(circle_at_54%_6%,#d8c5ff_0,transparent_31%),radial-gradient(circle_at_72%_13%,#665efd_0,transparent_32%),radial-gradient(circle_at_92%_8%,#ea2261_0,transparent_26%)] opacity-95 blur-2xl"></div>
        <div class="absolute inset-x-0 bottom-0 h-64 bg-gradient-to-b from-transparent to-white"></div>
      </div>

      <header class="mx-auto flex max-w-7xl items-center justify-between px-6 py-6 lg:px-8">
        <a href="#" class="flex items-center gap-3" aria-label="Estudio Jurídico Dr. Geréz">
          <span class="grid h-9 w-9 place-items-center rounded-full bg-[#0d253d] text-sm font-medium text-white shadow-sm">BG</span>
          <span class="text-[15px] font-light tracking-[-0.2px] text-[#0d253d]">Estudio Jurídico Dr. Geréz</span>
        </a>

        <nav class="hidden items-center gap-8 text-[14px] font-light text-[#273951] md:flex">
          <a href="#especialidad" class="hover:text-[#533afd]">Especialidad</a>
          <a href="#metodo" class="hover:text-[#533afd]">Método</a>
          <a href="#casos" class="hover:text-[#533afd]">Casos</a>
          <a href="#faq" class="hover:text-[#533afd]">FAQ</a>
          <a href="#contacto" class="hover:text-[#533afd]">Contacto</a>
        </nav>

        <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" class="rounded-full bg-[#533afd] px-4 py-2 text-[14px] font-normal leading-none text-white shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] transition hover:bg-[#4434d4] active:bg-[#2e2b8c]">
          Consultar ahora
        </a>
      </header>

      <div class="mx-auto grid max-w-7xl items-center gap-12 px-6 pb-24 pt-16 lg:grid-cols-[1.02fr_0.98fr] lg:px-8 lg:pb-32 lg:pt-24">
        <div>
          <p class="mb-6 inline-flex rounded-full bg-[#b9b9f9] px-3 py-1 text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">
            Derecho laboral · ART · accidentes de trabajo
          </p>

          <h1 class="max-w-4xl text-[42px] font-light leading-[1.03] tracking-[-1.2px] text-[#0d253d] sm:text-[56px]">
            Defensa laboral precisa para trabajadores en Argentina.
          </h1>

          <p class="mt-6 max-w-2xl text-[16px] font-light leading-[1.55] text-[#273951]">
            Representación técnica en accidentes de trabajo, enfermedades profesionales, apelaciones ante Comisión Médica, reclamos contra ART y conflictos laborales. Estrategia clara, documentación ordenada y seguimiento procesal constante.
          </p>

          <div class="mt-8 flex flex-col gap-3 sm:flex-row">
            <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" class="inline-flex min-h-11 items-center justify-center rounded-full bg-[#533afd] px-5 py-3 text-[16px] font-normal leading-none text-white transition hover:bg-[#4434d4] active:bg-[#2e2b8c]">
              Iniciar consulta
            </a>
            <a href="#metodo" class="inline-flex min-h-11 items-center justify-center rounded-full border border-[#533afd] bg-white px-5 py-3 text-[16px] font-normal leading-none text-[#533afd] transition hover:bg-[#f6f9fc]">
              Ver metodología
            </a>
          </div>
        </div>

        <div class="relative">
          <div class="rounded-[16px] bg-white p-4 shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] ring-1 ring-[#e3e8ee]">
            <div class="rounded-[12px] bg-[#1c1e54] p-5 text-white">
              <div class="mb-5 flex items-center justify-between gap-4">
                <div>
                  <p class="text-[10px] font-normal uppercase tracking-[0.1px] text-white/55">Panel de caso</p>
                  <h2 class="mt-1 text-[22px] font-light tracking-[-0.22px]">Reclamo laboral activo</h2>
                </div>
                <span class="rounded-full bg-white/10 px-3 py-1 text-[11px] font-light">En seguimiento</span>
              </div>

              <div class="grid gap-3 sm:grid-cols-3">
                <div class="rounded-xl bg-white/8 p-4 ring-1 ring-white/10">
                  <p class="text-[11px] text-white/55">Etapa</p>
                  <p class="mt-2 text-[14px] font-light">Comisión Médica</p>
                </div>
                <div class="rounded-xl bg-white/8 p-4 ring-1 ring-white/10">
                  <p class="text-[11px] text-white/55">Materia</p>
                  <p class="mt-2 text-[14px] font-light">Accidente ART</p>
                </div>
                <div class="rounded-xl bg-white/8 p-4 ring-1 ring-white/10">
                  <p class="text-[11px] text-white/55">Control</p>
                  <p class="mt-2 text-[14px] font-light">Plazos críticos</p>
                </div>
              </div>

              <div class="mt-5 rounded-xl bg-[#0d253d] p-4 ring-1 ring-white/10">
                <div class="mb-3 flex items-center justify-between">
                  <p class="text-[13px] font-normal">Checklist jurídico</p>
                  <p class="text-[12px] text-white/50">Actualizado</p>
                </div>
                <div class="space-y-3 text-[13px] font-light">
                  <div class="flex items-center justify-between gap-4 border-b border-white/10 pb-3">
                    <span>Denuncia y documentación médica</span>
                    <span class="text-[#b9b9f9]">Completo</span>
                  </div>
                  <div class="flex items-center justify-between gap-4 border-b border-white/10 pb-3">
                    <span>Control de dictamen / apelación</span>
                    <span class="text-[#f96bee]">En análisis</span>
                  </div>
                  <div class="flex items-center justify-between gap-4">
                    <span>Liquidación e intereses</span>
                    <span class="text-[#f5e9d4]">Pendiente</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="especialidad" class="bg-[#f6f9fc] py-20 sm:py-24">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="max-w-3xl">
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Especialidad</p>
          <h2 class="mt-3 text-[36px] font-light leading-[1.15] tracking-[-0.96px] sm:text-[48px]">Un estudio enfocado en conflictos laborales reales.</h2>
          <p class="mt-5 text-[16px] font-light leading-[1.55] text-[#273951]">Cada caso se trabaja con lectura jurídica, análisis médico-documental y una estrategia procesal orientada a obtener una solución concreta.</p>
        </div>

        <div class="mt-12 grid gap-5 md:grid-cols-3">
          <article v-for="item in specialties" :key="item.title" class="rounded-xl border border-[#e3e8ee] bg-white p-8 shadow-[rgba(0,55,112,0.08)_0_1px_3px]">
            <div class="mb-6 grid h-10 w-10 place-items-center rounded-full bg-[#b9b9f9] text-[#4434d4]">{{ item.icon }}</div>
            <h3 class="text-[26px] font-light leading-[1.12] tracking-[-0.26px]">{{ item.title }}</h3>
            <p class="mt-4 text-[15px] font-light leading-[1.55] text-[#61718a]">{{ item.copy }}</p>
          </article>
        </div>
      </div>
    </section>

    <section id="metodo" class="py-20 sm:py-28">
      <div class="mx-auto grid max-w-7xl gap-10 px-6 lg:grid-cols-[0.9fr_1.1fr] lg:px-8">
        <div class="rounded-xl bg-[#f5e9d4] p-8 lg:p-10">
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Método de trabajo</p>
          <h2 class="mt-3 text-[36px] font-light leading-[1.12] tracking-[-0.96px]">Orden técnico desde el primer contacto.</h2>
          <p class="mt-5 text-[15px] font-light leading-[1.6] text-[#273951]">El objetivo es reducir incertidumbre: saber qué reclamar, qué documentación falta, qué plazo controla el caso y cuál es el próximo movimiento procesal.</p>
        </div>

        <div class="grid gap-4">
          <div v-for="(step, index) in steps" :key="step.title" class="rounded-xl border border-[#e3e8ee] bg-white p-6 shadow-[rgba(0,55,112,0.08)_0_1px_3px]">
            <div class="flex gap-5">
              <span class="mt-1 grid h-8 w-8 shrink-0 place-items-center rounded-full bg-[#533afd] text-[13px] font-normal text-white [font-feature-settings:'tnum']">{{ index + 1 }}</span>
              <div>
                <h3 class="text-[20px] font-light tracking-[-0.2px]">{{ step.title }}</h3>
                <p class="mt-2 text-[15px] font-light leading-[1.55] text-[#61718a]">{{ step.copy }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="casos" class="bg-[#1c1e54] py-20 text-white sm:py-24">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="grid gap-10 lg:grid-cols-[0.8fr_1.2fr]">
          <div>
            <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-white/60">Áreas de reclamo</p>
            <h2 class="mt-3 text-[36px] font-light leading-[1.15] tracking-[-0.96px] sm:text-[48px]">Asistencia jurídica para etapas críticas.</h2>
          </div>
          <div class="grid gap-4 sm:grid-cols-2">
            <div v-for="caseType in caseTypes" :key="caseType" class="rounded-xl bg-white/8 p-6 ring-1 ring-white/10">
              <p class="text-[15px] font-light leading-[1.5]">{{ caseType }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="faq" class="bg-[#f6f9fc] py-20 sm:py-24">
      <div class="mx-auto grid max-w-7xl gap-10 px-6 lg:grid-cols-[0.9fr_1.1fr] lg:px-8">
        <div>
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Preguntas frecuentes</p>
          <h2 class="mt-3 text-[36px] font-light leading-[1.12] tracking-[-0.96px] sm:text-[48px]">Información inicial antes de consultar.</h2>
          <p class="mt-5 text-[15px] font-light leading-[1.6] text-[#273951]">Este bloque usa Headless UI Disclosure, adaptado al diseño premium de la landing.</p>
        </div>

        <div class="w-full rounded-2xl bg-white p-2 shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] ring-1 ring-[#e3e8ee]">
          <Disclosure v-slot="{ open }">
            <DisclosureButton class="flex w-full justify-between rounded-lg bg-[#f6f9fc] px-4 py-3 text-left text-sm font-medium text-[#0d253d] hover:bg-[#eef2ff] focus:outline-none focus-visible:ring focus-visible:ring-[#533afd]/75">
              <span>What is your refund policy?</span>
              <ChevronUpIcon :class="open ? 'rotate-180 transform' : ''" class="h-5 w-5 text-[#533afd] transition" />
            </DisclosureButton>
            <DisclosurePanel class="px-4 pb-2 pt-4 text-sm leading-6 text-[#64748d]">
              If you're unhappy with your purchase for any reason, email us within 90 days and we'll refund you in full, no questions asked.
            </DisclosurePanel>
          </Disclosure>

          <Disclosure as="div" class="mt-2" v-slot="{ open }">
            <DisclosureButton class="flex w-full justify-between rounded-lg bg-[#f6f9fc] px-4 py-3 text-left text-sm font-medium text-[#0d253d] hover:bg-[#eef2ff] focus:outline-none focus-visible:ring focus-visible:ring-[#533afd]/75">
              <span>Do you offer technical support?</span>
              <ChevronUpIcon :class="open ? 'rotate-180 transform' : ''" class="h-5 w-5 text-[#533afd] transition" />
            </DisclosureButton>
            <DisclosurePanel class="px-4 pb-2 pt-4 text-sm leading-6 text-[#64748d]">
              No.
            </DisclosurePanel>
          </Disclosure>
        </div>
      </div>
    </section>

    <section id="contacto" class="py-20 sm:py-28">
      <div class="mx-auto max-w-5xl px-6 text-center lg:px-8">
        <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Contacto</p>
        <h2 class="mt-3 text-[40px] font-light leading-[1.1] tracking-[-1.2px] sm:text-[56px]">Consultá tu caso laboral con documentación a la vista.</h2>
        <p class="mx-auto mt-6 max-w-2xl text-[16px] font-light leading-[1.55] text-[#273951]">Enviá una breve descripción del problema, fecha del hecho, ART o empleador interviniente y documentación disponible. Se revisa la vía más conveniente.</p>
        <div class="mt-8 flex flex-col items-center justify-center gap-3 sm:flex-row">
          <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" class="inline-flex min-h-11 items-center justify-center rounded-full bg-[#533afd] px-5 py-3 text-[16px] font-normal leading-none text-white transition hover:bg-[#4434d4] active:bg-[#2e2b8c]">
            Escribir por WhatsApp
          </a>
          <a href="mailto:estudiojuridicobg.clientes@gmail.com" class="inline-flex min-h-11 items-center justify-center rounded-full border border-[#533afd] bg-white px-5 py-3 text-[16px] font-normal leading-none text-[#533afd] transition hover:bg-[#f6f9fc]">
            Enviar email
          </a>
        </div>
      </div>
    </section>

    <footer class="border-t border-[#e3e8ee] bg-white px-6 py-10 text-[13px] font-light text-[#64748d] lg:px-8">
      <div class="mx-auto flex max-w-7xl flex-col justify-between gap-4 sm:flex-row">
        <p>© {{ year }} Estudio Jurídico Dr. Geréz. Derecho laboral y ART.</p>
        <p>Río Grande · Tierra del Fuego · Argentina</p>
      </div>
    </footer>
  </main>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronUpIcon } from '@heroicons/vue/20/solid'

const year = new Date().getFullYear()

const specialties = [
  { icon: '⚖️', title: 'Accidentes de trabajo', copy: 'Reclamos por siniestros laborales, prestaciones médicas, incapacidad, ILT y seguimiento ante ART.' },
  { icon: '🩺', title: 'Enfermedades profesionales', copy: 'Análisis de nexo causal, tareas habituales, documentación clínica y estrategia probatoria.' },
  { icon: '📄', title: 'Apelaciones ART', copy: 'Impugnación de dictámenes, control de porcentajes de incapacidad y revisión judicial de decisiones administrativas.' },
]

const steps = [
  { title: 'Diagnóstico inicial del caso', copy: 'Se identifican hechos, fechas, empleador, ART, diagnóstico, documentación médica y estado del trámite.' },
  { title: 'Estrategia documental y procesal', copy: 'Se ordena la prueba necesaria y se define si corresponde vía administrativa, apelación o acción judicial.' },
  { title: 'Seguimiento hasta resolución', copy: 'Control de plazos, audiencias, dictámenes, pericias, liquidaciones, intimaciones y ejecución de sentencia.' },
]

const caseTypes = [
  'Rechazo de siniestro por ART.',
  'Alta médica prematura o sin prestaciones suficientes.',
  'Diferencias en porcentaje de incapacidad.',
  'Falta de pago de prestaciones dinerarias.',
  'Apelación de dictámenes de Comisión Médica.',
  'Ejecución de sentencia y cobro de indemnizaciones.',
]
</script>
