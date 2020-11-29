<template>
  <div class="invitation">
    <div class="n-elm n-ele-in-0" style="padding: 15px; border-radius: 8px; position: relative">
      <div class="namste"></div>
      <div>
        <h1 class=" curve">Invitation</h1>
        <p class=" curve"><b>Mrs. Kanti Maurya W/o Late Sh. Radhey Shyam Maurya</b></p>
        <small>
          <p class="nm"><b>Add:</b> C-43, Parth City, Mehsana Gujarat -384001</p>
          <p class="nm">Cordially invites you to grace the wedding of there son</p>
        </small>
      </div>
    </div>
    <div class="n-elm n-ele-in-0" style="padding: 15px; border-radius: 8px;margin-top: 15px; position: relative">
      <div class="venue"></div>
      <div style="z-index: 10">
        <h1 class=" curve">Date & Venue</h1>
        <small>
          <p class="nm" style="color: #db0505;" >
            November <b> 30,2020 on 1:00PM </b> at Pushp Restaurant,
            Pusp Business Park Saradar Patel Ring Road,
            Opp Metro Station, Vastral, Ahmedabad, Gujarat -382418
          </p>
        </small>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.invitation {
  padding: 15px;
  text-align: center;
  color: #264653;
  .venue {
    position: absolute;
    top: 0px;
    left: 0px;
    bottom: 0px;
    right: 0px;
    z-index: 1;
    background-image: url('../assets/wedding-stage.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.15;
    border-radius: 8px;
  }
  .namste {
    position: absolute;
    top: 0px;
    left: 0px;
    bottom: 0px;
    right: 0px;
    z-index: 1;
    background-image: url('../assets/Namaste.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.15;
    border-radius: 8px;
  }
}
</style>
