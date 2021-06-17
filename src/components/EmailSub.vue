<template>
  <div id="email-sub">
    <span>Get information and special offer from Natural Farm</span>
    <input type="text" name="email sub" />
    <button>Subcribe</button>
  </div>
</template>

<script>
</script>

<style scoped>
#email-sub {
  text-align: center;
  margin-top: 20px;
  padding: 20px;
  background: ghostwhite;
  border-top: 1px solid gainsboro;
}

#email-sub span {
  font-size: 13px;
  padding-right: 10px;
}

#email-sub input {
  border: 1px solid gainsboro;
  margin-right: 10px;
  height: 40px;
  width: 250px;
  border-radius: 3px;
}

input[type=text]:focus {
  outline: 1px solid royalblue;
  border-radius: 3px;
}

#email-sub button {
  padding: 11px 20px;
  background: var(--primary-color);
  border: none;
  color: white;
  font-size: 16px;
  border-radius: 3px;
}
</style>
