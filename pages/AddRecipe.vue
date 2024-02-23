<template>
    <div class="w-full absolute top-10 flex flex-col items-center justify-center">
        
        <UFormGroup v-bind:label="ingre1">
            <br>
    <UInput placeholder="ใส่วัตถุดิบที่ 1" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  
  <UFormGroup label="วัตถุดิบที่ 2">
            <br>
    <UInput placeholder="ใส่วัตถุดิบที่ 2" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  <UFormGroup label="วัตถุดิบที่ 3">
            <br>
    <UInput placeholder="ใส่วัตถุดิบที่ 3" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>

  <UFormGroup label="วัตถุดิบที่ 4">
            <br>
    <UInput placeholder="ใส่วัตถุดิบที่ 4" icon="i-heroicons-envelope" class="w-60 h-5s" />
  </UFormGroup>
  <br>
  

  <div id="ingrInput"></div>

  <UButton v-on:click="createP">เพิ่มวัตถุดิบ</UButton>

  <UButton>บันถึก</UButton>

  <p>{{ ingre1 }}</p>

        <nuxt-link to="./">To index</nuxt-link>
    </div>
</template>

<script>

export default{
  data() {
    return {
      ingre1: "วัตถุดิบที่ 1",
      ingredient: 1,
      inputIngredient: '<UFormGroup label="วัตถุดิบที่ 4"> <br> <UInput placeholder="ใส่วัตถุดิบที่ 4" icon="i-heroicons-envelope" class="w-60 h-5s" /> </UFormGroup> <br>'
    }
  },
  methods: {
    addIngredient(){
      return this.inputIngredient
    },

    outputInput(){
      return this.inputIngredient
    },

    createP(){
      var element = document.getElementById('ingrInput');
      element.innerHTML = this.inputIngredients
    },

    ingredientCount(){

    }
  },
}

</script>
