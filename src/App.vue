/* eslint-disable */

<template>
  <!-- <Greet name="Bruce" heroName="Batman" />
  <Greet :name="name" :heroName="channel" /> -->
  <!-- <Article title="Article Tiitle" :Likes="50" :isPublished="true" /> -->
  <!-- <h2>App Component username {{ name }}</h2> -->
  <!-- <button @click="showPopup =true">Show Popup</button>
  <Popup v-show="showPopup" @close="closePopup" /> -->
  <!-- <Card></Card>
  <Card>
    Card Content
  </Card>
  <Card>
    <h2> Card Content</h2>
  </Card>
  <Card>
    <img src="https://www.shutterstock.com/image-photo/tree-against-sky-on-tranquil-260nw-434350822.jpg" />
  </Card>
  <Card>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="https://www.shutterstock.com/image-photo/tree-against-sky-on-tranquil-260nw-434350822.jpg" />
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </Card> -->
  <!-- <NameList>
    <template v-slot:default="slotProps">
      {{  slotProps.firstName  }}  {{  slotProps.lastName  }}
    </template> 
  </NameList> -->
  <!-- <h4> App Component Styles</h4> -->
  <!-- <button @click="active = 'TabA'">Tab A</button>
  <button @click="active = 'TabB'">Tab B</button>
  <button @click="active = 'TabC'">Tab C</button> -->

  <!-- <TabA v-if="active === 'TabA'" />
  <TabB v-if="active === 'TabB'"/>
  <TabC v-if="active === 'TabC'" /> -->
  <!-- <keep-alive>
  <component :is="active" />
</keep-alive> -->
                <!-- <Card content="Content 2" /> -->
<!-- <ParentComponent /> -->
<!-- <CreatePost /> -->
<Data />
</template>

<script>
// import Greet from "./components/Greet.vue";
// import Article from "./components/Article.vue";
// import ComponentC from "./components/ComponentC.vue";
// import Popup from "./components/popup.vue"
// import Card from "./components/Card.vue"
// import NameList from "./components/NamesList.vue"
// import ChildStyles from "./components/ChildStyles.vue"
// import TabA from './components/TabA.vue';
// import TabB from './components/TabB.vue';
// import TabC from './components/TabC.vue';
// import CreatePost from "./components/CreatePost.vue"
// import  ParentComponent from "./components/Parent"
import Data from "./components/Data.vue"
export default {
  name: 'App',
  components:{
    // Greet,
    // Card,
    // ChildStyles,,
    // ParentComponent,
    // CreatePost,
    Data
  },
  data(){
    return{
      showPopup:false,
      name:"",
      channel: "Code",
      active: 'TabA'
    }
  },
  methods:{
    closePopup(name){
      this.showPopup =false;
      console.log(name, "name")
    }
  },
  provide() {
    return {
      username: this.name

    }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: "flex";
  justify-content: "center";
}

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;


}

.new {
  color: olivedrab;
}

.solid-out {
  color: red;
}
h4{
  color: orange;
}
</style>
