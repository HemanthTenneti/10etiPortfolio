<script setup lang="ts">
// const route = useRoute();
const currentUTCDate = new Date();
const istTimeInMilliseconds = currentUTCDate.getTime();

const istDateTime = new Date(istTimeInMilliseconds);

const options: Intl.DateTimeFormatOptions = {
  hour: "2-digit",
  minute: "2-digit",
  hour12: false,
};

const istFormattedDateTime = istDateTime.toLocaleString("en-IN", options);
</script>

<template>
  <main>
    <div class="flex justify-center items-center w-screen h-screen">
      <h1
        class="bg-gradient-to-b from-[#2F2F2F] to-[#101012] bg-clip-text text-transparent font-bold text-[150px] lg:text-[600px]"
      >
        {{ istFormattedDateTime }}
      </h1>
    </div>
  </main>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&display=swap");
* {
  font-family: "Space Grotesk";
}
</style>
