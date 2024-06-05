# -codeAlpha_ImageGallery
#Task-1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>#Task-1|| Image-Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="complete-img" id="firstBox">
        <img src="photos/img1.jpg" id="first">
        <span onclick="closeFullImg()">X</span>
    </div>
    <div class="img-gallery">
        <img src="photos/img1.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img3.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img2.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img4.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img5.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img6.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img7.jpg"onclick="openFullImg(this.src)">
        <img src="photos/img8.jpg"onclick="openFullImg(this.src)">
    </div>
    <script>
        let x=document.getElementById("firstBox");
        let y=document.getElementById("first");
      const openFullImg=(pic)=>{
         x.style.display="flex";
         y.src=pic;
      }
      const closeFullImg=()=>{
        x.style.display="none";
      }
    </script>
</body>
</html>

Style.css
*{
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    box-sizing: border-box;
}
body{
    background: rgb(244, 242, 212);
}
.img-gallery{
    width: 80%;
    margin: 100px auto 50px;
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
   grid-gap:70px;
}
.img-gallery img{
    width: 310px;
    height: 270px;
    cursor: pointer;
}
.img-gallery img:hover{
    transform: scale(0.8) rotate(10deg);
    border-radius: 20px;
    box-shadow: 0 32px 75px rgba(68, 77, 136, 0.2);
}
.complete-img{
    width: 100%;
    height: 100vh;
    background:rgba(0, 0, 0, 0.9);
    position: fixed;
    top: 0;
    left: 0;
    display:none;
    align-items: center;
    justify-content: center;
    z-index: 100;
}
.complete-img img{
    width:90%;
    max-width:500px;
}
.complete-img span{
    position: absolute;
    top: 10%;
    right:10%;
    font-size: 30px;
    color: white;
    cursor: pointer;
}
