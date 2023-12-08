<template>
  <v-container class="fill-height">
    <v-responsive class="align-center text-center fill-height">
      <!-- <v-img height="300" src="@/assets/logo.svg" /> -->

      <div class="text-body-2 font-weight-light mb-n1">Let's learn</div>

      <h1 class="text-h2 font-weight-bold">Japanese!</h1>

      <div class="py-14" />

      <v-row class="d-flex align-center justify-center">
        <v-col cols="auto">
          <v-btn
            href="#"
            min-width="164"
            rel="noopener noreferrer"
            variant="text"
          >
            <v-icon
              icon="mdi-view-dashboard"
              size="large"
              start
            />

            How it works
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <router-link to="/quiz">
            <v-btn
              color="primary"
              min-width="228"
              rel="noopener noreferrer"
              size="x-large"
              variant="flat"
            >
              <v-icon
                icon="mdi-speedometer"
                size="large"
                start
              />

              Get Started
            </v-btn>
          </router-link>
        </v-col>

        <v-col cols="auto">
          <v-btn
            href="#"
            min-width="164"
            rel="noopener noreferrer"
            variant="text"
          >
            <v-icon
              icon="mdi-account-group"
              size="large"
              start
            />

            Community
          </v-btn>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script lang="ts" setup>
  //
</script>
