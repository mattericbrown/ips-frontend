<template>
  <div class="popup closed" id="popup">
    <div class="form">
      <button class="form__close" v-on:click="close">X</button>
      <div class="form__wrapper">
      <p class="form__text">Step 1 of 2</p>
      <div class="form__divide"></div>
      <h2 class="form__header">Enter Your Email To Get <span class="form__header--green">Free</span> iPhone Photography Email Tips:</h2>
      <form @submit="checkForm" novalidate="true">
      <input id="email" v-model="email" type="email" name="email" class="form__input" required/>
      <span v-if="error" class="form__input--placeholder-invalid" id="invalid">Please enter a valid email address</span>
      <span v-if="!error" class="form__input--placeholder" id="valid">Please enter your email here</span>
      <button class="form__button" type="submit" value="Submit">Send Me The Tips » </button>
      </form>
    </div>
    
  </div>
</div>
</template>

<script>
export default {
  name: 'Popup',
  data() {
    return {
        error: false,
        email: null,
    }
},
  methods: {
    close: function() {
      let popup = document.getElementById("popup");

      popup.classList.add("closed");
      popup.classList.remove("opened")
    },
    checkForm: function(e) {

      if(!this.validEmail(this.email)){
        this.error = true;
        console.log("here")
      }
      
      e.preventDefault();
    },
    validEmail: function (email) {
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .popup {
    position: fixed;
    top: 0;
    width: 100vw;
    height: 100%;
    background: rgba(38,38,38,0.8)
  }

    .form {
      position: relative;
      z-index: 10;
      left: 50%;
      transform: translateX(-50%);
      top: 322px;
      width: 570px;
      height: 310px;
      background: #FFFFFF;
      box-shadow: 0px 0px 60px rgba(0, 0, 0, 0.5);
      opacity: 1;
      
      &__close {
        position: absolute;
        right: 11px;
        top: 11px;
        font-size: 16px;
        border: none;
      }

       &__wrapper {
        margin: 0 64px;
      }

      &__text {
        padding-top: 16px;
        font-weight: 300;
        font-size: 14px;
        line-height: 17px;
        color: #848484;
        text-align: center;
      }

      &__divide {
      width: 377px;
      margin: 0 0 24px 32px;
      height: 1px;
      border-bottom: 1px solid;
      border-image-source: linear-gradient(90deg, #AC519C 0.83%, #E5424F 50%, #E5E5E5 51%, #e5e5e5 100%);
      border-image-slice: 1;
      }

     

      &__input {
        position: relative;
        width: 356px;
        height: 54px;
        margin: 16px 32px 24px;
        font-weight: 300;
        padding-left: 16px;
        font-size: 18px;
        line-height: 22px;
        box-shadow: inset 0px 1px 5px rgba(142, 142, 142, 0.5);

        &:focus ~ &--placeholder,
        &:not(:focus):valid ~ &--placeholder {
          font-size: 12px;
          line-height: 14px;
          bottom: 144px;
        }
        
        &--placeholder {
          position: absolute;
          pointer-events: none;
          z-index: 0;
          bottom: 122px;
          left: 112px;
          font-size: 18px;
          line-height: 22px;
          color: #828282;
        }

        &--placeholder-invalid {
          position: absolute;
          pointer-events: none;
          z-index: 0;
          left: 112px;
          font-size: 12px;
          line-height: 14px;
          bottom: 144px;
          color: red;
        }
      }

      &__header {
        text-align: center;
        margin: 0 32px;

        &--green {
          text-transform: uppercase;
          color: green;
        }
      }
      &__button {
        margin: 0 32px;
        width: 377px;
        background: linear-gradient(90deg, #AC519C 0.83%, #E5424F 100%);
        box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5);
        color: #ffffff;
        font-size: 15px;
        line-height: 18px;
        text-align: center;
        padding: 11px 40px;

        &:hover {
          background: linear-gradient(90deg, #B678AA 1.29%, #E28990 100%);
        }
      }
    }

    .closed {
      display: none;
    }

    .opened {
      display: block;
    }

    @media only screen and (max-width : 400px) {
        .form {
          width: 90%;
          top: 130px;
          
          &__wrapper {
            margin: 0;
          }

          &__header {
            font-size: 20px;
            line-height: 26px;
          }

          &__input {
          position: relative;
          width: 80%;
          height: 54px;
          margin: 16px 24px 24px;
          font-weight: 300;
          padding-left: 16px;
          font-size: 18px;
          line-height: 22px;
          box-shadow: inset 0px 1px 5px rgba(142, 142, 142, 0.5);

          &:focus ~ &--placeholder,
          &:not(:focus):valid ~ &--placeholder {
            font-size: 12px;
            line-height: 14px;
            bottom: 144px;
          }
          
          &--placeholder {
            position: absolute;
            pointer-events: none;
            z-index: 0;
            bottom: 102px;
            left: 42px;
            font-size: 18px;
            line-height: 22px;
            color: #828282;
          }

          &--placeholder-invalid {
            position: absolute;
            pointer-events: none;
            z-index: 0;
            left: 42px;
            font-size: 12px;
            line-height: 14px;
            bottom: 144px;
            color: red;
          }
        }

        &__button {
          margin: 0 24px;
          width: 90%;
          background: linear-gradient(90deg, #AC519C 0.83%, #E5424F 100%);
          box-shadow: 0px 3px 10px rgba(104, 104, 104, 0.5);
          color: #ffffff;
          font-size: 15px;
          line-height: 18px;
          text-align: center;
          padding: 11px 40px;

          &:hover {
            background: linear-gradient(90deg, #B678AA 1.29%, #E28990 100%);
          }
        }
      }

    }

</style>