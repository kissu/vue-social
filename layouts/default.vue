<template>
  <div class="layout">
    <social-chat icon :attendants="attendants">
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
export default {
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
