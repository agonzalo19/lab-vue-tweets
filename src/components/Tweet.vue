  
<template>
<div className="tweet">
    <Imatge :Imatge="tweet.user.image"/>

    <div className="body">
      <div className="top">
        <span className= "user">
          <span className="name">{{ tweet.name }}</span>
          <span className="handle">{{ tweet.handle }}/span>
        </span>

        <span className="timestamp">{{ tweet.timestamp }}</span>
      </div>

      <p className="message">
        {{ tweet.message }}
      </p>

      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import Imatge from "./Tweet-components/Imatge.vue";
import User from "./Tweet-components/User.vue"
import Message from "./Tweet-components/Message.vue"
import Actions from "./Tweet-components/Actions.vue"
import Timestamp from "./Tweet-components/Actions.vue"

export default{
    props: {
        Tweet: Object
    },
    components: { 
      Imatge,
      User,
      Message,
      Actions,
      Timestamp,
      }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
