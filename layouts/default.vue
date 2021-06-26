<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      dense
      flat
      class="primary"
      dark

    >
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon small>mdi-email</v-icon>

      </v-btn>

       <span v-text="title"></span>

      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon small>mdi-whatsapp</v-icon>
      </v-btn>

       <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon small>mdi-phone</v-icon>


      </v-btn>

      <span>03108559858</span>


    </v-app-bar>


    <v-toolbar class="mt-12" height="120px">

      <div>

       <v-img max-width="120px" src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png" />
      </div>

      <v-spacer />

      <div>

        <span class="pa-2">Home</span>
        <span class="pa-2">Winkel</span>
        <span class="pa-2">Neem Contact Op</span>
      </div>
    </v-toolbar>

    <v-carousel hide-delimiters>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      >


      <div>
        <div v-if="i == 0" dark class="mt-15 sliderSection sliderSection1 success lighten-2">one</div>
        <div v-if="i == 2" dark class="mt-15 sliderSection sliderSection3 error">one</div>
      </div>


       </v-carousel-item>
    </v-carousel>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

  <v-footer
      dark
      class="grey darken-3 pb-15"
      >
    <v-col cols="3"><v-img max-width="120px" src="https://delmaro.nl/wp-content/uploads/2020/10/delmaro_logo_optimize.png" />
    <p>Delmaro is al jaren een vertrouwde naam als het gaat om de import en export van Zuid Amerikaanse en Latijnse delicatessen.</p>
    <p>Al langer dan 10 jaar heeft onze groothandel kwaliteit én service hoog in het vaandel staan.</p>
    </v-col>

    <v-col cols="3">
      <h3 class="mb-5"> Get In Touch</h3>
      <p>Phone 085 444 4710</p>
      <p>Mobile</p>
      <p>Email info@delmaro.nl</p>

      <p>Chamber of Commerce number 58516395</p>
      <p>VAT number 853072292B01</p>
      <p>IBAN NL18INGB0008287958</p>
    </v-col>

 <v-col cols="3">
      <h3 class="mb-5">Useful Links</h3>
      <p to="/"> > Home</p>
      <p to="/"> > Privacy Policy</p>
      <p to="/"> > Get In Touch</p>
      <p to="/"> > About Us</p>
      <p to="/"> > Shop</p>
    </v-col>

     <v-col cols="3">
      <h3 class="mb-5">Product Categories</h3>
      <p to="/"> Chiles </p>
      <p to="/"> Chili Pasta </p>
      <p to="/"> Fruit </p>
      <p to="/"> Souces </p>
      <p to="/"> Specerijen En Specerijen </p>
      <p to="/"> Vegetables </p>
    </v-col>




    </v-footer>

    <v-footer app padless dark>
    <v-col>
    <div>© Copyright 2021 Delmaro</div>
    </v-col>

    </v-footer>

  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
          {
            src: 'https://delmaro.nl/wp-content/uploads/2021/05/2121.png',
          },
          {
            src: 'https://delmaro.nl/wp-content/uploads/2021/05/1123.png',
          }
        ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style>

    .sliderSection {

    width:50%;
    height:150px;
    color:white;
    }


    .sliderSection1 {
    opacity:0.9;
    }

    .sliderSection3 {
    opacity:0.5;
    }


</style>
