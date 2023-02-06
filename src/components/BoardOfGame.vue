<template>
  <div>
    <h1> {{ title }}</h1>
    <div class="bigBox" v-for="boxX in 10" v-bind:key="boxX">
      <div class="box" v-for="boxY in 10" v-bind:key="boxY" >
        <NewBox v-bind:box-x="boxX" v-bind:box-y="boxY"></NewBox>
      </div>
    </div>
  </div>
</template>

<script>
import NewBox from "@/components/NewBox";
export default {
  name: "BoardOfGame",
  data: function () {
    return {
      title: "Board of the game",
      boxes: [

      ],
      cases: [
        {
          hasShip: false,
          shipId: null,
          wasHit: false,
          boxX: null,
          boxY: null,
        }
      ]
    };
  },
  components: {
    NewBox
  }

}
</script>

<style scoped>
.bigBox {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.box {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: royalblue;
  color: black;
  height: 50px;
  width: 50px;
  border: 1px solid black;
}
</style>