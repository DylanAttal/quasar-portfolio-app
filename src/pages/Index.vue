<template>
  <q-page class="flex flex-center">
    <section
      id="top"
      class="column justify-center items-center full-width bg-teal-4"
    >
      <img
        src="../assets/prof-cropped.jpeg"
        class="profile-picture q-mb-xl"
        alt="A picture of Dylan's face smiling."
      />
      <p class="text-h2 text-white text-weight-bolder">DYLAN ATTAL</p>
      <p class="text-h3 text-white text-weight-bold">
        Full Stack Software Engineer
      </p>
    </section>
    <section id="portfolio">
      <h2 class="text-center">Portfolio</h2>
      <div class="q-pa-md row items-start q-gutter-md">
        <q-card class="my-card">
          <img src="../assets/hitch-gif.gif" class="portfolio-picture" />

          <q-card-section>
            <div class="text-h6">Hitch</div>
            <div class="text-subtitle2">
              Full stack app with React, Rails, and Auth0
            </div>
          </q-card-section>
        </q-card>
      </div>
    </section>
    <section id="resume" class="bg-teal-4">
      <h2>resume</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta
        excepturi, illum nesciunt accusamus qui sunt nam voluptate cum doloribus
        consequatur rerum animi consectetur inventore veniam alias labore
        quaerat aperiam nostrum!
      </p>
    </section>
    <section id="about">
      <h2>about</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta
        excepturi, illum nesciunt accusamus qui sunt nam voluptate cum doloribus
        consequatur rerum animi consectetur inventore veniam alias labore
        quaerat aperiam nostrum!
      </p>
    </section>
    <section id="contact" class="bg-teal-4">
      <h2>contact</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta
        excepturi, illum nesciunt accusamus qui sunt nam voluptate cum doloribus
        consequatur rerum animi consectetur inventore veniam alias labore
        quaerat aperiam nostrum!
      </p>
    </section>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex"
};
</script>

<style lang="scss" scoped>
section {
  min-height: calc(100vh - 62px);
}

.profile-picture {
  height: 300px;
  width: 280px;
  border-radius: 200px;
}

.portfolio-picture {
  height: 250px;
  width: auto;
}
</style>
