<!doctype html>
<html>

<head>
  <link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:200" rel="stylesheet">
  <meta http-equiv="refresh" content="30">
  <style>
    body {
      background-image: url('https://source.unsplash.com/category/nature/1600x900');
      background-size: cover;
      min-height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: top;
      font-size: 30px;
    }

    h1 {
      background-color: rgba(255, 255, 255, 0.3);
      padding: 0.3rem;
      color: rgb(0, 0, 0);
      font-family: 'Source Sans Pro', sans-serif;
      font-weight: 200;
    }

    #ViewTimer{
      <!-- background-color: white; -->
      align-items: top;
    };
  </style>
</head>

<body>

  <div id="ViewTimer"></div>

  <script language="JavaScript">
    var SetTime = 30;

    function msg_time() { 

      m = Math.floor(SetTime % 60) + "초";

      var msg = "현재 남은 시간은 <font color='red'>" + m + "</font> 입니다.";

      document.all.ViewTimer.innerHTML = msg;

      SetTime--;

    }

    window.onload = function TimerStart() {
      tid = setInterval('msg_time()', 1000)
    };
  </script>
</body>

</html>
