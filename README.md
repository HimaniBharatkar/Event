
<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width initial-scale=1.0">
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event_Page</title>
    <link rel="stylesheet" href="E_style.css">
    <style>
      body{
        text-align: center;
        
        font-weight: 100;
      }
      #clock{
        display: inline-block;
        color: #fff4f4;
        font-weight: 100;
        font-size: 30px;
      }
      #clock div.B{
        padding: 15px;
        display: inline-block;
        border-radius: 2px;
        background-color: #5e441f transparent;
        border: 1px solid white;
      }
      .smalltext{
        border: none;
        padding-top: 5px;
        font-size: 15px;
      }
    </style>
</head>
<body>
  
    <header>
      <nav id="topnav">
        
        <ul>
          <li><a href="#" class="home">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Photos</a></li>
          <li><a href="#">Events</a></li>
          <li><a href="#">Locations</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">RSVP</a></li>
        </ul>
      </nav>
        <p>Craving the Summer heat and beats </p>
        <h1>#theMusicModeOn</h1>
        <div id="clock">
        <div class="B">
          <span class="days" id="day"></span>
          <div class="smalltext">Days</div>
        </div>
        <div class="B">
          <span class="hours" id="hour"></span>
          <div class="smalltext">Hours</div>
        </div>
        <div class="B">
          <span class="minutes" id="minute"></span>
          <div class="smalltext">Minutes</div>
        </div>
        <div class="B">
          <span class="seconds" id="second"></span>
          <div class="smalltext">Seconds</div>
        </div>
      </div>

        <p id="demo"></p>
        <script>
          var countDownDate=new Date("October 2, 2023 12:00:00").getTime();
          var x=setInterval(function()
          {
            var now=new Date().getTime();
            var distance= countDownDate-now;
            
            var days=Math.floor(distance/(1000*60*60*24));
            var hours= Math.floor((distance%(1000*60*60*24))/(1000*60*60));
            var minutes=Math.floor((distance%(1000*60*60))/(1000*60));
            var seconds=Math.floor((distance%(1000*60))/1000)

            document.getElementById("day").innerHTML=days;
            document.getElementById("hour").innerHTML=hours;
            document.getElementById("minute").innerHTML=minutes;
            document.getElementById("second").innerHTML=seconds;
            if(distance<0){
              clearInterval(x);
              document.getElementById("demo").innerHTML="Event Over..!";
              document.getElementById("day").innerHTML="Event Over..!";
              document.getElementById("hour").innerHTML="Event Over..!";
              document.getElementById("minute").innerHTML="Event Over..!";
              document.getElementById("second").innerHTML="Event Over..!";
            }
            document.getElementById("demo").style.fontSize="40px";
          },1000);
        </script>
        
        
        <button>Register Now</button>  
      </header>
      <footer>
      <nav class="footernav">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Locations</a></li>
          <li><a href="#">RSVP</a></li>
        </ul>
      </nav>
        <p>&copy; - Copyright 2004</p>
      </footer>
</body>
</html>
