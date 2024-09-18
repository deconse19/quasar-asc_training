<template>
  <q-layout class="bg-primary" view="lHh Lpr lFf">
    <q-header>
      <q-toolbar class="bg-secondary text-center text-grey">
        <q-toolbar-title>
          Hello my name is Demoooo
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-img
      src="bg.jpg"
      class="fit absolute"
    />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
