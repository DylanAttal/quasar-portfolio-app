<template>
  <q-layout view="hHh lpR fFf">
    <q-header bordered class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-btn
            label="DYLAN ATTAL"
            flat
            size="xl"
            :ripple="{ center: true }"
          />
        </q-toolbar-title>

        <q-tabs>
          <q-tab label="Portfolio" :ripple="{ center: true }" />
          <q-tab label="Resume" :ripple="{ center: true }" />
          <q-tab label="About" :ripple="{ center: true }" />
          <q-tab label="Contact" :ripple="{ center: true }" />
        </q-tabs>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",

  components: {},

  data() {
    return {};
  }
};
</script>
