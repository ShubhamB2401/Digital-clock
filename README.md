<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital clock using javaScript</title>
    <style>
        *{
            padding: 0px;
            margin: 0px;
            font-family: Arial, Helvetica, sans-serif;
            box-sizing: border-box;
            
        }
        .hero{
            width: 100%;
            min-height: 100vh;
            background: linear-gradient(45deg, #08001f, #30197d);
            color: #fff;
            position: relative;
        }
        .container{
          width: 800px;
          height: 180px;
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }
        .clock{
            height: 100%;
            width: 100%;
            background: rgba(235, 0, 255, 0.11);
            display: flex;
            align-items: center;
            border-radius: 10px;
            justify-content: center;
            backdrop-filter: blur(40px);

        }
        .container::before{
            content: '';
            width: 180px;
            height: 180px;
            background: #f41b75;
            border-radius: 5px;
            position: absolute;
            left: -50px;
            top: -50px;
            z-index: -1;
        }
        .container::after{
            content: '';
            width: 180px;
            height: 180px;
            background: #419aff;
            border-radius: 50%;
            position: absolute;
            right: -30px;
            bottom: -50px;
            z-index: -1;
        }
        .clock span{
            font-size: 80px;
            width: 110px;
            display: inline-block;
            text-align: center;
            position: relative;
        }
        .clock span::after{
            font-size: 16px;    
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
        }
        #hrs::after{
            content:'HOURS';
        }
        #min::after{
            content:'MIN';
        }
        #sec::after{
            content:'SEC';
        }
    </style>
</head>
<body>
    <div class="hero">
       <div class="container">
        <div class="clock">
            <span id="hrs">00</span>
            <span>:</span>
            <span id="min">00</span>
            <span>:</span>
            <span id="sec">00</span>
        </div>
       </div>
    </div>

    <script>
        let hrs = document.getElementById("hrs")
        let  = document.getElementById("min")
        let  = document.getElementById("sec")
       
        setInterval(()=>{
            let currentTime = new Date();

hrs.innerHTML = currentTime.getHours();
min.innerHTML = currentTime.getMinutes();
sec.innerHTML = currentTime.getSeconds();   
        },1000)

     

    </script>
</body>
</html>
