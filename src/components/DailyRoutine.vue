<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faBone, faPaw, faCalendarDays } from '@fortawesome/free-solid-svg-icons'

const dailyRoutine = [
  {
    title: 'Spacer',
    icon: faPaw,
    description: [
      'Komenda, po której reaguje, żeby się zbierać do wyjścia: <span class="font-semibold">"Spacer"</span>.',
      'Jeżeli ciągnie na spacerze, zatrzymać się i poczekać, aż siądzie i popatrzy na was.',
      'Kontakt z innymi psami — starać się, żeby nie był zbyt blisko, a obserwował z daleka; absorbować jego uwagę, aby olał inne psy (np. smaczki).',
      'Warto wziąć lepsze smaczki — wtedy chętniej przybieka na spacerze i mniej ciągnie, chodzi przy nodze.',
      'Uczymy psa jak najdłuższego wytrzymywania siku, dlatego staramy się go wypuszczać na dwór co 3 h.',
      'Po każdym posiłku, po 15 min, wychodzimy z nim na dwór.',
      'Najlepiej, żeby raz w ciągu dnia miał dłuższy spacer 30-60 min + jakąś interakcję, np. rzucanie patyka/piłki.',
      'Przed pójściem spać wypuścić go na dwór, aby się załatwił i nie musiał w nocy wstawać.',
      'Starać się chodzić w miejsca, gdzie będą też ludzie i inne psy, żeby się przyzwyczajał do nich.',
    ],
  },
  {
    title: 'Jedzenie',
    icon: faBone,
    description: [
      'Posiłki dajemy 3 razy dziennie o stałej porze.',
      'Godziny posiłków: <span class="font-semibold">9:30, 15:30, 19:30</span>.',
      'Komenda, po której może zacząć jeść: <span class="font-semibold">"Jedzenie"</span>.',
      'Jednorazowa porcja karmy: <span class="font-semibold">150 g</span>.',
      'Dodatkowo podczas nauki można dawać mu suchą karmę (gorzej reaguje) lub pokrojone kawałki mokrej karmy jako nagrodę.',
      'Raz dziennie pół tabletki na stawy.',
      'Jeżeli nie chce spać albo jest zestresowany, dać Konga — wypełnić go suchą karmą, zalać wodą na kilka minut, zamrozić i dać do lizania.',
    ],
  },
  {
    title: 'Codzienność',
    icon: faCalendarDays,
    description: [
      'Dawać mu zabawkę/gryzaka, gdy nie śpi, żeby się nie nudził.',
      'Zabawy w ciągu dnia: przeciąganie szarpaka, węszenie smakołyków, rzucanie piłki.',
      'Jeżeli bardzo przeszkadza, dać żwacza do klatki — zajmie go to na kilka minut.',
      'Nauka komend 2/3/4 razy dziennie po 15 minut.',
      'Woda zawsze dostępna.',
      'Niereagowanie, gdy szczeka lub skacze.',
      'Jasno określone zasady, żeby każdy się ich trzymał — pies będzie się buntować, jeśli nie.',
      'Niech wszystkie zabawki nie leżą na wierzchu (dawać 2), zmieniać je raz na jakiś czas, żeby były dla niego bardziej atrakcyjne.',
      'Mycie zębów raz na 4 dni, szczoteczka na palec — najpierw niech poliże pastę, a potem stopniowo wprowadzać szczoteczkę.',
    ],
  },
]
</script>

<template>
  <div class="container max-w-7xl px-4 py-10 mx-auto flex flex-col items-center justify-center">
    <h2 class="text-2xl font-bold">Codzienna rutyna</h2>

    <div class="w-full mt-6 flex flex-col lg:flex-row gap-4 lg:justify-center xl:gap-10">
      <div
        v-for="(value, idx) in dailyRoutine"
        :key="idx"
        class="border border-solid border-gray-300 rounded-lg p-4 w-full md:w-auto gap-4 flex flex-col flex-1 flex-wrap"
      >
        <div class="flex items-center gap-2">
          <font-awesome-icon :icon="value.icon" />
          <h4 class="text-xl font-semibold">{{ value.title }}:</h4>
        </div>

        <ul class="list-disc list-inside">
          <li v-for="(text, index) in value.description" :key="index" class="mt-2" v-html="text" />
        </ul>
      </div>
    </div>
  </div>
</template>
