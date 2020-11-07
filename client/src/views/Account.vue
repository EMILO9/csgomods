<template>
  <div class="account">
      <v-container>
  <v-card tile>
          <v-toolbar>
      <v-toolbar-title>My Account (fuqboi@gmail.com)</v-toolbar-title>
    </v-toolbar>
        <v-form class="accountForm"> 
            <v-text-field dense outlined value="fuqboi@gmail.com" type="email" prepend-icon="mdi-email" disabled></v-text-field>
            <v-text-field dense outlined value="password" type="password" prepend-icon="mdi-lock" disabled></v-text-field>
                <v-btn color="primary" class="mr-4"  depressed @click="overlay = true">edit</v-btn>
                <v-btn color="success" class="mr-4"  depressed>save</v-btn>
                 <v-divider class="divider"></v-divider>
                   <v-tabs>
    <v-tab>Bought</v-tab>
    <v-tab>Sold</v-tab>
        <v-tab-item>
          <v-container fluid>
            <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Purchased
          </th>
          <th class="text-left">
            Seller
          </th>
          <th class="text-left">
            Price
          </th>
        <th class="text-left">
            Size
          </th>
          <th class="text-left">
            Download
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in 10"
          :key="item"
        >
          <td>{{ new Date().getDate() + item}} - {{new Date().getMonth() + item}} - {{new Date().getFullYear() + item}}</td>
          <td>Seller #{{item}}</td>
          <td>{{14.66 + item * 3}}</td>
          <td>{{0.55 + item * 5}}GB</td>
          <td><v-btn color="primary" class="mr-4" block  depressed>csgomod{{item}}.rar</v-btn></td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
        <v-pagination
      value=2
      color="primary"
      length=6
      total-visible=10
    ></v-pagination>
          </v-container>
        </v-tab-item>
                <v-tab-item>
          <v-container fluid>
            <v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Sold
          </th>
          <th class="text-left">
            Buyer
          </th>
          <th class="text-left">
            Price
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in 10"
          :key="item"
        >
          <td>{{ new Date().getDate() + item}} - {{new Date().getMonth() + item}} - {{new Date().getFullYear() + item}}</td>
          <td>Buyer #{{item}}</td>
          <td>{{14.66 + item * 3}}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
        <v-pagination
      value=2
      color="primary"
      length=6
      total-visible=10
    ></v-pagination>
          </v-container>
        </v-tab-item>
  </v-tabs>
                   
        </v-form>
  </v-card>
  </v-container>
     <v-overlay v-if="overlay" absolute="true" opacity="0.9" fluid>
       <v-form>
    <v-text-field
      dense outlined placeholder="Password"
    ></v-text-field>
        <v-text-field
      dense outlined placeholder="Repeat Password"
    ></v-text-field>

    <v-btn
      color="primary"
      class="checkbtn overlayWidth"
      depressed
      block
    >
      Check
    </v-btn>

    <v-btn
      block
      class="checkbtn overlayWidth"
      @click="overlay = false"
      depressed
    >
      Hide
    </v-btn>
  </v-form>
   </v-overlay>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Account",
  data () {
    return {
      overlay: false
    }
  },
  methods: {
      getParams () {
          console.log(this.$route.params.id)
      }
  }
};
</script>