<template>
  <div class="intro-wrap" @click="closeIntro">
    <h1>My Memo</h1> <br>
    <div class="intro-cont">
      <h1 class="intro-text">Click To me !</h1>
      <img :src="require('@/assets/images/intro.jpg')" />
    </div>
  </div>
</template>

<script>
export default {
  setup(props, context) {
    const closeIntro = () => {
      context.emit('closeintro');
    }
    return {
      closeIntro
    }
  }
}
</script>

<style scoped>
h1 {
  
    font-weight: 700;
    font-size: 60px;
    color: #321261;
}

  .intro-wrap {
    position: fixed;
    left: 0;
    top: 0;
    display: block;
    width: 100vw;
    height: 100vh;
    background-color: #fff;
    text-align: center;
    cursor: pointer;
  }

  .intro-text {
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translateX(-50%);
    font-weight: 700;
    font-size: 30px;
    color: #97bbf4;
  }

</style>