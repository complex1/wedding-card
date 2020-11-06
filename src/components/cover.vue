<template>
  <div class="cover">
    <div>
      <img src="../assets/subh-vivah-logo.png" width="110px" style="display: block;margin: auto" alt="">
    </div>
    <div class="cover-cont">
      <div>
        <div class=" family bride">
          <img class="n-elm n-ele-in-0 " src="../assets/groom-2.png" alt="">
          <div class="fadeInLeft">
             <b>Mr. Viplaw Maurya</b>
             <br>
             <small>Mrs Kanti Maurya W/o Late Sh. Radhey Shyam Maurya</small>
          </div>
        </div>
      </div>
      <img width="100px" class="n-elm n-ele-in-0" style="margin: 10px auto;padding: 5px;border-radius: 8px;" src="../assets/subh-vivah.png" alt="">
      <div>
        <div class="family groom">
          <div class="fadeInLeft">
             <b>Ms. Saloni Maurya</b>
             <br>
             <small>Daughter of Mr. & Mrs Madhuvan Maurya</small>
          </div>
          <img class="n-elm n-ele-in-0 " src="../assets/bride-2.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.cover {
  height: 100%;
  .cover-cont {
    padding: 15px;
    height: 100%;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .family {
      display: flex;
      & > div {
        flex-grow: 1;
        padding: 15px;
        box-shadow: inset 5px 5px 5px #b7b7b7, inset -5px -5px 4px #ffffff94;
        font-family: cursive;
        line-height: 16px;
      }
      img {
        height: 80px;
        width: 80px;
        padding: 5px;
        border-radius: 50%;
        margin: 0px 10px;
        border-radius: 50%;
      }
    }
  }
}
</style>
