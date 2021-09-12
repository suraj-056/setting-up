<template>
  <div id="home">
    <q-input
      class="q-pa-lg"
      autogrow:true
      bottom-slots
      v-model="text"
      placeholder="write something"
      counter
      maxlength="180"
      :dense="dense"
    >
      <template v-slot:before>
        <q-avatar>
          <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
        </q-avatar>
      </template>

      <template v-slot:append>
        <q-icon class="cursor-pointer" />
        <!-- <q-icon name="schedule" /> -->
      </template>

      <template v-slot:after>
        <q-btn
          @click="clicked"
          outline
          q-pa="10px"
          rounded
          color="primary"
          label="Sweet"
        />
      </template>
    </q-input>

    <q-item >
      <q-item-section>
        <q-item-label>name</q-item-label>
        <q-item-label caption lines="2"
          >Secondary line text. Lorem ipsum dolor sit amet, consectetur
          adipiscit elit.</q-item-label
        >
      </q-item-section>

      <q-item-section side top>
        <q-item-label caption>5 min ago</q-item-label>
        <q-icon name="star" color="yellow" />
      </q-item-section>
    </q-item>
  </div>
</template>

<script>
export default {
  name:'home',
  // data(){
  // newsweets:'',
  //    existingitems[
  //     {text:'insiodfjsaf',id:1},
  //     {text:'insiodfjsaf',id:3},
  //    {text:'insiodfjsaf',id:2}
      
  //     ]
  // },
  // methods:{
  //   clicked(){
  //     console.log("helo")
  //   }

  }

</script>
<style scoped>
li {
  width: 100%;
  background: blue;
}
</style>