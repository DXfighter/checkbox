<template>
  <fieldset class="flex flex-col">
    <legend class="font-semibold">ToDos</legend>
    <div class="mt-4">
      <div
        v-for="(person, personIdx) in people"
        :key="personIdx"
        class="text py-0"
      >
        <input
          :id="`person-${person.id}`"
          :info="`person-${person.id}`"
          type="checkbox"
          class="h-4 w-4 mr-1"
        />
        <label :for="`person-${person.id}`" class="select-none">{{
          person.info
        }}</label>
      </div>
    </div>
  </fieldset>
</template>

<script setup>
const people = [
  { id: 1, info: 'Email' },
  { id: 2, info: 'Call' },
  { id: 3, info: 'Orga Meeting' },
  { id: 4, info: 'Newsletter' },
];
</script>

<style scoped>
fieldset {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  align-self: stretch;
}

fieldset text {
  color: #000;
  font-family: 'Noto Sans';
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

fieldset legend {
  display: flex;
  color: #000;
  font-family: 'Noto Sans', sans-serif;
  font-size: 12px;
  font-style: normal;
  font-weight: 900;
  line-height: normal;
  position: fixed;
}
</style>
