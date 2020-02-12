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
        <q-card class="my-card cursor-pointer" @click="showHitchDialog = true">
          <img src="../assets/hitch-gif.gif" class="portfolio-picture" />

          <q-card-section>
            <div class="text-h6">Hitch</div>
            <div class="text-subtitle2">
              Full stack app with React, Rails, and Auth0
            </div>
          </q-card-section>
        </q-card>

        <q-dialog v-model="showHitchDialog">
          <q-card>
            <q-card-section>
              <div class="text-h4">Hitch</div>
            </q-card-section>

            <q-card-section class="q-pt-none column">
              <img
                src="../assets/hitch-gif.gif"
                class="dialog-picture q-mb-md"
              />
              <p class="text-h6">See it live</p>
              <p>https://hitch-app.herokuapp.com/</p>

              <p class="text-h6">Summary</p>
              <p>
                Hitch is a prototype for a peer-to-peer long-distance rideshare
                app built with a React front-end and Rails back-end. The idea
                behind the app is that traveling between cities in the United
                States is hard for someone who does not own a vehicle. Public
                transportation is lacking. Renting a car is expensive. I saw a
                gap in the market for intercity travel, and I think peer-to-peer
                rideshares can address it. Drivers on Hitch can afford to charge
                a low price per seat because they're already headed in that
                direction anyway; think of it as a friend covering your gas
                money. It's hitchhiking for the 21st century!
              </p>
              <p>
                The current prototype offers several core features: searching
                for a ride, booking a ride, offering a drive, displaying your
                rides and drives, and canceling your rides and drives. Users can
                search for rides based upon departure and arrival locations,
                dates, and times, as well as number of seats available in the
                vehicle and the price per seat.
              </p>
              <p>
                I utilized Auth0 for user authentication, and offered the
                ability for users to sign up and log in with their Google
                accounts. Hitch takes and stores the users' Google profile
                pictures, full names, and email addresses, displaying that
                information automatically on their profile pages. Users can then
                add more information to their profiles.
              </p>
              <p>
                I used Ruby ORMs to build an API with a postgresQL database.
                Instead of scaffolding, I wrote original models, controllers,
                and routes to manipulate user-generated data. My data is
                represented by three tables: People, Trips, and Rides (a
                junction table establishing the passengers for each trip).
              </p>
              <p>
                I imported the library react-map-gl in order to let users choose
                departure and arrival locations by simply dropping a pin on a
                map. I stored the latitude and longitude of those pins in state,
                and then passed that information to my back-end through a POST
                request tied to a form submission. Then the latitudes and
                longitudes were reverse-geocoded into an address by a custom
                method which I wrote for the Geocoder gem.
              </p>

              <p class="text-h6">Technologies used</p>
              <p>
                HTML, CSS, Javascript, React, React Router, React-Map-GL, Axios,
                Moment.js, Auth0, Ruby, Rails, Geocoder
              </p>
            </q-card-section>

            <q-card-actions align="right">
              <q-btn flat label="OK" color="primary" v-close-popup />
            </q-card-actions>
          </q-card>
        </q-dialog>
      </div>
    </section>
    <section
      id="resume"
      class="bg-teal-4 column justify-center items-center full-width"
    >
      <h2 class="text-center">Resume</h2>
      <img
        src="../../src/assets/DylanAttalResume.jpg"
        class="resume-picture q-mb-xl"
      />
    </section>
    <section id="about" class="column justify-center items-center full-width">
      <h2>About Me</h2>
      <div class="row justify-center items-center">
        <div class="col-md-5 q-ml-lg q-mr-lg">
          <p class="text-h5">
            Self-motivated full stack web developer with a proven track record
            of learning and implementing new technologies. Passionate about
            writing clean code and leveraging strengths of diverse teams. I have
            an entrepreneurial spirit paired with a relentless work ethic. I am
            a skilled communicator with excellent interpersonal and
            problem-solving skills.
          </p>
        </div>
        <div class="col-md-5 q-ml-lg q-mr-lg">
          <p class="text-h5">
            Tampa native with a passion for home-cooked meals and freshly-ground
            coffee. I believe that natural springs are Florida's best-kept
            secret; on the weekends you can find me on Rainbow River or St. Pete
            beach. As a card-carrying nerd, I enjoy reading non-fiction and
            watching anime, and my lifelong dream is to vacation in Japan during
            the spring to see the cherry blossoms in full bloom.
          </p>
        </div>
      </div>
    </section>
    <section
      id="contact"
      class="column justify-center items-center full-width bg-teal-4"
    >
      <h2>Contact Me</h2>
      <div class="row justify-center items-center full-width full-height">
        <div class="q-col-md-4">
          <a href="mailto:attal.dylan@gmail.com" target="_blank"
            ><q-icon :name="fasEnvelope" class="contact-icon q-ml-md q-mr-md"
          /></a>
        </div>

        <div class="q-col-md-4">
          <a href="https://www.linkedin.com/in/dylanattal/" target="_blank"
            ><q-icon :name="fabLinkedinIn" class="contact-icon q-ml-md q-mr-md"
          /></a>
        </div>

        <div class="q-col-md-4">
          <a href="https://github.com/DylanAttal" target="_blank"
            ><q-icon
              :name="fabGithubSquare"
              class="contact-icon q-ml-md q-mr-md"
          /></a>
        </div>

        <div class="q-col-md-4">
          <a href="https://medium.com/@DylanAttal" target="_blank"
            ><q-icon :name="fabMedium" class="contact-icon q-ml-md q-mr-md"
          /></a>
        </div>
      </div>
    </section>
  </q-page>
</template>

<script>
import { fasEnvelope } from "@quasar/extras/fontawesome-v5";
import { fabLinkedinIn } from "@quasar/extras/fontawesome-v5";
import { fabGithubSquare } from "@quasar/extras/fontawesome-v5";
import { fabMedium } from "@quasar/extras/fontawesome-v5";

export default {
  name: "PageIndex",
  data() {
    return {
      showHitchDialog: false,
      fasEnvelope: fasEnvelope,
      fabLinkedinIn: fabLinkedinIn,
      fabGithubSquare: fabGithubSquare,
      fabMedium: fabMedium
    };
  }
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

.dialog-picture {
  max-height: 350px;
  width: auto;
}

.resume-picture {
  max-height: 700px;
  width: auto;
}

a {
  color: #000;
  text-decoration: none;

  &:visited {
    color: #000;
  }
}

.contact-icon {
  height: 50px;
  width: auto;
}
</style>
