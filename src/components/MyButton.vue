<template>
  <button 
    class="button" 
    :class="{ double, triple, operation }"
    @click="$emit('onClick', label)"
  >
    {{label}}
  </button>
</template>

<script>
export default {
  props: {
    label: {},
    operation: { type: Boolean },
    double: { type:Boolean },
    triple: { type:Boolean },
  }
}
</script>

<style>
  :root{
    --bg-button: #f0f0f0;
    --border-button: solid 1px #888;
  }
  
  .button{
    font-size: 1.4em;
    background-color: var(--bg-button);
    border: none;
    border-right: var(--border-button);
    border-bottom: var(--border-button);
    outline: none;
    cursor: pointer;
  }

  .button:hover{
    background-color: #c7c7c7;
  }

  .button:active{
    background-color: rgb(97, 97, 97);
  }

  .button.double{
    grid-column: span 2;
  }

  .button.triple{
    grid-column: span 3;
  }

  .button.operation {
    background-color: #fa8231;
    color: #fff;
  }

  .button.operation:hover {
    background-color: #fa8231cc;
  }

  .button.operation:active {
    background-color: #803706cc;
  }

</style>