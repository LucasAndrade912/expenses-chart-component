<script setup>
import { data as json } from '@/data'

const data = json.map(mount => mount.amount)

const colors = [0, 1, 2, 3, 4, 5, 6].map(day => {
  const currentDay = new Date().getDay()
  
  if (day === currentDay) return '#76b5bc'
  return '#ec775f'
})

const series = [{
  name: 'amounts',
  data
}]

const options = {
  chart: {
    type: 'bar',
    toolbar: {
      show: false
    },
  },
  dataLabels: {
    enabled: false
  },
  xaxis: {
    categories: ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun'],
    axisBorder: {
      show: false
    },
    axisTicks: {
      show: false
    }
  },
  yaxis: {
    show: false
  },
  grid: {
    show: false
  },
  plotOptions: {
    bar: {
      distributed: true,
      borderRadius: 4
    }
  },
  legend: {
    show: false
  },
  colors
}
</script>

<template>
  <apexchart :options="options" :series="series" height="280" />
</template>