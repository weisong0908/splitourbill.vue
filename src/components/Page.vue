<template>
  <section class="section">
    <b-message title="Warning" type="is-warning" has-icon
      >This page is under development</b-message
    >
    <div class="tile is-vertical is-ancestor">
      <div class="tile is-parent">
        <div class="tile is-child">
          <p class="title">{{ title }}</p>
          <p class="subtitle">{{ subtitle }}</p>
        </div>
      </div>
      <div class="tile is-parent">
        <div class="tile is-child">
          <slot></slot>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import pageMixin from "../mixins/page";

export default {
  props: ["title", "subtitle"],
  mixins: [pageMixin],
  data() {
    return {
      friendRequests: []
    };
  }
};
</script>
