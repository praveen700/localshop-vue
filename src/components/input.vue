<template>
    <div>
        <label for="input-box">Enter your text:</label>
        <input type="text" 
        :value="modelValue" 
        @input="$emit('update:modelValue', $event.target.value)" 
         name="input-box" placeholder="Type something...">

    </div>
</template>

<script>
export default {
    name: 'Input',
    props: {
        modelValue: String
    }

}
</script>

<style scoped>
input[type="text"] {
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  font-size: 16px;
  outline: none;
  transition: border-color 0.2s ease-in-out;
}

input[type="text"]:focus {
  border-color: #6d9bf1;
}

</style>