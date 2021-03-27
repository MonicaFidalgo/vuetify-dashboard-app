<template>
    <div>
      <v-data-table
        :headers="headers"
        :items="contacts"
        item-key="name"
        class="elevation-1"
        show-select
      >
        <template v-slot:item.image="{ item }">
            <img :src="require(`../assets/img/${item.image}.png`)" style="width: 24px; height: 24px" />
        </template>
      </v-data-table>
    </div>
</template>


<script>
 export default {
  name: 'Table',
  data () {
    return {
      email: '',
      contacts: [
        {
          image:'LindseyStroud',
          name: 'Lindsey Stroud',
          email: 'lindsey.stroud@gmail.com',
          companyName: 'Hatchbuck',
          role: 'Manager',
          forecast: '50 %',
          activity: '5 Minutes ago',
        },
        {
          image:'NicciTroiani',
          name: 'Nicci Troiani',
          email: 'nicci.troiani@gmail.com',
          companyName: 'Slack',
          role: 'Manager',
          forecast: '75 %',
          activity: '14 Minutes ago',
        },
        {
          image:'GeorgeFields',
          name: 'George Fields',
          email: 'george.fields@gmail.com',
          companyName: 'Clockify',
          role: 'CEO',
          forecast: '10 %',
          activity: '6 Hours ago',
        },
        {
          image:'RebeccaMoore',
          name: 'Rebecca Moore',
          email: 'rebecca.moore@gmail.com',
          companyName: 'Upwork',
          role: 'Manager',
          forecast: '25 %',
          activity: 'Dec 14, 2018',
        },
        {
          image:'JaneDoe',
          name: 'Jane Doe',
          email: 'jane.doe@gmail.com',
          companyName: 'Trello',
          role: 'Engineer',
          forecast: '30 %',
          activity: 'Dec 12, 2018',
        },
        {
          image:'JonesDermot',
          name: 'Jones Dermot',
          email: 'dermot.jones@gmail.com',
          companyName:'Slack',
          role: 'Developer',
          forecast: '40 %',
          activity: 'Dec 12, 2018',
        },
        {
          image:'MartinMerces',
          name: 'Martin Merces',
          email: 'martin.merces@gmail.com',
          companyName: 'Google',
          role: 'Manager',
          forecast: '60 %',
          activity: 'Dec 18, 2018',
        },
        {
          image:'FranzFerdinand',
          name: 'Franz Ferdinand',
          email: 'franz.ferdiand@gmail.com',
          companyName: 'Facebook',
          role: 'Manager',
          forecast: '100 %',
          activity: 'Dec 11, 2018',
        },
      ],
    }
  },
  computed: {
    headers () {
      return [
         {
          text: 'Name',
          align: 'start',
          sortable: false,
          value: 'image',
          width: "24px"
        },
        {
          text: '',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        {
          text: 'Email',
          value: 'email',
        },
        { text: 'Company Name', value: 'companyName' },
        { text: 'Role', value: 'role' },
        { text: 'Forecast', value: 'forecast' },
        { text: 'Recent activity', value: 'activity' },
      ]
    },
  },
}
</script>