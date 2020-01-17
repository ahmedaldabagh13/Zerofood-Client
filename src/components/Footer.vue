<template>
  <v-footer height="auto">
    <v-layout justify-center row wrap>
      <v-row justify="center" align="start">
        <v-col md-cols="3" cols="12" color="dark black" dark>
          <v-card class="mx-auto" max-width="344" dark outlined>
            <v-list-item three-line>
              <v-list-item-content>
                <v-list-item-title class="headline mb-1"
                  >About Us</v-list-item-title
                >
                <v-list-item-subtitle
                  >We are a fast food service that trying to make the world
                  butter place to live</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
        <v-col md-cols="3" cols="12" color="dark black" dark>
          <v-card class="mx-auto" max-width="344" dark outlined>
            <v-list-item three-line>
              <v-list-item-content>
                <v-list-item-title class="headline mb-1"
                  >Terms of service</v-list-item-title
                >
                <v-list-item-subtitle
                  >Never involved in privacy violation Use the service
                  responsibly</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
        <v-col md-cols="3" cols="12" color="dark black" dark>
          <v-card class="mx-auto" max-width="344" dark outlined>
            <v-list-item three-line>
              <v-list-item-content>
                <v-list-item-title class="headline mb-1"
                  >Pay vai</v-list-item-title
                >
                <v-list-item-content>
                  <v-btn
                    depressed
                    small
                    color="blue-grey"
                    class="ma-2 white--text"
                  >
                    <a
                      href="https://www.paypal.com/"
                      target="_blank"
                      rel="noopener noreferrer"
                    >
                      <img
                        src="https://www.g2a.com/static/assets/payments/paypal.svg"
                        class="paypal"
                        style="width:auto"
                    /></a>
                  </v-btn>
                  <v-btn
                    depressed
                    small
                    color="blue-grey"
                    class="ma-2 white--text"
                  >
                    <a
                      href="https://www.mastercard.us/"
                      target="_blank"
                      rel="noopener noreferrer"
                    >
                      <img
                        src="https://www.g2a.com/static/assets/payments/mastercard.svg"
                        class="mastercard"
                        style="width:auto"
                      />
                    </a>
                  </v-btn>
                  <v-btn
                    depressed
                    small
                    color="blue-grey"
                    class="ma-2 white--text"
                  >
                    <a
                      href="https://usa.visa.com/"
                      target="_blank"
                      rel="noopener noreferrer"
                    >
                      <img
                        src="https://www.g2a.com/static/assets/payments/visa.svg"
                        class="visa"
                        style="width:auto"
                    /></a>
                  </v-btn>
                </v-list-item-content>
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-col>
      </v-row>
      <v-flex
        color="indigo"
        justify="center"
        dark
        py-3
        text-xs-center
        white--text
        xs12
      >
        <p class="text-center black--text">
          &copy; {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </p>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    icons: [
      'fab fa-facebook',
      'fab fa-twitter',
      'fab fa-google-plus',
      'fab fa-linkedin',
      'fab fa-instagram'
    ]
  })
}
</script>

<style>
a {
  text-decoration: none !important;
  color: white !important;
  text-align: left !important;
}

.footer-payments .logo-payments {
  height: 22px;
  margin: 0;
}

.footer-payments .logo-payments {
  display: inline-block;
  height: 17px;
  margin-top: 10px;
  overflow: hidden;
  vertical-align: middle;
}

.footer-payments .logo-payments img.visa {
  height: 14px;
}

.visa {
  width: 50px !important;
}

.mastercard {
  width: 120px !important;
}

.paypal {
  width: 80px !important;
}

.footer-payments .logo-payments img.mastercard {
  height: 14px;
}
</style>
