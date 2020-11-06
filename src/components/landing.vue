<template>
  <div class="landing">
    <div class="top">
      <div class="logo">
        <img src="../assets/subh-vivah-logo.png" height="100%" alt="">
      </div>
      <div class="weds curve">
        <p class="nm" style="text-align: left;">Viplaw</p>
        <p class="nm" style="text-align: center; font-size: 18px; color: #4361ee">with</p>
        <p class="nm" style="text-align: right">Saloni</p>
      </div>
    </div>
    <div class="n-elm n-ele-0 couple-pic">
      <div class="image"></div>
    </div>
    <div class="n-elm n-ele-in-0 mantra">
        वक्रतुण्ड महाकाय सूर्यकोटि समप्रभ।
        <br>
        निर्विघ्नं कुरु मे देव सर्वकार्येषु सर्वदा॥
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.landing {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .top {
    width: 100%;
    display: flex;
    justify-content: space-between;
    .logo {
      padding: 10px;
      height: 80px;
      margin: 10px;
      margin-bottom: 20px;
      border-radius: 4px;
    }
  }
  .weds {
    width: 150px;
    display: flex;
    padding: 15px;
    flex-direction: column;
    font-weight: bold;
    color: #f3722c;
    font-size: 24px;
    p{
      padding: 5px;
    }
  }
  .couple-pic {
    height: 200px;
    width: 200px;
    border-radius: 50%;
    padding: 15px;
    overflow: hidden;
    .image {
      height: 100%;
      width: calc(100% - 30px);
      background-image: url('../assets/ganesha.svg');
      background-repeat: no-repeat;
      background-size: cover;
    }
  }
  .mantra {
    padding: 1rem;
    margin: 10px;
    text-align: center;
  }
}
</style>
