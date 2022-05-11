<template>
  <div class="principal">
    <section class="container">
      <div class="box">
        <div class="star-circle">
          <!-- <img src="../assets/icon-star" alt="estrela" /> -->
        </div>
        <div class="title">How did we do?</div>
        <div class="card-info">
          Please let us know how we did with your support request. All feedback
          is appreciated to help us improve our offering!
        </div>

        <div class="circle" @click="handleRating">1</div>
        <div class="circle" @click="handleRating">2</div>
        <div class="circle" @click="handleRating">3</div>
        <div class="circle" @click="handleRating">4</div>
        <div class="circle" @click="handleRating">5</div>

        <div class="btn" @click="handleChange">SUBMIT</div>
      </div>
    </section>
    <div @click="handleCloseModal">
      <ThankYouComponent v-if="openModal" />
    </div>
  </div>
</template>

<script>
import ThankYouComponent from "./ThankYouComponent.vue";

export default {
  components: {
    ThankYouComponent,
  },
  data() {
    return {
      mainMenu: true,
      openModal: false,
    };
  },
  methods: {
    handleRating() {
      console.log("clicou aqui");
    },
    handleChange() {
      this.openModal = true;
      console.log("abrir");
    },
    handleCloseModal() {
      this.openModal = false;
    },
    handleCloseMenu() {
      this.mainMenu = false;
      console.log("giovana o forninho caiu");
    },
  },
};
</script>

<style scoped>
* {
  font-family: "Overpass", sans-serif;
}

.principal {
  width: 100vw;
  height: 100vh;
  background: #141519;
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  width: 320px;
  height: 400px;
  background: #222933;
  border-radius: 30px;
}

.star-circle {
  border-radius: 50%;
  width: 15px;
  height: 15px;
  padding: 10px;
  margin-left: 20px;
  margin-top: 30px;
  margin-bottom: 30px;
  display: inline-block;
  background: #262d37;
}

.title {
  color: #e7eaec;
  font-family: "Overpass", sans-serif;
  font-size: 30px;
  margin-left: 20px;
  padding-bottom: 10px;
}

.card-info {
  color: #e7eaec;
  font-family: "Overpass", sans-serif;
  font-size: 0.874rem;
  line-height: 1.5;
  opacity: 0.5;
  margin-left: 20px;
  padding-bottom: 50px;
  margin-right: 40px;
}

.circle {
  border-radius: 50%;
  width: 15px;
  height: 15px;
  padding: 10px;
  margin-left: 20px;
  display: inline-block;
  background: #262d37;
  color: #e7eaec;
  text-align: center;
}

.circle.active {
  background-color: hsl(25, 97%, 53%);
}

.circle:hover {
  border-radius: 50%;
  width: 15px;
  height: 15px;
  padding: 10px;
  margin-left: 20px;
  display: inline-block;
  transition: 0.5s;
  opacity: 0.7;
  color: #e7eaec;
  text-align: center;
}

.btn {
  background-color: hsl(25, 97%, 53%);
  color: #e7eaec;
  margin-top: 30px;
  margin-left: 30px;
  margin-right: 30px;
  text-align: center;
  border-radius: 50px;
  padding-top: 10px;
  padding-bottom: 10px;
  font-weight: 700;
  font-family: "Overpass", sans-serif;
}
</style>
