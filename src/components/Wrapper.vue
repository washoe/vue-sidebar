<template>
  <div class="wrapper with-sidebar">
    <div>
      <Sidebar />
      <Main />
    </div>
  </div>
</template>

<script>
import Sidebar from "./Sidebar";
import Main from "./Main";
export default {
  components: { Sidebar, Main }
};
</script>

<style>
.wrapper {
  background-color: thistle;
}
.with-sidebar > * {
  display: flex;
  flex-wrap: wrap;
  margin: -0.5rem;
}

.with-sidebar > * > * {
  /* ↓ applies to both elements */
  margin: 0.5rem;
}

/* Prefers 20rem width, but will grow as space permits. Thus 20rem is the effective minimum width */
.sidebar {
  flex-basis: 20rem;
  flex-grow: 1;
}

.not-sidebar {
  /* ↓ grow from nothing - this keeps it from being pushed below the sidebar */
  flex-basis: 0;
  /* A really big number - keeps the sidebar to its minimum width when they are adjacent */
  flex-grow: 999;
  /* Determines when the layout will break out onto a second line - before the main content becomes narrower than the sidebar. We remove 1rem to compensate for the 0.5rem margin. */
  min-width: calc(50% - 1rem);
}
</style>
