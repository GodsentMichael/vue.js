<template>
  <div class="text-black border space-y-4  w-15 p-6 flex flex-col mb-4 justify-center items-center">
    <header>
      <slot name="header">Default data</slot>
    </header>

    <main>
      <slot name="main">Default data</slot>
    </main>

    <footer>
      <slot name="footer"> Default data</slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Child",
};
</script>
