<script setup lang="ts">
import {Button} from '@/components/ui/button'
import { Calendar } from '@/components/ui/calendar'
import {supabase} from '@/lib/supabase'
import { onMounted } from 'vue';

onMounted(()=>{
  getData()
})

async function getData(){
  const {data} = await supabase.from('products').select('*')
  console.log(data)
}
</script>

<template >
  <div>
    <Button>HEEEELELOOOO</Button>
    <LoginForm/>
  </div>
</template>

<style scoped></style>
