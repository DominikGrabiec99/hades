<script setup lang="ts">
import AccordionTrick from './AccordionTrick.vue'

const tricks = [
  {
    name: 'Skupienie uwagi',
    command: '-',
    description:
      'Wyciągamy smaczka w bok, pies powinien wtedy spojrzeć na nas następnie nagradzmay go smaczkiem',
    ytLink: 'https://www.youtube.com/watch?v=K1EWibyPqqU&t=1s',
    film: '',
  },
  {
    name: 'Do mnie',
    command: 'Do mnie',
    description:
      'Wołamy "Do mnie", jeżeli przybiega dajemy mu smaczek i chwalimy go. Warto robić w różnych odlegościach i wołać go jak nie jest na nas sfokusowany.',
    ytLink: 'https://www.youtube.com/watch?v=lDCmeGN9sgg&t=1s',
    film: '',
  },
  {
    name: 'Siad',
    command: 'Siad',
    description:
      'Pies powinien wykonać komendę na samo słowo siad, jeżeli tego nie robi dodać gest palca w dół jak na filmie.',
    ytLink: 'https://www.youtube.com/watch?v=OnLbb8RimWg',
    film: '',
  },
  {
    name: 'Leżeć',
    command: 'Leżeć',
    description: 'Pies umie kłaść się na komende, jeżei tego nie robi dodać - pozioma dłoń.',
    ytLink: 'https://www.youtube.com/watch?v=kKxDjZ7rl0ns',
    film: '',
  },
  {
    name: 'Łapa',
    command: 'Łapa + druga łapa',
    description:
      'Podstawiamy rękę pod jego łapę jak stoi/siedzi i wydajemy komendę łapa jak poda nagradzamy smaczkiem, na zmianę z sekwensją łapa + druga łapa i dopiero wtedy dajemy smaczek.',
    ytLink: 'https://www.youtube.com/watch?v=v1VNhQSjqUY',
    film: '',
  },
  {
    name: 'Proszenie o smakołyk',
    command: 'Proś',
    description:
      'Pies podskakuje na tą komenddę i prosi, połowicznie umie na samą komende warto trenować z gestem stopniowo go wycofując.',
    ytLink: 'https://www.youtube.com/watch?v=sIxGgXbz_kA&t=149s',
    film: '',
  },
  {
    name: 'Czekaj',
    command: 'Czekaj',
    description:
      'Pies siada i czeka na komędę do mnie. Wydłużać czas czekania z każdym powtórzeniem. Warto powiedzieć komendę, odejść wrócić do psa po x czasu nagrodzić go wydać znowu komendę odejśc na jakiś czas i go zawołać, jak przybiegnie nagrodzić.',
    ytLink: 'https://www.youtube.com/watch?v=31CprFHWo78&t=139s',
    film: '',
  },
  {
    name: 'Na miejsce',
    command: 'Na miejsce',
    description:
      'Należy palcem wskazać miejsce na którę ma iśc pies, powinien się położyć i czekać na komendę do mnie. Na początku nagradzać za samo pojście na swoje miejsce. Odejśc na jakiś czas (na razie wytrzymuje do 1 min), wrócić i nagrodzić psa potem znowu odejśc i go zawołać wraz z nagrodą za przyjście.',
    ytLink: 'https://www.youtube.com/watch?v=StgN2DQuhao',
    film: '',
  },
  {
    name: 'Noga',
    command: 'Noga',
    description:
      'Pies po wydaniu tej komendy powiinien chodzić przy prawej nodze, ważne żeby nakierować go smaczkiem na dobrą nogę jeżeli idzie po złej. Nagradzać co jakiś czas (np: 15s czy 30s) za chodzenie przy nodze. Tak samno na spacerze jak sam z siebie chodzi blisko również nagrodzić.',
    ytLink: 'https://www.youtube.com/watch?v=Gd_rx9K8aW4&t=149s',
    film: '',
  },
  {
    name: 'Środek',
    command: 'Środek',
    description:
      'Pies po tej komendzie i geście od tyłu wchodzi pomiędzy nogami i siada patrząc na nas. Próbować również bez gestu.',
    ytLink: 'https://www.youtube.com/watch?v=XqpOum5r7OY&t=81s',
    film: '',
  },
  {
    name: 'Slalom',
    command: 'Slalom',
    description:
      'Pies przechodzi pomiędzy nogami, pamiętać żeby zacząć od dobrej nogi, od przeciwnej niż po której stoi pies. Nagradzać go po przejściu sekwencji 4 przejść.',
    ytLink: 'https://www.youtube.com/watch?v=S2Jox8tKOL4',
    film: '',
  },
  {
    name: 'Zostaw',
    command: 'Zostaw',
    description:
      'Podczas zabawy z psem szarpakiem  przestać szarpać i wydać komendę zostaw pies powinien się uspokoić i oddać zabawkę, po oddaniu zabawki bawić się z nim dalej tą samą zabawką. Powtarzać kilka razy przy zabawie.',
    ytLink: 'https://www.youtube.com/watch?v=9g9thndLB7A',
    film: '',
  },
  {
    name: 'Jedzenie',
    command: 'Jedzenie',
    description:
      'Komenda informująca psa, że zaraz dostanie jedzienie. Komende powiedzieć przed nasypaniem do miski jedzenia. Pies po położeniu miski powinienn czekać na komędę jeżlei tego nie zrobi zakryć jedzenie nogą i czekać aż na nas spoojrzy. Sprawdzać psa co jakiś czas mówiąć rożne słowa bardziej lub mniej zbliżone do słowa komendy.',
    ytLink: '',
    film: '',
  },
  {
    name: 'Nie',
    command: 'Nie',
    description:
      'Komenda informująca psa, że nie wolno mu robić czegoś. Duże pole do poprawy w tej komendzie, warto ją trenować w różnych sytuacjach i miejscach. Trenować jak na filmach.',
    ytLink: 'https://www.youtube.com/watch?v=SZ-CRwWSyJA',
    film: '',
  },
  {
    name: 'Ukłon',
    command: 'Ukłon',
    description:
      'Pies klania sie przednimi łapkami na tą komędę wraz z gestem. Stopniowo zmiejszać gest tak aby na koniec wykjonywał ją jedynie poprzez komende.',
    ytLink: 'https://www.youtube.com/watch?v=OfzE-dJ4jAs',
    film: '',
  },
  {
    name: 'Obrót',
    command: 'Obrót',
    description: 'Pies wykonuje tą komendę poprzez ruch ręką w okół niego.',
    ytLink: 'https://www.youtube.com/shorts/-j40M-wcdDI',
    film: '',
  },
  {
    name: 'Pozwolenie',
    command: 'Proszę',
    description:
      'Kładziemy na ręku smaczka i czekamy aż pies będzie na nas patrzył i nie będzie zainteresowany smaczkiem. Wydajemy komędę pozwolenia i dajemy mu smaczka. Tak samo ćwiczymy na zabawkach. Jeżeli próbuje zabrać smaczka lub chwycić zabawkę zamykamy rękę lub oddalamy powoli od niego.',
    ytLink: '',
    film: '',
  },
  {
    name: 'Spacer',
    command: 'Spacer',
    description:
      'Komenda "Czy" "chcesz" "iść" "na" "spacer" wykonana pojedyńczymy słowami zachęca psa żeby pójśc na spacer. Przed samym wyjściem powtórzyć komendę "spacer". Przed założeniem obroży należy wydać komendę siad i dopiero wtedy założyć psu obrożę i z nim wyjść. Adekwatnie powrót.',
    ytLink: '',
    film: '',
  },
]

