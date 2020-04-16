<template>
  <div class="password-protect" v-if="$props.blocked">
    <form>
      <label for="pass">Enter password</label>
      <div>
        <input type="password" id="pass" name="password" required>
        <button>Let me in.</button>
      </div>
      <p :class="{show: $props.tried}">Incorrect, please try again</p>
    </form>
  </div>
</template>

<script>

  export default {

    data: function () {
      return {

      }
    },
    props: {
     blocked: Boolean,
     tried: Boolean
    },
    components: {
    },
    mounted: function() {
      var that = this;

      document.querySelector('form').addEventListener('submit', function(e){
        var val = document.querySelector('input').value;
        e.preventDefault();
        that.$emit('enterPassword', val);
      });
    }
  }
</script>

<style scoped>

.password-protect {
  position: fixed;
  height: 100vh;
  width: 100vw;
  background: #F2F2F2;
  z-index: 100;
}

form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  max-width: 300px;
  margin: 0 auto;
}

div {
  width: 100%;
  display:flex;
}

label {
  font-size: 20px;
  font-family: 'Roboto-bold', sans-serif;
  margin: 0 0 10px;
}

input {
  width: 70%;
  height: 40px;
  font-size: 20px;
  padding: 0 0 0 10px;
  margin: 0;
  border: 1px solid #A0A0A0;
}

input:focus {
  outline: none;
}

button {
  width: 30%;
  padding: 0;
  margin: 0;
  border: 1px solid #A0A0A0;
  border-left: none;
  cursor: url(../images/hover.png), pointer; 
}

p {
  margin: 10px 0 0 0;
  font-size: 12px;
  opacity: 0;
  transition: opacity .5s ease;
}

p.show {
  opacity: 1;
}
  
</style>
