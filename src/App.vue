<template>
  <div id="app1">
    <v-card style="z-index: 3">
      <v-layout>
        <!-- <v-system-bar color="deep-purple darken-3"></v-system-bar> -->

        <v-app-bar color="primary" prominent>
          <v-app-bar-nav-icon
            variant="text"
            @click.stop="drawer = !drawer"
          ></v-app-bar-nav-icon>

          <v-toolbar-title>My files</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn variant="text" icon="mdi-magnify"></v-btn>

          <v-btn variant="text" icon="mdi-filter"></v-btn>

          <v-btn variant="text" icon="mdi-dots-vertical"></v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" location="bottom" temporary>
          <v-list :items="items"></v-list>
        </v-navigation-drawer>
      </v-layout>
    </v-card>

    <aside class="asidearea">
      <v-text class="asidetext"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic
        cupiditate sed nostrum, recusandae ullam enim facilis minus repellat eos
        ut dicta saepe debitis! Voluptates accusantium explicabo ex dicta quos
        voluptatem facilis deserunt nostrum itaque, earum nobis voluptas
        laudantium! Non, corporis inventore aliquid eius eum beatae quibusdam
        quos saepe. Delectus perspiciatis ad molestiae vel autem cumque suscipit
        voluptas quos atque sapiente? Deserunt voluptas sequi saepe deleniti
        distinctio delectus omnis aliquid neque quia, iste, explicabo quis
        fugiat, vero vitae quod repudiandae numquam molestiae eos inventore
        suscipit sint officiis! Numquam, minima sapiente? Dolores nesciunt quo
        sequi, ducimus rem alias dolore distinctio! Alias, corrupti?</v-text
      >
    </aside>
    <div id="kolon1">
      <v-card v-for="(item, index) in items" :key="index" class="box" :id="item.id" style="{ order: index + 1 }">
        <v-card class="innercard">
          <v-img
            :width="100"
            aspect-ratio="9/9"
            cover
            :src="item.imageUrl"
            class="inner-img"
          ></v-img>
        <v-card-text>
            {{ item.text }}
        </v-card-text>
        </v-card>
      </v-card>
    </div>
    <v-card class="rightdiv">date:01.02.2000</v-card>
  </div>
</template>
<script setup>
import HelloWorld from "./components/HelloWorld.vue";
const items = [
  { id: "mor", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg" },
  { id: "pembe", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg"  },
  { id: "sari", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg" ,text:"erfıroeg" },
  { id: "mor", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg"  },
  { id: "pembe", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg"  },
  { id: "sari", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg"  },
  { id: "mor", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg"  },
  { id: "pembe", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg" },
  { id: "sari", imageUrl: "https://cdn.britannica.com/68/172968-050-13BEB8E0/Tom-Ford-mix-textures-patterns-collection-Pop-art-February-2013.jpg",text:"erfıroeg"  },

  // Diğer öğeler
];
var sira=1;
</script>

<style scoped>
.v-img{
  opacity:1 !important;
  z-index:2;
}
.innercard{
  z-index: 1;
  width:80%; height:80%;
  opacity: 0.5;
  padding: 1rem;
  
}
#app1 {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  width: 100vw;
  height: 100vh;
  overflow: auto;
}
.asidearea {
  margin-top: 62px;
  grid-column: 1;
  background-color: #fafafa;
  font-size: 2rem;
  padding: 10%;
  overflow-y: auto;
}
#kolon1 {
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
  grid-column: 2;
  justify-content: space-between;
}
#kolon1 :last-child {
  margin-bottom: 100px;
}
.box:first-child {
  margin-top: 70px;
}
.box {
  margin-right: 2rem;
  margin-left: 2rem;
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  align-items:center ;
  height: 200px;
}
.v-card {
  overflow: visible;
}
#mor {
  box-shadow: rgba(0, 0, 0, 0.2) 0px 60px 40px -7px;
  background: #da22ff; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #9733ee,
    #da22ff
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #9733ee,
    #da22ff
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
 
}
#pembe {
  box-shadow: rgba(0, 0, 0, 0.2) 0px 60px 40px -7px;
  background: #ec008c; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #fc6767,
    #ec008c
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #fc6767,
    #ec008c
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

  
}
#sari {
  box-shadow: rgba(0, 0, 0, 0.2) 0px 60px 40px -7px;
  background: #ffe259; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #ffa751,
    #ffe259
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #ffa751,
    #ffe259
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
.rightdiv {
  margin-top: 6rem;
  background-color: palevioletred;
  height: 200px;
  grid-column: 3;
}
.asidetext {
  overflow-wrap: break-word;
  word-wrap: break-word;
  overflow: hidden;
}
</style>
