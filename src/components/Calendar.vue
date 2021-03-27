<template>
    <v-row class="fill-height">
      <v-col>
        <v-sheet height="64">
          <v-toolbar
            flat
          >
            <v-toolbar-title class="text-uppercase">{{title}}</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
      </v-sheet>
        <v-sheet height="600">
          <v-calendar
            ref="calendar"
            v-model="value"
            color="primary"
            :events="events"
            :event-height="100"
          >
          </v-calendar>
        </v-sheet>
      </v-col>
    </v-row>
</template>

<script>
 export default {
    name: 'Calendar',
    data: () => ({
      title: '',
      type: 'month',
      month: '2020-03-01',
      value: '',
      events: [
        {
          name: 'Aviation case study',
          start: '2021-03-03',
          color: '#219653'
        },
        {
          name: 'Aviation case study',
          start: '2021-03-06',
          color: '#219653'
        },
        {
          name: 'Voyager Emissions Dashboard',
          start: '2021-03-08',
          color: '#2D9CDB',
        },
        {
          name: 'Voyager Emissions Dashboard',
          start: '2021-03-09',
          color: '#2D9CDB',
        },
        {
          name: 'Create mailing lists',
          start: '2021-03-11',
          color: '#828282'
        },
        {
          name: 'Karthik ?project',
          start: '2021-03-18',
          color: '#9B51E0'
        },
        {
          name: '?',
          start: '2021-03-23',
          color: '#F2994A'
        }
      ],
    }),
     methods: {
      // getMonthName(dtStr) {
      //   const date = new Date(dtStr)
      //   if (date.toString() !== 'Invalid Date')
      //       return date.toLocaleString('en-us', { month: 'long' })
      //   else
      //       return 'December'
      // },
       getTitle: function() {
         this.title = this.$refs.calendar.title}
    },
    mounted: function(){
        this.getTitle()
    }
  }
</script>