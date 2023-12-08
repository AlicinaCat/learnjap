<template>
  <v-container class="fill-height">
    <v-responsive class="align-center text-center fill-height">
      <v-row class="d-flex align-center justify-center">
        <h1>Quiz</h1>
      </v-row>
      <v-row class="d-flex align-center justify-center">
        <h2>word is {{vocab[index].hiragana}}</h2>
      </v-row>
      <v-row class="d-flex align-center justify-center">
        <v-text-field v-model="translation" label="translation"></v-text-field>
      </v-row>
      <v-row class="d-flex align-center justify-center">
        <v-btn type="submit" @click="submit" block class="mt-2">Submit</v-btn>
      </v-row>
      <v-row class="d-flex align-center justify-center">
        <v-btn type="submit" @click="next" block class="mt-2">Next</v-btn>
      </v-row>
      <v-row class="d-flex align-center justify-center">
        <p v-show="correct">Good job!</p>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script lang="ts" setup>
import vocab from '../vocab';
import { ref, computed } from 'vue';
// import HelloWorld from '@/components/HelloWorld.vue'

const translation = ref('');
const index = ref(Math.floor(Math.random()*vocab.length));
const correct = ref(false);

const submit = () => {
  console.log('submitting', translation.value)

  if (translation.value === vocab[index.value].english) {
    console.log('yay');
    correct.value = true;
  } else {
    console.log('boo', vocab[index.value].english);
  }
}

const next = () => {
  translation.value = '';
  correct.value = false;
  index.value = Math.floor(Math.random()*vocab.length);
}

// todo 
//- remove used words from array.
//- choose kanji or hiragana 
//- calculate score
//- see translation
</script>

