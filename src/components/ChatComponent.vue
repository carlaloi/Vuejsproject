<template>
  <div>
    <h1>{{ msg }}</h1>
    <div>
      <b-row>
        <b-col>
          <div class="container message">
            <span class="time-left">Felipe</span>
            <br>
            <p id="expand">Hello. How are you?</p>
            <span class="time-left">12:50</span>
          </div>
        </b-col>
        <b-col></b-col>
        <b-col></b-col>
      </b-row>
      <br />
      <b-row>
        <b-col></b-col>
        <b-col></b-col>

        <b-col>
          <div class="container message">
            <p id="expand">Hi. I'm fine!</p>
            <span class="time-right">12:59</span>
          </div></b-col
        >
      </b-row>
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
      messages: [{}],
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
</style>
