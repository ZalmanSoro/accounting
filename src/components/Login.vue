<template>
  <v-dialog v-model="dialog" max-width="300">
    <v-card class="text-center hebrew">
      <v-card-title >
        <v-col >פתח חשבון</v-col>
      </v-card-title>
      <v-card-text>
        <div
          class="mb-2"
          v-for="({ img, text }, index) in providers"
          :key="index"
        >
          <v-btn dense outlined large color="primary" dark min-width="250">
            <span> <b> {{ text }} </b> </span>
            <v-spacer></v-spacer>
            <img :src="img" />
          </v-btn>
        </div>
        <v-divider></v-divider>
        <span>או</span>
        <v-text-field
          label="התחבר באמצעות מייל"
          outlined
          dense
          min-width="250"
        ></v-text-field>
        <v-btn dense large color="primary" dark min-width="250">
          <span>הרשם</span>
        </v-btn>
      </v-card-text>

      <!-- <v-card-title>הרשמה</v-card-title>

      <v-card-text> </v-card-text>
      <v-divider />
      <v-col class="text-center">
      <span>התחבר באמצצעות</span>
      </v-col>
      <v-card-actions class="text-center">
        <v-col>
          <v-btn outlined rounded @click="dialog = false">
            <img
              src="https://img.icons8.com/fluent/30/000000/google-logo.png"
            />
          </v-btn>
        </v-col>
        <v-col>
          <v-btn rounded outlined @click="dialog = false">
            <img
              src="https://img.icons8.com/color/30/000000/facebook-new.png"
            />
          </v-btn>
        </v-col>
      </v-card-actions> -->
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: ["dialog"],
  data: () => ({
    providers: [
      {
        text: "התחבר עם גוגל",
        img: "https://img.icons8.com/fluent/30/000000/google-logo.png",
      },
      {
        text: "התחבר עם פייסבוק",
        img: "https://img.icons8.com/color/30/000000/facebook-new.png",
      },
      {
        text: "התחבר עם אפל",
        img: "https://img.icons8.com/ios-filled/30/000000/mac-os.png",
      },
    ],
  }),
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@300&display=swap');
.hebrew {
    font-family: 'Rubik', sans-serif;
}
</style>