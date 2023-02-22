<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- displays site properly based on user's device -->

  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&display=swap" rel="stylesheet">

  <title>Frontend Mentor | Product preview card component</title>

  <!-- Feel free to remove these styles or customise in your own stylesheet 👍 -->
  <style>
    body {
      margin: 100px auto 100px auto;
      background-color: hsl(30, 30%, 92%);
    }

    h1 {
      color: hsl(212, 21%, 14%);
      font-family: 'Fraunces', sans-serif;
      line-height: 1;
    }

    h2 {
      color: hsl(240, 3%, 57%);
      font-family: 'Montserrat', sans-serif;
      font-weight: 400;
      text-transform: uppercase;
      font-size: 12px;
      letter-spacing: .3rem;
    }


    #big-number {
      font-family: 'Fraunces', sans-serif;
      color: hsl(158, 36%, 37%);
      font-size: 32px;
      padding-bottom: 40px;
    }

    #number {
      font-family: 'Montserrat', sans-serif;
      color: hsl(240, 3%, 57%);
      font-size: 14px;
      margin: 15px;
      padding: 0px 0px 5px 16px;
      text-decoration: line-through;
      padding-bottom: 40px;
    }


    #perfume {
      text-transform: uppercase;
    }

    p {
      font-family: 'Montserrat', sans-serif;
      color: hsl(240, 3%, 57%);
      font-size: 14px;
      line-height: 1.4rem;
      font-weight: 400;
      padding-bottom: 10px;
    }

    .attribution {
      font-size: 11px;
      text-align: center;
      margin: 10px auto 0px auto;
    }

    .attribution a {
      color: hsl(228, 45%, 44%);
    }

    .container {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: auto;
      grid-template-areas:
        "box1 box2";
      max-width: 600px;
      height: 450px;
      margin: 0px auto 0px auto;
      

    }

    .box1 {
      grid-area: "box1";
      background-image: url(https://i.ibb.co/dLspbwX/image-product-desktop.jpg);
      background-size: contain;
      background-repeat: no-repeat;
      border-top-left-radius: 10px;
      border-bottom-left-radius: 10px;
    }

    .box2 {
      grid-area: "box2";
      background-color: hsl(0, 0%, 100%);
      text-align: left;
      padding: 30px;
      border-top-right-radius: 10px;
      border-bottom-right-radius: 10px;
    }

    .btn {
      -webkit-border-radius: 6;
      -moz-border-radius: 6;
      border-radius: 6px;
      font-family: 'Montserrat', sans-serif;
      color: #ffffff;
      font-size: 14px;
      background: hsl(158, 36%, 37%);
      padding: 13px 60px 13px 60px;
      text-decoration: none;


    }

    .btn:hover {
      background: hsl(158, 38%, 32%);
      text-decoration: none;
    }
    @media screen and (max-width:750px) {
      body {
      margin: 40px auto 100px auto;
      background-color: hsl(30, 30%, 92%);
    }

      .container {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;
      grid-template-areas:
        "box1"
        "box2";
      
      height: 680px;
      width: 400px;
      
    }
    .box1 {
      grid-area: "box1";
      background-image: url(https://i.ibb.co/HDcFY6X/image-product-mobile.jpg);
      background-size: 400px;
      background-repeat: no-repeat;
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
      border-bottom-left-radius: 0px;
      border-bottom-right-radius: 0px;
      width: 400px;
      height: 280px;
    }
    .box2 {
      grid-area: "box2";
      background-color: hsl(0, 0%, 100%);
      text-align: left;
      padding: 30px;
      border-top-right-radius: 0px;
      border-bottom-left-radius: 10px;
      border-top-left-radius: 0px;
      border-bottom-right-radius: 10px;
      width: 340px;
      height: 370px;
    }
    h1 {
      color: hsl(212, 21%, 14%);
      font-family: 'Fraunces', sans-serif;
      line-height: 1;
      width: 300px;
    }
    p {
      font-family: 'Montserrat', sans-serif;
      color: hsl(240, 3%, 57%);
      font-size: 14px;
      line-height: 1.4rem;
      font-weight: 400;
      padding-bottom: 10px;
      width: 310px;
    }
    .btn {
      -webkit-border-radius: 6;
      -moz-border-radius: 6;
      border-radius: 6px;
      font-family: 'Montserrat', sans-serif;
      color: #ffffff;
      font-size: 14px;
      background: hsl(158, 36%, 37%);
      padding: 13px 110px 13px 110px;
      text-decoration: none;
    
    }
    .attribution {
      font-size: 11px;
      text-align: center;
      margin: 50px auto 0px auto;
    }
    }
  </style>
</head>

<body>
  <div class="container">
    <div class="box1"></div>

    <div class="box2">
      <h2>Perfume</h2>
      <h1>Gabrielle Essence Eau De Parfum</h1>
      <p>A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of
        <span id="perfume">Chanel</span>.
      </p>
      <table>
        <tr class="table">
          <td id="big-number">$149.99</td>
          <td id="number">$169.99</td>
        </tr>
      </table>
      <a class="btn" href="#"><img src="https://i.ibb.co/3yyZX0p/icon-cart2.png" alt="icon-cart"> <span
          style="padding-left: 10px; padding-top: 10px;">Add to Cart</span></a>

    </div>
  </div>

  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
    Coded by <a href="https://www.frontendmentor.io/profile/moistmike101">Michael Doratt</a>.
  </div>
</body>
<!--
<a href="https://imgbb.com/"><img src="https://i.ibb.co/3yyZX0p/icon-cart2.png" alt="icon-cart2" border="0"></a>
<a href="https://ibb.co/yYmkhcK"><img src="https://i.ibb.co/dLspbwX/image-product-desktop.jpg" alt="image-product-desktop" border="0"></a>
<a href="https://ibb.co/C5j1vgW"><img src="https://i.ibb.co/HDcFY6X/image-product-mobile.jpg" alt="image-product-mobile" border="0"></a>
<a href="https://ibb.co/C5j1vgW"><img src="https://i.ibb.co/HDcFY6X/image-product-mobile.jpg" alt="image-product-mobile" border="0"></a>

-->
</html>
