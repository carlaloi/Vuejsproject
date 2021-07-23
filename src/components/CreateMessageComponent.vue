<template>
  <div id="extern">
    <b-form-textarea
      id="text"
      v-model="text"
      placeholder="Enter something"
      rows="2"
      max-rows="2"
    >
    </b-form-textarea>
    <b-button variant="success" id="sent">Sent</b-button>
  </div>
</template>

<script>
export default {
  name: "CreateMessageComponent",
  data() {
    return {
      text: "",
    };
  },
};
</script>

<style>
#text {
  width: 75%;
  float: left;
  height: 100%;
}
#sent {
  float: right;
  width: 20%;
  padding-left: 10px;
}
#extern {
  height: 40px;
  width: 100%;
}
</style>