<template>
  <main class="home">
    <section class="left">
      <div class="container">
        <h1 class="title">Let's get together in an online meetup with devs!</h1>
        <div class="intro">
          <h2 class="when">What:</h2>
          <p>WebDevs Unite is hosting a virtual event where developers can meet each other and casually talk about their interests.</p>

          <h2 class="where">Where:</h2>
          <p>
            The event will be held on Jitsi Meet, a
            <abbr title="free and open source">FOSS</abbr>,
            <abbr title="end-to-end encrypted">E2EE</abbr> video conferencing platform usable with any modern web browser, and on Android or iOS devices.
          </p>

          <h2>When:</h2>
          <p>
            On 2's day &ndash;
            <time datetime="2022-02-22T22:22Z">22 February 2022 at 22:22 UTC</time>
            &ndash;
            <NuxtLink to="/WebDevsUnite-Invite.ics" no-prefetch>let's add this to your calendar.</NuxtLink>
          </p>
        </div>

        <div class="callToAction">
          <div class="before-button">
            <span>
              See you on
              <time
                datetime="2022-02-22T22:22Z"
                title="Tuesday, 22nd of February, 2022"
              >2's day!</time>
            </span>
          </div>
          <div class="buttons">
            <CTAButton class="cta-button" link="/WebDevsUnite-Invite.ics">Save the date</CTAButton>
            <!-- <CTAButton class="cta-button" link="/meeting">Join meeting</CTAButton> -->
          </div>
        </div>
      </div>
    </section>
    <aside class="logo-container">
      <Logo class="logo" />
    </aside>
  </main>
</template>

<style lang="scss">
.home {
  @apply min-h-screen flex flex-col-reverse items-center justify-center text-gray-600 sm:flex-row;
  @apply dark:bg-black dark:text-gray-100;
  .left {
    @apply w-full p-6 flex justify-center lg:w-1/2;
    .container {
      @apply max-w-lg;
      .title {
        @apply text-4xl font-bold mb-8;
      }

      .intro {
        @apply mb-8 leading-7;
        h2 {
          @apply text-xl mb-4 font-semibold;
        }
        p {
          @apply mb-4;
        }
        a {
          @apply text-teal-700 underline dark:text-teal-400;
        }
      }
      .callToAction {
        .before-button {
          @apply text-3xl font-thin mb-12;
        }
        .buttons {
          .button {
            @apply mr-4 last:mr-0 transition-all;
            @apply dark:bg-transparent dark:text-teal-100 dark:border dark:border-teal-400;
            @apply dark:hover:bg-teal-400 dark:hover:text-black;
          }
        }
        @apply mb-6;
      }
    }
  }
  .logo-container {
    @apply w-full h-full flex justify-center p-10 text-gray-600 sm:w-1/2 sm:p-0;
    .logo {
      @apply fill-teal-600 w-32 sm:w-80;
    }
  }
}
</style>

<script setup lang="ts">
import Logo from '@/components/Logo.vue';
</script>
