#Event

  header {
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),url("https://temporarypowersolutionsuk.files.wordpress.com/2016/05/music-fest.jpg");
    font-family: 'Dancing Script', cursive;
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    
  }
  header h1{
    text-align: center;
    color: #ffffff;
    font-size: 15vh;
    margin-top: 2px;
  }
  header p{
    font-size: 25px;
    margin-top: 2px;
    text-align: center;
    color: #ffffff;
  }
  header button{
    background: transparent;
    color:#d3a566 ;
    box-shadow:  -1px -1px 2px #cca152, 1px 1px 2px rgba(150, 112, 42, 0.856);
    font-size: 25px;
    cursor: pointer;
    margin: 20px;
    text-align: center;
    position: relative;
    left: 0%;
    border-radius: 5px;
    font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; 
  }
  button:hover{
    background-color: #4b3618;
    color: #fffcfc;
  }
  #topnav p{
    font-size: 20px;
    padding: 10px 5px;
    color: #ffffff;
  }
  #topnav{
    font-family: 'Dancing Script', cursive;
    font-size: 20px;
    width: 100%;
    height: 100px;
    margin: 0px ;
  }
  #topnav ul{
    
    margin: 0px;
    text-align: right;
  }
  #topnav ul li{
    list-style-type: none;
    display: inline;
    
  }
  #topnav ul li a{
    color: #b6843f;
    text-decoration: none;
    margin: 6px 5px;
    padding: 10px 15px;
    margin-top: 0px;
    
  }
  #topnav ul li a:hover{
    color: #ffffff;
    border-bottom: 3px solid #f1f0f0;
    transition: 50ms linear 2s ease;
    -moz-transition: 50ms linear 0s;
    -webkit-transition: 50ms linear 0s;
  }
  body{
    background-color: black;
    
  }
  #content{
    font-family: 'Lora', serif;
  }
  #content h1, h2, h3, h4, h5, h6{
    color: #c3cadb;
    text-align: center;
    font-family: 'Dancing Script', cursive;
  }
  
  #content img{
    display: inline;
    margin-left: auto;
    margin-right: auto;
  }
  .pic{
    margin-left: 10vh;
    padding-right: 5px;
    display: block;
  }
  img{
    
    height: 45vh;
    width: 60vh;
  }
  footer{
    border-top: 10px solid #975d27;
    width: 100%;
    margin: 0px auto;
  }
  footer p{
    color: #7a5d33;
    float: right;
    padding-top: 5px;
    padding-right: 0px;
    padding-bottom: 5px;
    padding-left: 0px;
    margin: 0px;
    font-family: 'Lora', serif;
  }
  .footernav{
    padding-top: 5px;
    padding-left: 0px;
    float: left;
  }
  .footernav ul{
    margin: 0px;
    padding: 2px 4px;
  }
  .footernav ul li{
    list-style-type: none;
    display: inline;
    padding: 2px 10px;
    margin-right: 20px;
  }
  .footernav ul li a:link, .footernav ul li a:visited{
    color: #5e441f;
    text-decoration: none;
    font-family: 'Dancing Script';
  }
  .footernav ul li a:hover{
    color: #fffcfc;
  } 
  

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
