# scotch-moon
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Scotch Videocassette - Premium Quality</title>
        <Style>
            @import url("https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Mulish:ital,wght@0,200..1000;1,200..1000&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Work+Sans:ital,wght@0,100..900;1,100..900&display=swap");

:root {
  --dark-color: #191f1d;
  --mid-dark: #555a57;
  --light-color: #ece0c8;
  --mid-light: #949993;
  --shadow: #0005;
  --linear-rainbow: linear-gradient(
    to right,#ede6bf,#ecc947,#cb5a31,#6f5d79,#4e779a
  );
  --circle-rainbow: radial-gradient(
    circle at left top,#ede6bf,#ecc947,#cb5a31,#6f5d79,#4e779a
  );
  --noise-texture: url(https://i.gyazo.com/a26366e538851a5c569ff648e99b7fd4.png);
  --gif-texture: url(https://64.media.tumblr.com/da60c13b478dda09ab90c27e880983b8/tumblr_nd4pwdPKdc1tun3l0o1_1280.gifv);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  display: grid;
  place-items: center;
  min-height: 100vh;
  background: var(--dark-color);
  background-image: var(--noise-texture);
  background-blend-mode: overlay;
  font-family: "Mulish", sans-serif;
}

h1 {
  margin: 0;
  font-family: "Mulish", sans-serif;
  font-weight: 1000;
  font-size: 64px;
  color: var(--light-color);
  text-shadow: 2px 2px 4px var(--shadow);
}

h2 {
  font-family: "Playfair Display", serif;
  font-size: 16px;
  color: var(--mid-light);
  letter-spacing: 2px;
  margin: 8px 0;
}

h3 {
  font-family: "DM Serif Display", serif;
  font-size: 24px;
  color: var(--mid-light);
  margin-bottom: 16px;
}

p {
  font-family: "Mulish", sans-serif;
  font-weight: 700;
  width: 390px;
  color: var(--mid-light);
  line-height: 1.6;
  margin-bottom: 24px;
}

nav {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding: 24px 48px;
  gap: 48px;
}

a {
  font-family: "Mulish", sans-serif;
  color: var(--mid-light);
  text-decoration: none;
  transition: all 0.3s ease;
}

a:not(.buy, .buy-cta) {
  font-size: 14px;
  font-weight: 500;
}

a:hover:not(.buy, .buy-cta) {
  color: var(--light-color);
  text-shadow: 0 0 8px var(--light-color);
}

.scotch-container {
  position: relative;
  height: 580px;
  width: 960px;
  background-image: linear-gradient(
    150deg,
    var(--dark-color) 60.2%,
    var(--mid-dark) 60.28%,
    var(--mid-dark) 60.7%,
    var(--dark-color) 60.78%,
    var(--dark-color) 61.4%,
    var(--mid-dark) 61.48%,
    var(--mid-dark) 62.6%,
    var(--dark-color) 62.68%,
    var(--dark-color) 63.4%,
    var(--mid-dark) 63.48%,
    var(--mid-dark) 64.6%,
    var(--dark-color) 64.68%,
    var(--dark-color) 65.4%,
    var(--mid-dark) 65.48%,
    var(--mid-dark) 67.4%,
    var(--dark-color) 67.48%,
    var(--dark-color) 68.4%,
    var(--mid-dark) 68.48%,
    var(--mid-dark) 71.4%,
    var(--dark-color) 71.48%,
    var(--dark-color) 72.4%,
    var(--mid-dark) 72.48%,
    var(--mid-dark) 76.4%,
    var(--dark-color) 76.48%,
    var(--dark-color) 77.4%,
    var(--mid-dark) 77.48%,
    var(--mid-dark) 81.4%,
    var(--dark-color) 81.48%,
    var(--dark-color) 82.4%,
    var(--mid-dark) 82.48%,
    var(--mid-dark) 87.4%,
    var(--dark-color) 87.48%
  );
  animation: spawn 2s ease-in-out forwards;
  box-shadow: 0 8px 32px var(--shadow);
  border-radius: 8px;
  overflow: hidden;
}

.scotch-container::before {
  content: "";
  position: absolute;
  inset: 0;
  background-image: var(--noise-texture);
  mix-blend-mode: overlay;
  pointer-events: none;
  z-index: 3;
}

.scotch-container:hover::after {
  content: "";
  position: absolute;
  inset: 0;
  background-image: var(--gif-texture);
  background-size: cover;
  mix-blend-mode: screen;
  opacity: 0.64;
  pointer-events: none;
  z-index: 3;
}

.main-container {
  padding: 48px;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.text-sphere-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 64px;
}

.text-container {
  flex: 1;
}

.sphere {
  height: 200px;
  width: 200px;
  background-image: var(--circle-rainbow);
  border: 3px solid var(--dark-color);
  border-radius: 50%;
  transition: all 0.4s ease;
  box-shadow: 0 4px 16px var(--shadow);
  cursor: pointer;
}

.sphere:hover {
  transform: scale(1.1);
  box-shadow: 16px 16px 32px var(--shadow);
}

.buy {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-weight: 900;
  border: 1px solid var(--mid-light);
  height: 40px;
  width: 128px;
  border-radius: 4px;
}

.buy:hover {
  transform: scale(1.1);
  background: var(--light-color);
  color: var(--dark-color);
  border-color: var(--light-color);
}

.buy-cta {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: var(--dark-color);
  font-weight: 900;
  background: var(--light-color);
  height: 48px;
  width: 200px;
  font-size: 16px;
  border-radius: 4px;
  transition: all 0.4s ease;
}

.buy-cta:hover {
  transform: scale(1.1);
  color: var(--light-color);
  background-image: var(--linear-rainbow);
}

.learn-arrow {
  text-align: center;
  margin-top: 32px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.learn {
  font-size: 14px;
  color: var(--mid-light);
  margin-bottom: 8px;
}

.arrow {
  font-size: 24px;
  color: var(--mid-light);
  animation: bounce 2s infinite;
}

@keyframes spawn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
}
        </Style>
        </head>
<body>
<div class="scotch-container">
    <nav>
        <a href="#">CONTACT</a>
        <a href="#">ABOUT</a>
        <a href="https://www.amazon.com/-/es/Scotch-Cinta-blanco-T-120-est%C3%A1ndar/dp/B008C7Z54Y" class="buy">BUY NOW</a>
    </nav>
    <div class="main-container">
        <div class="text-sphere-container">
            <div class="text-container">
                <h1>Scotch</h1>
                <h2>VIDEOCASSETTE EG</h2>
                <h3>T 120</h3>
                <p>Designed by the inventors of videotape, this Scotch EG Videocassette gives you superior performance and reliability for all your recording needs.</p>
                <a href="https://www.amazon.com/-/es/Scotch-Cinta-blanco-T-120-est%C3%A1ndar/dp/B008C7Z54Y" class="buy-cta">Buy Now</a>
            </div>
            <a href="https://www.amazon.com/-/es/Scotch-Cinta-blanco-T-120-est%C3%A1ndar/dp/B008C7Z54Y">
                <div class="sphere"></div>
            </a>
        </div>
        <div class="learn-arrow">
            <div class="learn">LEARN MORE</div>
            <div class="arrow">↓</div>
        </div>
    </div>
</div>
</body>
</html>
