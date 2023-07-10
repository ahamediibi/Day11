<!DOCTYPE html>
<html>
<head>
  <title>Countdown Timer</title>
  <style>
    body{
        background-color:black;
    }
    #countdown {
        color:black;
        text-shadow:5px 5px 25px blueviolet,25px 25px 50px blueviolet;
        font-size: 180px;
        font-weight: bold;
        text-align: center;
        margin: auto;
    }
    #startButton{
        color:black;
        background-color: black;
        text-shadow: 2px 2px 5px blueviolet;
        box-shadow: 2px 2px 5px blueviolet;
        font-size: 20px;
        font-weight: bold;
        width:20%;
        margin-top:140px;
        margin-right:30px;
        height:30px;
        float:right;
    }
  </style>
</head>
<body>
  <button id="startButton">Start Countdown</button>
  <div id="countdown"></div>
  <audio id="countdownSound" src="mixkit-female-microphone-countdown-341.wav" autoplay></audio>
  <script>
    function startTimer(duration, callback) {
      setTimeout(function () {
        callback();
      }, duration);
    }

    function playSound() {
      var audio = document.getElementById("countdownSound");
      audio.play();
    }

    document.getElementById("startButton").addEventListener("click", function () {
      playSound();
      startTimer(1000, function () {
        document.getElementById("countdown").textContent = "10";
        playSound();
        startTimer(1000, function () {
          document.getElementById("countdown").textContent = "9";
          playSound();
          startTimer(1000, function () {
            document.getElementById("countdown").textContent = "8";
            playSound();
            startTimer(1000, function () {
              document.getElementById("countdown").textContent = "7";
              playSound();
              startTimer(1000, function () {
                document.getElementById("countdown").textContent = "6";
                playSound();
                startTimer(1000, function () {
                  document.getElementById("countdown").textContent = "5";
                  playSound();
                  startTimer(1000, function () {
                    document.getElementById("countdown").textContent = "4";
                    playSound();
                    startTimer(1000, function () {
                      document.getElementById("countdown").textContent = "3";
                      playSound();
                      startTimer(1000, function () {
                        document.getElementById("countdown").textContent = "2";
                        playSound();
                        startTimer(1000, function () {
                          document.getElementById("countdown").textContent = "1";
                          playSound();
                          startTimer(1000, function () {
                            document.getElementById("countdown").textContent = "Happy Independence Day!";
                            playSound();
                          });
                        });
                      });
                    });
                  });
                });
              });
            });
          });
        });
      });
    });
  </script>
</body>
</html>
