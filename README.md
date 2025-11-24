# creativity-meets-code
NeuraCanvas is a vibrant one-section landing page that fuses imagination with technology. Built entirely with pure HTML and CSS, it features a dynamic hero animation that flows with color, motion, and light — capturing the spirit of creativity meeting code. No frameworks, just handcrafted design that inspires innovation.
mkdir creativity-meets-code
cd creativity-meets-code
touch index.html style.css
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NeuraCanvas | Creativity Meets Code</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <section class="hero">
    <div class="content">
      <h1 class="headline">
        Creativity <span>Meets</span> Code
      </h1>
      <p class="subtext">
        NeuraCanvas — Where imagination compiles into reality.
      </p>
      <a href="#" class="cta-btn">Join the Beta</a>
    </div>
    <div class="glow"></div>
  </section>
</body>
</html>
/* Basic Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Poppins", sans-serif;
  background: radial-gradient(circle at top left, #080808, #141414, #000);
  color: white;
  overflow: hidden;
}

/* Hero Section */
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  position: relative;
  text-align: center;
  flex-direction: column;
}

/* Animated Headline */
.headline {
  font-size: 3.5rem;
  font-weight: 700;
  letter-spacing: 1px;
  background: linear-gradient(90deg, #ff0077, #00e5ff, #ff0077);
  background-size: 300%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: flowGradient 6s infinite linear, fadeUp 1.2s ease-out;
}

.headline span {
  display: inline-block;
  animation: bounceIn 1.5s ease-in-out infinite alternate;
}

/* Subtext */
.subtext {
  margin-top: 1rem;
  font-size: 1.1rem;
  color: #b3b3b3;
  animation: fadeUp 1.8s ease-out;
}

.cta-btn {
  margin-top: 2rem;
  padding: 0.8rem 1.8rem;
  background: linear-gradient(90deg, #ff0077, #00e5ff);
  border: none;
  color: white;
  border-radius: 25px;
  text-decoration: none;
  font-weight: 600;
  transition: 0.3s;
}

.cta-btn:hover {
  transform: scale(1.1);
}

/* Glowing Background Animation */
.glow {
  position: absolute;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(255,0,119,0.25), transparent 70%);
  animation: pulse 4s ease-in-out infinite;
  z-index: -1;
  border-radius: 50%;
}

/* KEYFRAMES */

/* Flowing gradient on text */
@keyframes flowGradient {
  0% { background-position: 0%; }
  100% { background-position: 300%; }
}

/* Bounce animation for “Meets” word */
@keyframes bounceIn {
  0% { transform: translateY(0); }
  100% { transform: translateY(-10px); }
}

/* Smooth fade-up effect for hero text */
@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Pulsing glow behind text */
@keyframes pulse {
  0%, 100% {
    transform: scale(0.9);
    opacity: 0.6;
  }
  50% {
    transform: scale(1.1);
    opacity: 1;
  }
}

/* Responsive */
@media (max-width: 768px) {
  .headline {
    font-size: 2.2rem;
  }
  .subtext {
    font-size: 1rem;
  }
}
git init
git add .
git commit -m "Initial commit: Creativity Meets Code landing page"