const newTricks = [
  {
    name: 'Skok przez rękę/przeskodę',
    command: 'Hop',
    description: '',
    descriptionLink: 'https://johndog.pl/blog/wychowanie/skok-przez-przeszkode/',
    ytLink: 'https://www.youtube.com/watch?v=81MH7pe8mV0',
    film: '',
  },
  {
    name: 'Przynieś',
    command: 'Przynieś',
    description: '',
    ytLink:
      'https://www.youtube.com/watch?v=6Gpg4pS1FFc&list=PLJKV2_OdaYLUNSyL9Ex-aWQzU1LkLJJkl&index=15',
    film: '',
  },
]

const list = [
  'Codzinnie powtarzać z psem komendy przez 10 - 15 min 2/3 razy dziennie.',
  'WAŻNE!!! Po każdej prawidłowo wykonanej komendzie mówimy "SUPER" a następnie nagardzamy smaczkiem. Słowo "Super" powinno być wypowiedziane jak najszybciej po prawidłowym zachowaniu psa, żeby wiedział za co został nagrodzony.',
  'Każdą komendę wykonać kilka razy po sobie dać smaczka przy piewrwszym wykonaniu oraz ostanim w środkowcyh powtórzeniach nie zawsze dawać jeżlei idzie my lepiej dawać żadziej.',
  'Komendy wykonywać w różnych miejscach i sytuacjach żeby pies się nie przyzwyczajał do nich tylko w konkretnych warunkach.',
  'Podczas spacerów codzieennie ćwiczyć komende do mnie, noga oraz czekaj i nagradzać go smaczkiem (warto brać mokre smaczki na spacery wtedy lepiej słucha).',
  'Komendy wydawać raz wraz z gestem, jeżeli nie wykona komendy odejść na chwilę i spróbować ponownie.',
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
    <h2 class="text-lg font-bold text-center">Hades chętnie pozna któreś z nich</h2>
    <AccordionTrick v-for="trick in newTricks" :key="trick.name" v-bind="trick" />
  </div>
</template>
