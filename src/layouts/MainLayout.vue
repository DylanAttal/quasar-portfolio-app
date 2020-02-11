<template>
  <q-layout view="hHh lpR fFf">
    <q-header bordered class="bg-blue-grey-10 text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-btn
            label="DYLAN ATTAL"
            flat
            size="xl"
            :ripple="{ center: true }"
            @click="scrollTo('top')"
          />
        </q-toolbar-title>

        <q-tabs>
          <q-tab
            @click="scrollTo('portfolio')"
            label="Portfolio"
            :ripple="{ center: true }"
          />
          <q-tab
            @click="scrollTo('resume')"
            label="Resume"
            :ripple="{ center: true }"
          />
          <q-tab
            @click="scrollTo('about')"
            label="About"
            :ripple="{ center: true }"
          />
          <q-tab
            @click="scrollTo('contact')"
            label="Contact"
            :ripple="{ center: true }"
          />
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
  },

  methods: {
    scrollTo(id) {
      document
        .getElementById(id)
        .scrollIntoView({ block: "end", behavior: "smooth" });
    }
  }
};
</script>
