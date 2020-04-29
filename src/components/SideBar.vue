<template>
  <div class="sidebar">
    <button class="sidebar__button" v-on:click="openPopup">Send Me The Tips</button>
  </div>
</template>

<script>
export default {
  name: 'SideBar',
  methods: {
    openPopup: function() {
      let popup = document.getElementById("popup");

      popup.classList.add("opened");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .sidebar {
    background-color: #f5f5f5;
    position: absolute;
    right: 20vw;
    top: 154px;
    max-width: 270px;
    height: 640px;

    &__button {
      position: relative;
      top: 64px;
      background: linear-gradient(90deg, #AC519C 0.83%, #E5424F 100%);
      box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5);
      color: #ffffff;
      font-size: 15px;
      line-height: 18px;
      text-align: center;
      padding: 11px 40px;
      margin: 0 24px;
    }
  }
    @media only screen and (max-width : 1386px) {
      .sidebar {
        right: 16vw;
      }
    }

    @media only screen and (max-width : 1280px) {
      .sidebar {
        right: 12vw;
      }
  }

  @media only screen and (max-width : 1200px) {
      .sidebar {
        right: 10vw;
      }
  }

   @media only screen and (max-width : 1024px) {
      .sidebar {
        right: 6vw;
      }
  }

  @media only screen and (max-width : 768px) {
      .sidebar {
        right: 2vw;
        max-width: 154px;

        &__button {
          font-size: 12px;
          line-height: 18px;
          padding: 11px 8px;
          margin: 0 12px;
        }
      }
  }

  @media only screen and (max-width : 412px) {
      .sidebar {
        position: relative;
        right: 5%;
        left: 5%;
        top: 32px;
        width: 90%;
        height: 426px;
        max-width: 100vw;
        margin-bottom: 32px;

        &__button {
          position: absolute;
          margin: 0;
          left: 50%;
          transform: translateX(-50%);
          padding: 11px 40px;
        }
      }
  }

</style>