<template>
  <div>
    <h1> {{ title }}</h1>
    <div class="container">
      <div>
        <div class="bigBox" v-for="boxY in 10" v-bind:key="boxY">
          <div class="box" v-for="boxX in 10" v-bind:key="boxX" >
            <NewBox v-bind:box-x="boxX" v-bind:box-y="boxY"></NewBox>
          </div>
        </div>
      </div>
      <div class="shipsInBox">
        <div class="ship" v-for="ship in ships" v-bind:key="ship.shipId">
          Name: {{ship.shipName}}
          <br>
          Size: {{ship.shipSize}}
        </div>
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
      square: [
        {
          boxX: null,
          boxY: null,
          wasHit: false,
          hasShip: false,
          shipId: null,
        }
      ],
      ships: [
        {
          shipId: 1,
          shipSize: 5,
          shipName: "Aircraft carrier"
        },
        {
          shipId: 2,
          shipSize: 4,
          shipName: "Cruiser"
        },
        {
          shipId: 3,
          shipSize: 3,
          shipName: "Destroyer"
        },
        {
          shipId: 4,
          shipSize: 3,
          shipName: "Submarine"
        },
        {
          shipId: 5,
          shipSize: 2,
          shipName: "Torpedo boat"
        },
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
  align-items: center;
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

.container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: row;

}

.shipsInBox {
  display: flex;
  flex-direction: column;
}

.ship {
  color: aqua;
  background-color: black;
  border: 1px greenyellow solid;
}

</style>