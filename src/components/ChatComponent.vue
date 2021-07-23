<template>
  <div>
    <div>
      <div v-for="msg in messages" :key="msg.id">
        <b-row v-if="!msg.itsme">
          <b-col>
            <div class="container message">
              <span class="time-left">{{ msg.idRecipient }}</span>
              <br />
              <p id="expand">{{ msg.text }}</p>
              <span class="time-left">{{ msg.time }}</span>
            </div>
          </b-col>
          <b-col></b-col>
          <b-col></b-col>
        </b-row>
        <b-row v-if="msg.itsme">
          <b-col></b-col>
          <b-col></b-col>

          <b-col>
            <div class="container message">
              <span class="time-left">Me</span>
              <br>

              <p id="expand">{{ msg.text }}</p>
              <span class="time-right">{{ msg.time }}</span>
            </div></b-col
          >
        </b-row>
      </div>

      <br />
    </div>
  </div>
</template>

<script>
export default {
  name: "ChatComponent",
  props: {
    msg: String,
  },
  data() {
    return {
      messages: [
        {
          id: 0,
          idRecipient: 1,
          idSender: 0,
          itsme: false,
          text: "Hi. How are you?",
          time: "12:50",
        },
        {
          idRecipient: 1,
          idSender: 0,
          itsme: true,
          text: "Im fine and you?",
          time: "12:59",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.message {
  height: 100%;
  padding: 10px;
  background-color: white;
  border: 1px solid black;
  border-radius: 10px;
}
#expand {
  width: 100%;
}
.navbar-brand {
  color: white !important;
  align-content: center;
}
.time-right {
  float: right;
  color: #aaa;
}

/* Style time text */
.time-left {
  float: left;
  color: #999;
}
.row {
  margin: 0;
}
</style>
