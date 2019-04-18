<template>
<div>
  <div v-if="user">
    <div class="header">
      <div class ="username">
        <h1>{{user.name}}</h1>
      </div>
      <div>
        <p>
          <a @click="toggleUpload"><i class="fa fa-quote-right" aria-hidden="true"></i></a>
          <a href="#" @click="logout"><i class="fa fa-window-close" aria-hidden="true"></i></a>
        </p>
      </div>
    </div>
    <uploader :show="show" @escape="escape" @uploadFinished="uploadFinished" />
  </div>
  <div v-else>
    <p>If you would like to upload a quote, please register for an account or login.</p>
    <router-link to="/register" class="pure-button">Register</router-link> or
    <router-link to="/login" class="pure-button">Login</router-link>
  </div>
</div>
</template>


<script>
export default {
  name: 'mypage',
  computed: {
    user() {
      return this.$store.state.user;
    }
  },
   created() {
    this.$store.dispatch("getUser");
  },
  methods: {
    async logout() {
      try {
        this.error = await this.$store.dispatch("logout");
      } catch (error) {
        console.log(error);
      }
    },
  }
}
</script>

<style scoped>
.header {
  display: flex;
}

.username {
    margin-left:545px;
}

.header a {
  padding-left: 50px;
  color: #222;
  font-size: 2em;
}

.header svg {
  margin-top: 12px;
}
</style>