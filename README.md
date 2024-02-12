# final-one
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine Card</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="envelope">
            <div class="card">
                <h1 class="message">Do you know!<br>what's on valentine's menu?<br>Me n U</h1>
                <div class="heart"></div>
            </div>
        </div>
        <div class="cover"></div>
        <div class="lid"></div>
        <div class="shadow"></div>
    </div>
  <style>
    * {
    margin: 0;
    padding: 0;
}
 h1 {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif ;
 }
 body {
    height: 100vh;
    width: 100vw;
    background: #fee2e9;
    font-family: "pangolin", cursive;
    font-size: 1vmin;
    display: flex;
    align-items: center;
    justify-content: center;
 }
 .container {
    position: relative;
    top: 0vmin;
 }
 .envelope {
    position: relative;
    background: #f980a1;
    height: 30vmin;
    width: 47.9vmin;
 }
 .card {
    position: absolute;
    background: white;
    height: 25vmin;
    width: 43vmin;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    left: 2.5vmin;
    top: 0vmin;
    animation: slide-rev 0.2s ease-out;
 }
 .message {
    position: absolute;
    top: 5vmin;
 }
 .cover {
    position: absolute;
    height: 0;
    width:0;
    border-bottom: 15vmin solid #fba7bd;
    border-left: 24vmin solid transparent;
    border-right: 24vmin solid  transparent;
    top: 15vmin;
    z-index: 3;
 }
 .cover::after {
    /*left triangle*/
    position: absolute;
    content: "";
    border-left: 24.5vmin solid #fcbbcc;
    border-bottom: 15vmin solid transparent;
    border-top: 15vmin solid transparent;
    top: -15vmin;
    left: -24vmin;
 }
 .cover::before {
    position: absolute;
    content: "";
    border-right: 24.5vmin solid #fcbbcc;
    border-bottom: 15vmin solid transparent;
    border-top: 15vmin solid transparent;
    top: -15vmin;
    left: -0.5vmin;
 }
 .lid {
    position: absolute;
    height: 0;
    width: 0;
    border-top: 15vmin solid #f980a1;
    border-left: 24vmin solid transparent;
    border-right: 24vmin solid transparent;
    top: 0;
    transform-origin: top;
    animation: open-rev 2s;
 }
 .container:hover .lid {
    animation: open 0.5s;
    animation-fill-mode: forwards;
 }
 .container:hover .card {
    animation: slide 0.2s;
    animation-delay: 0.5s;
    animation-fill-mode: forwards;
 }
 .shadow {
    position: relative;
    top: 3vmin;
    border-radius: 50%;
    opacity: 0.7;
    height: 2vmin;
    width: 48vmin;
    background: #e8c5d0;
 }
 .heart {
    position: relative;
    width: 5vmin;
    height: 4vmin;
    top: 7vmin;
    left: -1vmin;
 }
 .heart:before,
 .heart:after {
    position: absolute;
    content: "";
    left: 2.vmin;
    top: 7vmin;
    width: 2.5vmin;
    height: 4vmin;
    background: #f40b4a;
    border-radius: 2.5vmin 2.5vmin 0 0;
    transform: rotate(-45deg);
    transform-origin: 0 100%;
 }
 .heart:after {
    left: 0;
    transform: rotate(45deg);
    transform-origin: 100% 100%;
 }
 @keyframes open {
    100% {
        transform: rotate(180deg);
    }
 }
 @keyframes slide {
    100% {
        transform: translateY(-15vmin);
        z-index: 2;
    }
 }
 @keyframes open-rev {
    from {
        transform:rotateX(-180deg);
    }
 }
 @keyframes slide-rev {
    from {
        transform: rotateY(-15vmin);
    }
 }
  </style>
</body>
</html>
