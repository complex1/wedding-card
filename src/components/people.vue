<template>
  <div class="people">
    <div class="n-elm n-ele-in-0">
      <h3 class="nm">दर्शनाभिलाषी</h3>
      <p>Shubham Maurya</p>
    </div>
    <div class="n-elm n-ele-in-0">
      <h3 class="nm">स्वागतकांक्षी</h3>
      <p>Mr. & Mrs. Sonu Kumar Maurya</p>
      <p>Mr. & Mrs. Sumit Maurya</p>
      <p>Dheeraj, Sanidhya, Satvik</p>
    </div>
    <div class="n-elm n-ele-in-0">
      <h3 class="nm">विशेष आग्रह</h3>
      <p>Dheeraj, Sanidhya, Satvik</p>
    </div>
    <small>
        <b>
          Designed BY:
        </b>
        <span class="curve">Shubham Maurya</span>
    </small>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.people {
  & > div {
    margin: 15px 5px;
    padding: 10px;
    border-radius: 4px;
  }
  padding: 10px;
  h3 {
    color: #507f52;
  }
  p {
    margin: 0px;
    padding: 5px 15px;
    color: #1a4487;
    // font-weight: bold;
  }
  small {
    float: right;
  }
}
</style>
