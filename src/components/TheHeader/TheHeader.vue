<script lang="ts" setup>
import GtLogo from "~/assets/images/nkgt-2025-logo.svg?component";
import NorthernKingsLogo from "~/assets/images/nk-logo-vertical.svg?component";
// import UkCokLogo from "~/assets/images/uk-cok-logo.svg?component";
import VButton from "~/components/VButton";

defineProps({
  compact: Boolean,
});
</script>

<template>
  <header :class="['c-header', compact && 'c-header--compact']">
    <div class="c-header__presents">
      <span class="c-header__presents-label">The</span>
      <a href="https://thenorthernkings.com/">
        <NorthernKingsLogo class="c-header__presents-logo" />
      </a>
      <span class="c-header__presents-label">Present</span>
    </div>
    <div class="c-header__main">
      <template v-if="compact">
        <div class="c-header__logo c-header__logo--compact">
          <a href="/">
            <GtLogo class="c-header__logo__image" />
          </a>
        </div>
      </template>
      <template v-else>
        <div class="c-header__logo">
          <GtLogo class="c-header__logo__image" />
        </div>
        <p class="c-header__date">
          Ossett, West Yorkshire. <span>June 21<sup>st</sup> and 22<sup>nd</sup> </span>
        </p>
        <!-- <p class="c-header__strapline u-text-uppercase">
          <UkCokLogo class="c-header__cok" />
          Regional Qualifier
        </p> -->
        <!-- <p class="c-header__strapline u-text-uppercase">Sorry, the event has now sold out</p> -->
      </template>
    </div>
    <div class="c-header__book-now">
      <VButton
        class="c-header__book-now__action"
        href="/register"
        :variants="['sm', 'lg:lg', 'decorative', 'ghost', 'invert']"
      >
        Register Now
      </VButton>
      <!-- <VButton disabled :variants="['sm', 'lg:lg', 'decorative', 'ghost', 'invert']">
        Sold Out
      </VButton> -->
    </div>
  </header>
</template>

<style src="./TheHeader.css"></style>
