<template>
    <div class="w-full absolute top-10 flex flex-col items-center justify-center">
        
        <UFormGroup v-bind:label="ingre1">
            <br>
    <UInput v-on:input="firstIngre" placeholder="ใส่วัตถุดิบที่ 1" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  
  <UFormGroup label="วัตถุดิบที่ 2">
            <br>
    <UInput v-on:input="secondIngre" placeholder="ใส่วัตถุดิบที่ 2" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  <UFormGroup label="วัตถุดิบที่ 3">
            <br>
    <UInput v-on:input="thirdIngre" placeholder="ใส่วัตถุดิบที่ 3" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  <UFormGroup label="วัตถุดิบที่ 4">
            <br>
    <UInput v-on:input="fourtIngre" placeholder="ใส่วัตถุดิบที่ 4" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>
  

 


 
  <UButton v-on:click="saveAllIngre(firstIngre, secondIngre, thirdIngre, fourtIngre)">บันถึก</UButton>

  <p>วัตถุดิบที่ 1 = {{ ingredient1 }}</p>
  <p>วัตถุดิบที่ 2 = {{ ingredient2 }}</p>
  <p>วัตถุดิบที่ 3 = {{ ingredient3 }}</p>
  <p>วัตถุดิบที่ 4 = {{ ingredient4 }}</p>

        <nuxt-link to="./">To index</nuxt-link>

  

    </div>
</template>

<script>

export default{
  data() {
    return {
      ingre1: "วัตถุดิบที่ 1",
      ingredient1: '',
      ingredient2: '',
      ingredient3: '',
      ingredient4: '',
      ingredient: 1
      //inputIngredient: '<UFormGroup label="วัตถุดิบที่ 4"> <br> <UInput placeholder="ใส่วัตถุดิบที่ 4" icon="i-heroicons-envelope" class="w-60 h-5s" /> </UFormGroup> <br>'
    }
  },
  methods: {

    firstIngre(event){
      this.ingredient1 = event.target.value

    },

    secondIngre(event){
      this.ingredient2 = event.target.value

    },
    thirdIngre(event){
      this.ingredient3 = event.target.value

    },
    fourtIngre(event){
      this.ingredient4 = event.target.value

    },
  components:{
    
  }
 }
}

</script>
