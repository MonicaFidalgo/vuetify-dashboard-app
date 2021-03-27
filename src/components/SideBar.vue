<template>
  <v-card class="card">
    <v-tabs vertical>
      <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Homepage
      </v-tab>
      <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Menu 1
      </v-tab>
      <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Users
      </v-tab>
      <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Calendar
      </v-tab>
      <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Menu 4
      </v-tab>
       <v-tab class="justify-start">
        <v-icon left>
          mdi-view-dashboard-outline
        </v-icon>
        Menu 5
      </v-tab>

      <v-tab-item>
        <v-card flat>
          <v-card-text class="u-bg--white">
            <p>
              Homepage
            </p>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-text class="u-bg--white">
            <p>
              Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
            </p>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-text>
          <Table />
          <Footer />
          </v-card-text>
        </v-card>
      </v-tab-item>
            <v-tab-item>
        <v-card flat>
          <v-card-text>
          <Calendar />
          <Footer />
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs>
  </v-card>
</template>


<script>

import Calendar from './Calendar';
import Footer from './Footer';
import Table from './Table';

 export default {
  name: 'SideBar',
  components: {
    Calendar,
    Table,
    Footer
    },
}
</script>