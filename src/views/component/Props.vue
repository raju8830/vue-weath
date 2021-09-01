<template>


  <!-- Page Props Section part -->
  <div class="props">
    <div class="btn_props">
      <button>{{ btnText }}</button>
      <button>{{ abc }}</button>
    </div>
  </div>



</template>

<script>
export default {
  props:['btnText','abc', 'content']
};
</script>

<style>
button{
  background: aquamarine;
  font-size: 60px;
  border-radius: 20px;
  padding: 10px;
  color: black;
  outline: none;
  border: none;
  margin-top: 10px;
  text-transform: capitalize;
  margin-right: 10px;
}
</style>