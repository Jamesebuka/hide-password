<template>
      <div class="field">
          <img 
          @click="change"
          v-if="!show" 
          class="absolute"
          style="top: 10px" 
          src="https://img.icons8.com/material-outlined/24/000000/closed-eye.png"/>

          <img 
          @click="change" 
          v-if="show" 
          class="absolute" 
          src="https://img.icons8.com/ios/50/000000/visible--v1.png"/>
       <input v-if="!show" v-model="input" type="text" placeholder="Password" /> 
       <input v-if="show" v-model="input" type="password" placeholder="password" />
      </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      show: true,
      input: ""
    }
  },
  methods: {
    change() {
      this.show = !this.show;
      console.log("change now");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.field {
 width: 300px;
 height: 35;
 margin: 0 auto;
 position: relative;
}

.absolute {
  position: absolute;
  right: 5%;
  cursor: pointer;
}

input {
  width: 100%;
  height: 30px;
  padding: 5px 10px;
}

input:focus {
  outline: none;
}
</style>
