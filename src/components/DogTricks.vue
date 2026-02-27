<script setup lang="ts">
import AccordionTrick from './AccordionTrick.vue'

import doMnieVideo from '@/assets/videos/do-mnie.mp4'
import siadVideo from '@/assets/videos/siad.mp4'
import lezecVideo from '@/assets/videos/lezec.mp4'
import lapaVideo from '@/assets/videos/lapa.mp4'
import prosVideo from '@/assets/videos/pros.mp4'
import czekajVideo from '@/assets/videos/czekaj.mp4'
import nogaVideo from '@/assets/videos/noga.mp4'
import srodekVideo from '@/assets/videos/srodek.mp4'
import slalomVideo from '@/assets/videos/slalom.mp4'
import nieVideo from '@/assets/videos/nie.mp4'
import obrotVideo from '@/assets/videos/obrot.mp4'
import uklonVideo from '@/assets/videos/uklon.mp4'
import proszeVideo from '@/assets/videos/prosze.mp4'

const tricks = [
  {
    name: 'Skupienie uwagi',
    command: '-',
    description:
      'Wyciągamy smaczek w bok, pies powinien wtedy spojrzeć na nas, następnie nagradzamy go smaczkiem.',
    ytLink: 'https://www.youtube.com/watch?v=K1EWibyPqqU&t=1s',
    video: '',
  },
  {
    name: 'Do mnie',
    command: 'Do mnie',
    description:
      'Wołamy "Do mnie", jeżeli przybiega, dajemy mu smaczek i chwalimy go. Warto robić w różnych odległościach i wołać go, gdy nie jest na nas skupiony.',
    ytLink: 'https://www.youtube.com/watch?v=lDCmeGN9sgg&t=1s',
    video: doMnieVideo,
  },
  {
    name: 'Siad',
    command: 'Siad',
    description:
      'Pies powinien wykonać komendę na samo słowo "siad", jeżeli tego nie robi, dodać gest palca w dół jak na videoie.',
    ytLink: 'https://www.youtube.com/watch?v=OnLbb8RimWg',
    video: siadVideo,
  },
  {
    name: 'Leżeć',
    command: 'Leżeć',
    description: 'Pies umie kłaść się na komendę, jeżeli tego nie robi, dodać poziomą dłoń.',
    ytLink: 'https://www.youtube.com/watch?v=kKxDjZ7rl0ns',
    video: lezecVideo,
  },
  {
    name: 'Łapa',
    command: 'Łapa + druga łapa',
    description:
      'Podstawiamy rękę pod jego łapę, gdy stoi/siedzi i wydajemy komendę "łapa", gdy poda, nagradzamy smaczkiem. Na zmianę z sekwencją "łapa + druga łapa" i dopiero wtedy dajemy smaczek.',
    ytLink: 'https://www.youtube.com/watch?v=v1VNhQSjqUY',
    video: lapaVideo,
  },
  {
    name: 'Proszenie o smakołyk',
    command: 'Proś',
    description:
      'Pies podskakuje na tę komendę i prosi, połowicznie umie na samą komendę, warto trenować z gestem, stopniowo go wycofując.',
    ytLink: 'https://www.youtube.com/watch?v=sIxGgXbz_kA&t=149s',
    video: prosVideo,
  },
  {
    name: 'Czekaj',
    command: 'Czekaj',
    description:
      'Pies siada i czeka na komendę "do mnie". Wydłużać czas czekania z każdym powtórzeniem. Warto powiedzieć komendę, odejść, wrócić do psa po jakimś czasie, nagrodzić go, wydać znowu komendę, odejść na jakiś czas i go zawołać, gdy przybiegnie, nagrodzić.',
    ytLink: 'https://www.youtube.com/watch?v=31CprFHWo78&t=139s',
    video: czekajVideo,
  },
  {
    name: 'Na miejsce',
    command: 'Na miejsce',
    description:
      'Należy palcem wskazać miejsce, na które ma iść pies, powinien się położyć i czekać na komendę "do mnie". Na początku nagradzać za samo pójście na swoje miejsce. Odejść na jakiś czas (na razie wytrzymuje do 1 min), wrócić i nagrodzić psa, potem znowu odejść i go zawołać wraz z nagrodą za przyjście.',
    ytLink: 'https://www.youtube.com/watch?v=StgN2DQuhao',
    video: '',
  },
  {
    name: 'Noga',
    command: 'Noga',
    description:
      'Pies po wydaniu tej komendy powinien chodzić przy prawej nodze, ważne, żeby nakierować go smaczkiem na dobrą nogę, jeżeli idzie po złej. Nagradzać co jakiś czas (np. 15 s czy 30 s) za chodzenie przy nodze. Tak samo na spacerze, gdy sam z siebie chodzi blisko, również nagrodzić.',
    ytLink: 'https://www.youtube.com/watch?v=Gd_rx9K8aW4&t=149s',
    video: nogaVideo,
  },
  {
    name: 'Środek',
    command: 'Środek',
    description:
      'Pies po tej komendzie i geście od tyłu wchodzi pomiędzy nogami i siada, patrząc na nas. Próbować również bez gestu.',
    ytLink: 'https://www.youtube.com/watch?v=XqpOum5r7OY&t=81s',
    video: srodekVideo,
  },
  {
    name: 'Slalom',
    command: 'Slalom',
    description:
      'Pies przechodzi pomiędzy nogami, pamiętać, żeby zacząć od dobrej nogi, od przeciwnej niż po której stoi pies. Nagradzać go po przejściu sekwencji 4 przejść.',
    ytLink: 'https://www.youtube.com/watch?v=S2Jox8tKOL4',
    video: slalomVideo,
  },
  {
    name: 'Zostaw',
    command: 'Zostaw',
    description:
      'Podczas zabawy z psem szarpakiem przestać szarpać i wydać komendę "zostaw", pies powinien się uspokoić i oddać zabawkę, po oddaniu zabawki bawić się z nim dalej tą samą zabawką. Powtarzać kilka razy przy zabawie.',
    ytLink: 'https://www.youtube.com/watch?v=9g9thndLB7A',
    video: '',
  },
  {
    name: 'Jedzenie',
    command: 'Jedzenie',
    description:
      'Komenda informująca psa, że zaraz dostanie jedzenie. Komendę powiedzieć przed nasypaniem do miski jedzenia. Pies po położeniu miski powinien czekać na komendę, jeżeli tego nie zrobi, zakryć jedzenie nogą i czekać, aż na nas spojrzy. Sprawdzać psa co jakiś czas, mówiąc różne słowa bardziej lub mniej zbliżone do słowa komendy.',
    ytLink: '',
    video: '',
  },
  {
    name: 'Nie',
    command: 'Nie',
    description:
      'Komenda informująca psa, że nie wolno mu robić czegoś. Duże pole do poprawy w tej komendzie, warto ją trenować w różnych sytuacjach i miejscach. Trenować jak na videoach.',
    ytLink: 'https://www.youtube.com/watch?v=SZ-CRwWSyJA',
    video: nieVideo,
  },
  {
    name: 'Ukłon',
    command: 'Ukłon',
    description:
      'Pies kłania się przednimi łapkami na tę komendę wraz z gestem. Stopniowo zmniejszać gest tak, aby na koniec wykonywał ją jedynie poprzez komendę.',
    ytLink: 'https://www.youtube.com/watch?v=OfzE-dJ4jAs',
    video: uklonVideo,
  },
  {
    name: 'Obrót',
    command: 'Obrót',
    description: 'Pies wykonuje tę komendę poprzez ruch ręką wokół niego.',
    ytLink: 'https://www.youtube.com/shorts/-j40M-wcdDI',
    video: obrotVideo,
  },
  {
    name: 'Pozwolenie',
    command: 'Proszę',
    description:
      'Kładziemy na ręce smaczek i czekamy, aż pies będzie na nas patrzył i nie będzie zainteresowany smaczkiem. Wydajemy komendę pozwolenia i dajemy mu smaczek. Tak samo ćwiczymy na zabawkach. Jeżeli próbuje zabrać smaczek lub chwycić zabawkę, zamykamy rękę lub oddalamy powoli od niego.',
    ytLink: '',
    video: proszeVideo,
  },
  {
    name: 'Spacer',
    command: 'Spacer',
    description:
      'Komenda "Czy", "chcesz", "iść", "na", "spacer" wykonana pojedynczymi słowami zachęca psa, żeby pójść na spacer. Przed samym wyjściem powtórzyć komendę "spacer". Przed założeniem obroży należy wydać komendę "siad" i dopiero wtedy założyć psu obrożę i z nim wyjść. Adekwatnie powrót.',
    ytLink: '',
    video: '',
  },
]

