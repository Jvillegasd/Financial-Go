<template>
  <div class="flex flex-col h-screen justify-center items-center">

      <div id="title" class="mb-10">
        <img id="image" src="../assets/logo.svg" class="block mx-auto">
        <a id="landing_redirect" class="text-5xl font-regular text-white text-center" href="/">Financial Go</a>
      </div>
  
      <div id="card" class="mb-20 text-center xs:w-full sm:w-full md:w-c-507">
        <h1 class="text-4xl font-regular">Login</h1>

        <div class="mb-2">
          <Textbox
            label="Email"
            :width=360
            :labelFontSize=20
            :inputFontSize=25
            class="mx-auto mb-12">
          </Textbox>

          <div class="grid grid-cols-2 mb-8 mx-auto" style="width: 360px;">
            <Textbox
              label="Password"
              :width=245
              :labelFontSize=20
              :inputFontSize=25
              :isPassword=true
              class="mx-auto">
            </Textbox>

            <ArrowButton class="ml-28">
            </ArrowButton>
          </div>
        </div>

        <div>
          <p class="font-regular" style="font-size: 20px;">
            Don't have an account? <a href="/sign_up" class="text-blue" id="sign_up">Sign up</a>
          </p> 
        </div>

      </div>
  </div>

</template>

<script>
  import Textbox from '../components/Textbox/Textbox';
  import ArrowButton from '../components/Buttons/Arrow_btn';

  export default {
    name: 'Sign-in',
    components: {
      Textbox,
      ArrowButton
    },
    beforeCreate: function() {
      document.body.className = 'sign_in';
    }
  }
</script>

<style scoped>
  #card {
    background-color: white;
    height: 449px;
    border-radius: 53px;
    margin-top: 0px;
  }
  
  #card > h1 {
    padding: 44px;
  }
  
  #image {
    width: 119.03px;
    height: 93.36px;
  }

  #landing_redirect {
    display: block;
    width: 300px;
  }
</style>