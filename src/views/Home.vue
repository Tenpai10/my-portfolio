<template>
  <v-app id="app">
    <v-app-bar app color="white" elevate-on-scroll>
      <v-tabs centered class="ml-n9" color="grey darken-1">
        <v-tab v-for="link in links" :key="link">
          {{ link }}
        </v-tab>
      </v-tabs>
    </v-app-bar>

    <v-main class="white">
      <v-container>
        <v-row>
          <v-col cols="12" sm="2"> </v-col>

          <v-col cols="12" sm="8">
            <v-sheet class="transparent mt-8" min-height="20vh" rounded="lg">
              <h1 class="text-justify mb-8">
                Hello! I’m Franz Arvae Ignacio a product designer and graphics
                artist based in the Philippines. I specialise in designing and
                developing websites and mobile applications.
              </h1>
              <v-divider class="black"></v-divider>
              <h1 class="mt-4" style="font-size: 3rem">Projects & Designs</h1>
              <div class="my-8" v-for="item in 4" v-bind:key="item">
                <v-card class="" max-width="100%" outline>
                  <v-row>
                    <v-col class="pa-12" cols="6">
                      <v-card-subtitle class=""> UI/UX Design </v-card-subtitle>
                      <v-card-title
                        style="font-size: 2rem"
                        class="font-weight-black mt-n6 text-md-left"
                        >PROJECT TITLE
                      </v-card-title>
                      <v-card-text class="text--primary">
                        <p>
                          Lorem ipsum dolor sit amet, consectetur adipiscing
                          elit, sed do eiusmod tempor incididunt ut labore et
                          dolore magna aliqua. Ut enim ad minim veniam
                        </p>
                      </v-card-text>
                      <v-card-actions>
                        <v-btn color="black" text> Visit </v-btn>
                        <v-btn color="black" text> Explore </v-btn>
                      </v-card-actions>
                    </v-col>
                    <v-col cols="6" class="pa-0">
                      <v-img
                        position="center"
                        height="100%"
                        width="98%"
                        src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
                        gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
                      ></v-img>
                    </v-col>
                  </v-row>
                </v-card>
              </div>

              <div>
                <h1 class="mt-16" style="font-size: 3rem">
                  Traditional & Graphic Artworks
                </h1>
                <v-carousel
                  cycle
                  :interval="8000"
                  hide-delimiters
                  show-arrows-on-hover
                  v-model="model"
                >
                  <v-carousel-item v-for="(color, i) in colors" :key="color">
                    <v-sheet :color="color" height="100%" tile>
                      <v-row
                        class="fill-height"
                        align="center"
                        justify="center"
                      >
                        <div class="text-h2">Slide {{ i + 1 }}</div>
                      </v-row>
                    </v-sheet>
                  </v-carousel-item>
                </v-carousel>
              </div>

              <div class="mt-16">
                <v-row>
                  <v-col cols="6">
                    <h1 style="font-size: 3rem">Let's Work together!</h1>
                    <h2 class="mt=4 text-decoration-underline">
                      franz_webdev@gmail.com
                    </h2>
                  </v-col>
                  <v-col cols="6" align="center">
                    <v-btn
                      outlined
                      raised
                      rounded
                      x-large
                      height="6em"
                      width="16em"
                    >
                      <h2>Hire Me!</h2></v-btn
                    >
                  </v-col>
                </v-row>
              </div>

              <div class="my-20"></div>
            </v-sheet>
          </v-col>

          <v-col cols="12" sm="2"> </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    links: ["About me", "Contacts"],
    model: 0,
    colors: [
      "grey",
      "grey darken-2",
      "grey",
      "grey darken-2",
      "grey",
      "grey darken-2",
    ],
  }),
};
</script>
