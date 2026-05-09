<template>
  <main class="min-h-screen bg-white text-[#0d253d] antialiased selection:bg-[#b9b9f9] selection:text-[#1c1e54]">
    <section class="relative overflow-hidden">
      <div class="absolute inset-x-0 top-0 -z-10 h-[58rem]">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_8%_16%,#f5e9d4_0,transparent_28%),radial-gradient(circle_at_31%_9%,#f7a66d_0,transparent_30%),radial-gradient(circle_at_54%_6%,#d8c5ff_0,transparent_31%),radial-gradient(circle_at_72%_13%,#665efd_0,transparent_32%),radial-gradient(circle_at_92%_8%,#ea2261_0,transparent_26%)] opacity-95 blur-2xl"></div>
        <div class="absolute inset-x-0 bottom-0 h-64 bg-gradient-to-b from-transparent to-white"></div>
      </div>

      <header class="mx-auto flex max-w-7xl items-center justify-between px-6 py-6 lg:px-8">
        <a href="#" class="flex items-center gap-3" aria-label="Estudio Jurídico Dr. Geréz">
          <span class="grid h-9 w-9 place-items-center rounded-full bg-[#0d253d] text-sm font-medium text-white shadow-sm">BG</span>
          <span class="text-[15px] font-light tracking-[-0.2px] text-[#0d253d]">Estudio Jurídico Dr. Geréz</span>
        </a>

        <nav class="hidden items-center gap-8 text-[14px] font-light text-[#273951] md:flex">
          <a v-for="link in navLinks" :key="link.href" :href="link.href" class="hover:text-[#533afd]">{{ link.label }}</a>
        </nav>

        <div class="hidden md:block">
          <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" class="rounded-full bg-[#533afd] px-4 py-2 text-[14px] font-normal leading-none text-white shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] transition hover:bg-[#4434d4] active:bg-[#2e2b8c]">
            Reservar consulta
          </a>
        </div>

        <Menu as="div" class="relative md:hidden">
          <MenuButton class="rounded-full border border-[#e3e8ee] bg-white px-4 py-2 text-[14px] text-[#0d253d] shadow-sm">
            Menú
          </MenuButton>
          <MenuItems class="absolute right-0 z-20 mt-2 w-64 rounded-2xl border border-[#e3e8ee] bg-white p-2 shadow-[rgba(0,55,112,0.12)_0_12px_32px] focus:outline-none">
            <MenuItem v-for="link in navLinks" :key="link.href" v-slot="{ active }">
              <a :href="link.href" :class="[active ? 'bg-[#f6f9fc] text-[#533afd]' : 'text-[#273951]', 'block rounded-xl px-4 py-3 text-sm']">{{ link.label }}</a>
            </MenuItem>
            <MenuItem v-slot="{ active }">
              <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" :class="[active ? 'bg-[#4434d4]' : 'bg-[#533afd]', 'mt-1 block rounded-xl px-4 py-3 text-sm text-white']">Reservar consulta</a>
            </MenuItem>
          </MenuItems>
        </Menu>
      </header>

      <div class="mx-auto grid max-w-7xl items-center gap-12 px-6 pb-24 pt-16 lg:grid-cols-[1.02fr_0.98fr] lg:px-8 lg:pb-32 lg:pt-24">
        <div>
          <p class="mb-6 inline-flex rounded-full bg-[#b9b9f9] px-3 py-1 text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">
            Derecho laboral · ART · accidentes de trabajo
          </p>

          <h1 class="max-w-4xl text-[42px] font-light leading-[1.03] tracking-[-1.2px] text-[#0d253d] sm:text-[56px]">
            Defensa laboral clara y efectiva.
          </h1>

          <p class="mt-6 max-w-2xl text-[16px] font-light leading-[1.55] text-[#273951]">
            Salud primero; indemnización bien calculada. Acompañamiento integral desde la Comisión Médica hasta la sentencia, con estrategia probatoria, cautelar y liquidatoria.
          </p>

          <ul class="mt-6 space-y-3 text-[15px] font-light text-[#273951]">
            <li v-for="bullet in heroBullets" :key="bullet" class="flex gap-3">
              <CheckCircleIcon class="mt-0.5 h-5 w-5 shrink-0 text-[#533afd]" />
              <span>{{ bullet }}</span>
            </li>
          </ul>

          <div class="mt-8 flex flex-col gap-3 sm:flex-row">
            <a href="https://wa.me/5492964540752" target="_blank" rel="noreferrer" class="inline-flex min-h-11 items-center justify-center rounded-full bg-[#533afd] px-5 py-3 text-[16px] font-normal leading-none text-white transition hover:bg-[#4434d4] active:bg-[#2e2b8c]">
              Reservar consulta
            </a>
            <a href="#casos" class="inline-flex min-h-11 items-center justify-center rounded-full border border-[#533afd] bg-white px-5 py-3 text-[16px] font-normal leading-none text-[#533afd] transition hover:bg-[#f6f9fc]">
              Ver casos y etapas
            </a>
          </div>
        </div>

        <div class="relative">
          <div class="rounded-[16px] bg-white p-4 shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] ring-1 ring-[#e3e8ee]">
            <div class="rounded-[12px] bg-[#1c1e54] p-5 text-white">
              <div class="mb-5 flex items-center justify-between gap-4">
                <div>
                  <p class="text-[10px] font-normal uppercase tracking-[0.1px] text-white/55">Panel estratégico</p>
                  <h2 class="mt-1 text-[22px] font-light tracking-[-0.22px]">Caso laboral activo</h2>
                </div>
                <span class="rounded-full bg-white/10 px-3 py-1 text-[11px] font-light">En seguimiento</span>
              </div>

              <div class="grid gap-3 sm:grid-cols-3">
                <div v-for="metric in caseMetrics" :key="metric.label" class="rounded-xl bg-white/8 p-4 ring-1 ring-white/10">
                  <p class="text-[11px] text-white/55">{{ metric.label }}</p>
                  <p class="mt-2 text-[14px] font-light">{{ metric.value }}</p>
                </div>
              </div>

              <div class="mt-5 rounded-xl bg-[#0d253d] p-4 ring-1 ring-white/10">
                <div class="mb-3 flex items-center justify-between">
                  <p class="text-[13px] font-normal">Checklist jurídico</p>
                  <p class="text-[12px] text-white/50">Actualizado</p>
                </div>
                <div class="space-y-3 text-[13px] font-light">
                  <div v-for="item in checklist" :key="item.label" class="flex items-center justify-between gap-4 border-b border-white/10 pb-3 last:border-b-0 last:pb-0">
                    <span>{{ item.label }}</span>
                    <span :class="item.color">{{ item.status }}</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="que-hacemos" class="bg-[#f6f9fc] py-20 sm:py-24">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="max-w-3xl">
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Qué hacemos</p>
          <h2 class="mt-3 text-[36px] font-light leading-[1.15] tracking-[-0.96px] sm:text-[48px]">Soluciones jurídicas para etapas críticas.</h2>
          <p class="mt-5 text-[16px] font-light leading-[1.55] text-[#273951]">Cada reclamo se aborda con lectura médica, documentación ordenada, control de plazos y una estrategia orientada al resultado.</p>
        </div>

        <div class="mt-12 grid gap-5 md:grid-cols-3">
          <article v-for="item in services" :key="item.title" class="rounded-xl border border-[#e3e8ee] bg-white p-8 shadow-[rgba(0,55,112,0.08)_0_1px_3px] transition hover:-translate-y-1 hover:shadow-[rgba(0,55,112,0.10)_0_12px_28px]">
            <component :is="item.icon" class="mb-6 h-10 w-10 rounded-full bg-[#b9b9f9] p-2 text-[#4434d4]" />
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
          <p class="mt-5 text-[15px] font-light leading-[1.6] text-[#273951]">La consulta inicial busca definir qué reclamar, qué documentación falta, qué plazo controla el caso y cuál es el próximo movimiento procesal.</p>
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
        <div class="flex items-start justify-between gap-6">
          <div class="max-w-3xl">
            <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-white/60">Casos y etapas</p>
            <h2 class="mt-3 text-[36px] font-light leading-[1.15] tracking-[-0.96px] sm:text-[48px]">Intervención jurídica en momentos decisivos.</h2>
          </div>
          <div class="flex gap-2">
            <button @click="prevCase" class="grid h-10 w-10 place-items-center rounded-full bg-white/10 ring-1 ring-white/10 hover:bg-white/15" aria-label="Caso anterior">‹</button>
            <button @click="nextCase" class="grid h-10 w-10 place-items-center rounded-full bg-white/10 ring-1 ring-white/10 hover:bg-white/15" aria-label="Caso siguiente">›</button>
          </div>
        </div>

        <article class="mt-10 rounded-2xl bg-white/8 p-8 ring-1 ring-white/10">
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-white/50">{{ cases[currentCase].tag }}</p>
          <h3 class="mt-3 text-[34px] font-light leading-tight tracking-[-0.8px]">{{ cases[currentCase].title }}</h3>
          <p class="mt-4 max-w-3xl text-[16px] font-light leading-7 text-white/75">{{ cases[currentCase].copy }}</p>
        </article>
      </div>
    </section>

    <section id="faq" class="bg-[#f6f9fc] py-20 sm:py-24">
      <div class="mx-auto grid max-w-7xl gap-10 px-6 lg:grid-cols-[0.9fr_1.1fr] lg:px-8">
        <div>
          <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Preguntas frecuentes</p>
          <h2 class="mt-3 text-[36px] font-light leading-[1.12] tracking-[-0.96px] sm:text-[48px]">Información inicial antes de consultar.</h2>
          <p class="mt-5 text-[15px] font-light leading-[1.6] text-[#273951]">Respuestas orientativas para ordenar documentación, plazos y próximos pasos.</p>
        </div>

        <div class="w-full rounded-2xl bg-white p-2 shadow-[rgba(0,55,112,0.08)_0_8px_24px,rgba(0,55,112,0.04)_0_2px_6px] ring-1 ring-[#e3e8ee]">
          <Disclosure v-for="faq in faqs" :key="faq.question" as="div" class="mt-2 first:mt-0" v-slot="{ open }">
            <DisclosureButton class="flex w-full justify-between rounded-lg bg-[#f6f9fc] px-4 py-3 text-left text-sm font-medium text-[#0d253d] hover:bg-[#eef2ff] focus:outline-none focus-visible:ring focus-visible:ring-[#533afd]/75">
              <span>{{ faq.question }}</span>
              <ChevronUpIcon :class="open ? 'rotate-180 transform' : ''" class="h-5 w-5 text-[#533afd] transition" />
            </DisclosureButton>
            <DisclosurePanel class="px-4 pb-2 pt-4 text-sm leading-6 text-[#64748d]">
              {{ faq.answer }}
            </DisclosurePanel>
          </Disclosure>
        </div>
      </div>
    </section>

    <section id="contacto" class="py-20 sm:py-28">
      <div class="mx-auto max-w-5xl px-6 text-center lg:px-8">
        <p class="text-[10px] font-medium uppercase tracking-[0.1px] text-[#4434d4]">Contacto</p>
        <h2 class="mt-3 text-[40px] font-light leading-[1.1] tracking-[-1.2px] sm:text-[56px]">Reservá una consulta con documentación a la vista.</h2>
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
import { ref } from 'vue'
import { Disclosure, DisclosureButton, DisclosurePanel, Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
import { ChevronUpIcon } from '@heroicons/vue/20/solid'
import { CheckCircleIcon, ScaleIcon, ShieldCheckIcon, ClipboardDocumentCheckIcon } from '@heroicons/vue/24/outline'

const year = new Date().getFullYear()
const currentCase = ref(0)

const navLinks = [
  { href: '#que-hacemos', label: 'Qué hacemos' },
  { href: '#metodo', label: 'Método' },
  { href: '#casos', label: 'Casos' },
  { href: '#faq', label: 'FAQ' },
  { href: '#contacto', label: 'Contacto' },
]

const heroBullets = [
  'Accidentes y enfermedades laborales bajo Ley de Riesgos del Trabajo.',
  'Medidas cautelares para prestaciones médicas y tratamientos urgentes.',
  'Apelaciones, pericias, liquidaciones, intereses y ejecución de sentencia.',
]

const caseMetrics = [
  { label: 'Etapa', value: 'CM / Judicial' },
  { label: 'Materia', value: 'Accidente ART' },
  { label: 'Control', value: 'Plazos críticos' },
]

const checklist = [
  { label: 'Denuncia y documentación médica', status: 'Completo', color: 'text-[#b9b9f9]' },
  { label: 'Control de dictamen / apelación', status: 'En análisis', color: 'text-[#f96bee]' },
  { label: 'Liquidación e intereses', status: 'Pendiente', color: 'text-[#f5e9d4]' },
]

const services = [
  { icon: ShieldCheckIcon, title: 'Cautelares médicas', copy: 'Pedidos urgentes para asegurar prestaciones, tratamientos, estudios, medicación y cobertura inmediata cuando la salud lo exige.' },
  { icon: ScaleIcon, title: 'Apelaciones Art. 46', copy: 'Impugnación de dictámenes de Comisión Médica, revisión de incapacidad, nexo causal y alcance de las prestaciones.' },
  { icon: ClipboardDocumentCheckIcon, title: 'Ejecución y cobros', copy: 'Liquidaciones, intereses, intimaciones, transferencias y ejecución de sentencias o acuerdos incumplidos.' },
]

const steps = [
  { title: 'Diagnóstico inicial del caso', copy: 'Se identifican hechos, fechas, empleador, ART, diagnóstico, documentación médica y estado del trámite.' },
  { title: 'Estrategia documental y procesal', copy: 'Se ordena la prueba necesaria y se define si corresponde vía administrativa, apelación o acción judicial.' },
  { title: 'Seguimiento hasta resolución', copy: 'Control de plazos, audiencias, dictámenes, pericias, liquidaciones, intimaciones y ejecución de sentencia.' },
]

const cases = [
  { tag: 'Prestaciones médicas', title: 'Medida cautelar por tratamiento urgente.', copy: 'Intervención orientada a restablecer cobertura médica cuando la ART omite, demora o interrumpe prestaciones esenciales para la recuperación del trabajador.' },
  { tag: 'Incapacidad laboral', title: 'Revisión de porcentaje y nexo causal.', copy: 'Análisis del dictamen administrativo, historia clínica, baremo aplicable y prueba médica para cuestionar incapacidades insuficientes o rechazos improcedentes.' },
  { tag: 'Cobro de sentencia', title: 'Ejecución, intereses y transferencia.', copy: 'Control de cumplimiento, liquidación, intimación y pedido de transferencia para que el resultado judicial se traduzca en cobro efectivo.' },
]

const faqs = [
  { question: '¿Qué documentación conviene enviar para la primera consulta?', answer: 'DNI, recibos de sueldo, denuncia del siniestro, constancias de ART, estudios médicos, certificados, alta médica y dictámenes de Comisión Médica si existen.' },
  { question: '¿Se puede reclamar si la ART rechazó el accidente o la enfermedad?', answer: 'Sí. El rechazo puede ser revisado administrativa o judicialmente, según el estado del trámite, la prueba médica y los plazos vigentes.' },
  { question: '¿Qué pasa si la ART no brinda tratamiento?', answer: 'Cuando hay urgencia y verosimilitud del derecho, puede evaluarse una medida cautelar para requerir prestaciones médicas inmediatas.' },
]

function nextCase() {
  currentCase.value = (currentCase.value + 1) % cases.length
}

function prevCase() {
  currentCase.value = (currentCase.value - 1 + cases.length) % cases.length
}
</script>
