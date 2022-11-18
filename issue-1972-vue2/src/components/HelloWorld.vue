<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Scenario using v2
      <input v-model="teste"
         :disabled="true"
         :required="false"
         :custom-1="true"
         :custom-2.prop="true"
         :custom-3="true ? '' : null"
      >.
    </p>

    <p>
      Scenario using custom component with prop="true"
      <CustomComponent :shouldRender="true"/>
    </p>

    <p>
      Scenario using custom component with prop="false"
      <CustomComponent :shouldRender="false"/>
    </p>
  </div>
</template>

<script>
import CustomComponent from './CustomComponent.vue';

export default {
    name: "HelloWorld",
    props: {
        msg: String,
    },
    components: { CustomComponent }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
