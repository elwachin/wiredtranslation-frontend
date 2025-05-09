<template>
  <div class="app">
    <h1>LanguageWire Translator</h1>
    <input v-model="text" @input="debouncedTranslate" :placeholder="placeholder" />
    <select v-model="language" @change="debouncedTranslate">
      <option v-for="lang in languages" :key="lang" :value="lang">{{ lang }}</option>
    </select>
    <p><strong>Translation:</strong> {{ result }}</p>
  </div>
</template>

<script>
import axios from 'axios'
import { debounce } from 'lodash'
import { API_URL, DEFAULT_PLACEHOLDER, LANGUAGES } from './constants'
import '@/assets/css/styles.css'

export default {
  data() {
    return {
      text: '',
      language: 'spanish',
      result: '',
      languages: LANGUAGES,
      placeholder: DEFAULT_PLACEHOLDER
    }
  },
  methods: {
    async translate() {
      if (!this.text) return
      try {
        const res = await axios.post(`${API_URL}/translate`, {
          text: this.text,
          target_language: this.language
        })
        this.result = res.data.translation
      } catch (err) {
        this.result = err.response?.data?.detail || 'Translation failed'
      }
    },
    debouncedTranslate: debounce(function () {
      this.translate()
    }, 1000)
  }
}
</script>
