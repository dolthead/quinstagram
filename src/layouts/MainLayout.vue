<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">
        <q-btn
          to="/"
          icon="eva-home-outline"
          class="large-screen-only"
          size="18px"
          flat
          round
          dense
        ></q-btn>
        <q-separator vertical spaced class="large-screen-only" />
        <q-toolbar-title> Quinstagram </q-toolbar-title>
        <q-btn
          to="/about"
          icon="eva-info-outline"
          class="large-screen-only"
          size="18px"
          flat
          round
          dense
        ></q-btn>
      </q-toolbar>
    </q-header>

    <q-footer bordered class="bg-white small-screen-only">
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab to="/" icon="eva-home-outline" />
        <q-route-tab to="/about" icon="eva-info-outline" />
      </q-tabs>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts"></script>

<style lang="scss">
  .q-toolbar {
    @media (min-width: $breakpoint-sm-min) {
      height: 76px;
    }
  }
  .q-footer .q-tab__icon {
    font-size: 32px;
  }
  .q-header .q-toolbar__title {
    font-family: 'Grand Hotel', cursive;
    font-size: 32px;
    @media (max-width: $breakpoint-xs-max) {
      text-align: center;
    }
  }
</style>
