<script setup>
console.log('CLIENT LOG');

const requestFromAPI = async () => {
  console.log('EXECUTE API REQUEST');

  const apiResult = await useFetch('/api/test');

  console.log(apiResult?.data?.value);
};
</script>

<template>
  <div>
    <button @click="requestFromAPI">
      EXECUTE API REQUEST
    </button>

    <NuxtWelcome />
  </div>
</template>

<style>
button {
  padding: 24px 32px;
  background-color: green;
  color: white;
  font-weight: bold;
  cursor: pointer;
}
</style>
