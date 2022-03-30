<template>
  <div class="layout">
    <nuxt />
    <!-- important to have the rest of the page  -->
    <social-chat id="social-button" icon :attendants="attendants">
      <p slot="header">
        Click on one of our attendants below to chat on WhatsApp.
      </p>
      <template #button>
        <img
          src="https://raw.githubusercontent.com/ktquez/vue-social-chat/master/src/icons/whatsapp.svg"
          alt="icon whatsapp"
          aria-hidden="true"
        />
      </template>
      <small slot="footer">Opening hours: 8am to 6pm</small>
    </social-chat>
  </div>
</template>

<script>
import { SocialChat } from 'vue-social-chat'

export default {
  name: 'DefaultLayout',
  components: {
    SocialChat,
  },
  data() {
    return {
      attendants: [
        {
          app: 'whatsapp',
          label: 'Technical support',
          name: 'Alan Ktquez',
          number: '5581983383532',
          avatar: {
            src: 'https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4',
            alt: 'Alan Ktquez avatar',
          },
        },
      ],
    }
  },
}
</script>

<style>
:root #social-button {
  --vsc-bg-header: orange;
  --vsc-bg-footer: #fafafa;
  --vsc-text-color-header: yellow;
  --vsc-text-color-footer: green;
  --vsc-bg-button: pink;
  --vsc-text-color-button: purple;
  --vsc-outline-color: #333;
  --vsc-border-color-bottom-header: teal;
  --vsc-border-color-top-footer: #f3f3f3;
}
</style>
