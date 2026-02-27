<script setup lang="ts">
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from '@/components/ui/accordion'

defineProps<{
  name: string
  command: string
  description?: string
  ytLink?: string
  descriptionLink?: string
  video?: string
}>()
</script>

<template>
  <Accordion type="single" collapsible class="w-full">
    <AccordionItem value="item-1">
      <AccordionTrigger>
        <span class="font-bold cursor-pointer">{{ name }}</span>
      </AccordionTrigger>
      <AccordionContent>
        <div class="flex flex-col gap-1">
          <p class="mb-2">
            Komenda: <span class="font-bold">{{ command }}</span>
          </p>
          <p v-if="description" class="mb-2">Opis: {{ description }}</p>
          <a v-if="ytLink" :href="ytLink" target="_blank" class="text-blue-500 underline">
            Link do filmu na YouTube
          </a>
          <a
            v-if="descriptionLink"
            :href="descriptionLink"
            target="_blank"
            class="text-blue-500 underline"
          >
            Link do opisu sztuczki
          </a>

          <video v-if="video" height="500" class="!h-125" controls>
            <source :src="video" type="video/mp4" />
          </video>
        </div>
      </AccordionContent>
    </AccordionItem>
  </Accordion>
</template>
