<template >
  <section class="main">
    <br /><br /><br /><br />
    <div>
      <h2 class="titles">BiZUp</h2>
      <h4 class="subtitle">A one stop solution to all your business needs</h4>
      <div class="links">
        <u class="txt">New user?</u>

        <NLink to="/user/register" class="button--green">Register</NLink>&emsp;
        <u class="txt">Already a user?</u>
        <NLink to="/user/login" class="button--grey">Login</NLink>
      </div>
    </div>
  </section>
</template>
<script>
export default {};
</script>

<style scoped>
.main {
  height: 100vh;
  min-width: 100% !important;
  background: white;
  background-repeat: no-repeat;
  background-size: 100% !important;
  background-blend-mode: blend;
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 400;
  font-size: 100px;
  color: #2E495E;
  letter-spacing: 1px;
  font-size: 6em;
}
.green {
  color: #00C48D;
}

.subtitle {
  font-weight: 300;
  font-size: 3em;
  color: #2E495E;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
* {
  font-family: Roboto;
}
.titles {
  font-style: normal;
  font-weight: normal;
  font-size: 120px;
  line-height: 160px;
  text-align: center;

  color: #FFFFFF;

  backdrop-filter: blur(4px);
}
.subtitle {
  font-style: normal;
  font-weight: normal;
  font-size: 36px;
  line-height: 42px;
  text-align: center;

  color: #FFFFFF;
}
.txt {
  display: inline-block;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  text-align: justify;
  text-decoration-line: underline;

  color: #FFFFFF;
}
</style>