const newTricks = [
  {
    name: 'Skok przez rękę/przeszkodę',
    command: 'Hop',
    description: '',
    descriptionLink: 'https://johndog.pl/blog/wychowanie/skok-przez-przeszkode/',
    ytLink: 'https://www.youtube.com/watch?v=81MH7pe8mV0',
    video: '',
  },
  {
    name: 'Przynieś',
    command: 'Przynieś',
    description: '',
    ytLink:
      'https://www.youtube.com/watch?v=6Gpg4pS1FFc&list=PLJKV2_OdaYLUNSyL9Ex-aWQzU1LkLJJkl&index=15',
    video: '',
  },
]

const list = [
  'Codziennie powtarzać z psem komendy przez 10-15 min, 2-3 razy dziennie.',
  'WAŻNE!!! Po każdej prawidłowo wykonanej komendzie mówimy "SUPER", a następnie nagradzamy smaczkiem. Słowo "Super" powinno być wypowiedziane jak najszybciej po prawidłowym zachowaniu psa, żeby wiedział, za co został nagrodzony.',
  'Każdą komendę wykonać kilka razy pod rząd. Dać smaczka przy pierwszym i ostatnim wykonaniu, w środkowych powtórzeniach nie zawsze dawać — jeżeli idzie mu lepiej, nagradzać rzadziej.',
  'Komendy wykonywać w różnych miejscach i sytuacjach, żeby pies nie przyzwyczajał się do nich tylko w konkretnych warunkach.',
  'Podczas spacerów codziennie ćwiczyć komendy "do mnie", "noga" oraz "czekaj" i nagradzać go smaczkiem (warto brać mokre smaczki na spacery — wtedy lepiej słucha).',
  'Komendy wydawać raz wraz z gestem. Jeżeli nie wykona komendy, odejść na chwilę i spróbować ponownie.',
]
</script>

<template>
  <div class="container max-w-7xl px-4 py-10 mx-auto flex flex-col gap-4 md:gap-6">
    <h2 class="text-2xl font-bold text-center">Codzienna rutyna</h2>
    <ul class="list-disc list-inside">
      <li v-for="(text, index) in list" :key="index" class="mt-1" v-html="text" />
    </ul>
    <h2 class="text-lg font-bold text-center">Hades zna</h2>
    <AccordionTrick v-for="trick in tricks" :key="trick.name" v-bind="trick" />

    <h2 class="text-lg font-bold text-center mt-4">Hades chętnie pozna któreś z nich</h2>
    <AccordionTrick v-for="trick in newTricks" :key="trick.name" v-bind="trick" />
  </div>
</template>
