<template>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/profile">Profile</nuxt-link>
      </li>
      <li v-if="$auth.loggedIn">
        <a href="/logout" @click.prevent="$auth.logout()">Log out</a>
      </li>
      <li v-else>
        <nuxt-link to="/login">Log in</nuxt-link>
      </li>
    </ul>
</template>