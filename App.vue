<template>
  <v-app>
    <v-app-bar
      app
      color="dark"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
      <Mypage/>
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <Cards title="Daniele test1000" description="bla blafggfh bla testo di prova" :colore="coloreApp[1]">
              <template slot="A"><p>Sono una slot machine</p></template>
              <template slot="B"><h1>Hello World</h1></template>
            </Cards>
          </div>
          <div class="col-sm">
            <Cards title="Daniele test2" description="bla bla bla racconto di prova" colore="red">
              <template slot="B"><a v-bind:href="url" target="/blank"><h1>Hello World2</h1></a></template>
              <template slot="A"><p>Sono una slot machine</p></template>
            </Cards>
          </div>
          <div class="col-sm">
            <Cards title="Daniele test3" description="bla bla bla frase di prova test immagine" colore="red"/>
          </div>
        </div>
      </div>
      <hr/><br/>
      <Form/>
      <br/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Mypage from './components/Mypage.vue';
import Cards from './components/Cards.vue';
import Form from './components/Form.vue';
export default {
  name: 'App',

  components: {
    HelloWorld,
    Mypage,
    Cards,
    Form
  },
  data(){
    return{
      coloreApp: ['verde','giallo','Celeste'],
      url:'https://getbootstrap.com/docs/4.6/components/forms/'
    }
  }
};
</script>
