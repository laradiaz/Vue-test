<template>
  <div>
    <v-app-bar color="blue-grey darken-2" dense dark>
      <v-toolbar-title>Accounts</v-toolbar-title>

      <v-spacer />
      <v-btn>{{ userEmail }}</v-btn>
      <v-btn @click="logout" id="logout">
        Salir
      </v-btn>
    </v-app-bar>

    <v-container class="accounts">
      <v-row>
        <v-col>
          <accounts-form />
        </v-col>

        <v-col>
          <account-list />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import AccountsForm from "../components/AccountsForm";
import AccountList from "../components/AccountList";

export default {
  name: "Accounts",
  components: { AccountList, AccountsForm },

  computed: {
    userEmail() {
      return localStorage.getItem("user-username");
    },
  },

  methods: {
    logout() {
      localStorage.removeItem("user-token");
      this.$router.go("/");
    },
  },
};
</script>

<style lang="scss">
.accounts {
  padding-top: 200px;
  padding-bottom: 63px;
}
</style>
