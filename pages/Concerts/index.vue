<template>
  <keep-alive>
    <div class="form-center">
      <h1 class="form-title">Wecolme to Concert Ticket Booking 🌏</h1>
      <form action="">
        <b-field grouped>
          <b-field label="Firstname" expanded>
            <b-input v-model="firstname" id="firstname"></b-input>
          </b-field>
          <b-field label="Lastname" expanded>
            <b-input v-model="lastname" id="lastname"></b-input>
          </b-field>
        </b-field>

        <b-field grouped>
          <b-field
            label="Email"
            message="We'll use this for sending you tickets"
            expanded
          >
            <b-input type="email" value="" maxlength="30"> </b-input>
          </b-field>

          <b-field label="Select a date" type="is-success" expanded>
            <b-datepicker
              v-model="dateselected"
              placeholder="Click to select..."
              icon="calendar-today"
              trap-focus
            >
            </b-datepicker>
          </b-field>
        </b-field>

        <b-button
          class="submitbutton"
          type="is-success"
          expanded
          v-on:click.prevent="logging"
          >Book Tickets</b-button
        >
      </form>
    </div>
  </keep-alive>
</template>

<script>
export default {
  data() {
    return {
      firstname: "",
      lastname: "",
      email: "",
      phonenumber: "",
      dateselected: new Date()
    };
  },
  methods: {
    logging: function() {
      console.log(
        `FN: ${this.firstname}, LN: ${this.lastname}, Email: ${this.email}, `
      );
    }
  }
};
</script>

<style scoped>
.form-title {
  text-align: center;
  margin-bottom: 3em;
}

.form-center {
  padding-top: 4em;
  width: 1000px;
  margin: 0 auto;
}
.submitbutton {
  margin-top: 2em;
}
</style>
