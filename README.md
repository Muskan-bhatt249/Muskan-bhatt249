<div align="center">
  <h1>
    <span id="typed-text"></span>
    <span class="cursor">|</span>
  </h1>
</div>

<style>
  /* Typing Effect */
  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  #typed-text {
    font-family: 'Courier New', monospace;
    font-size: 2em;
    color: #fff;
    white-space: nowrap;
    overflow: hidden;
    border-right: 3px solid;
    width: 0;
    animation: typing 3s steps(30) forwards, blink 0.75s step-end infinite;
  }

  .cursor {
    font-size: 2em;
    color: #fff;
    display: inline-block;
    margin-left: 2px;
    animation: blink 1s step-end infinite;
  }
</style>

<script>
  const typedText = "Hi, I'm Muskan-bhatt249";  // Change this to your desired text
  const speed = 100;  // Speed of typing in milliseconds

  let i = 0;
  function typeWriter() {
    if (i < typedText.length) {
      document.getElementById("typed-text").innerHTML += typedText.charAt(i);
      i++;
      setTimeout(typeWriter, speed);
    }
  }
  typeWriter();
</script>
