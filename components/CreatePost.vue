<template>
  <div id="CreatePost" class="fixed z-50 bottom-0 h-full w-full overflow-hidden">

  </div>
</template>



<script setup>
import { v4 as uuidv4 } from 'uuid'
import { useUserStore } from '../stores/user'
const userStore = useUserStore()
let text = ref(null)
let isLoading = ref(false)

const adjustTextareaHeight = () => {
  var textarea = document.getElementById("textarea");
  textarea.style.height = "auto"
  textarea.style.height = textarea.scrollHeight + "px"
}


let file = ref(null)
let fileDisplay = ref(null)
let fileData = ref(null)

const clearDaata = () => {
  text.value = null
  file.value = null
  fileDisplay.value = null
  fileData.value = null
}


//const client = useSupabaseClient()
//const user = useSupabbaseUser()
</script>