<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="index.css">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Travel India</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f7f9fc;
      color: #102b5c;
    }

    .main1 {
      display: none;
      min-height: 100vh;
    }

    .active-main1 {
      display: block;
    }

    .sub11-navbar {
      height: 65px;
      background: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 50px;
      border-bottom: 1px solid #e5e7eb;
    }

    .sub11-logo {
      color: #0755d9;
      font-size: 22px;
      font-weight: bold;
      cursor: pointer;
    }

    .sub11-links {
      display: flex;
      list-style: none;
      gap: 38px;
      height: 65px;
      align-items: center;
    }

    .sub11-links a {
      text-decoration: none;
      color: #102b5c;
      font-size: 13px;
      font-weight: bold;
      cursor: pointer;
      height: 65px;
      display: flex;
      align-items: center;
      border-bottom: 3px solid transparent;
    }

    .sub11-links a:hover,
    .sub11-links a.active-link {
      color: #0755d9;
      border-bottom: 3px solid #75a7ff;
    }

    .sub11-login-btn {
      background: #064cc9;
      color: white;
      border: none;
      padding: 10px 22px;
      border-radius: 6px;
      font-weight: bold;
      cursor: pointer;
    }

    .sub12-hero {
      margin: 0 35px;
      height: 410px;
      border-radius: 0 0 18px 18px;
      background:
        linear-gradient(to right, rgba(0, 28, 70, 0.75), rgba(0, 0, 0, 0.1)),
        url("https://t3.ftcdn.net/jpg/03/62/78/02/360_F_362780264_ZrbVHyL54KH2CNnxl8xPFpLobTTIRmBr.jpg");
      background-size: cover;
      background-position: center;
      padding: 75px 45px;
      color: white;
    }

    .sub12-hero h1 {
      font-size: 43px;
      line-height: 1.2;
      margin-bottom: 20px;
    }

    .sub12-hero p {
      font-size: 16px;
      line-height: 1.7;
      max-width: 420px;
      margin-bottom: 25px;
    }

    .sub12-hero button {
      padding: 13px 24px;
      border: none;
      border-radius: 6px;
      margin-right: 10px;
      cursor: pointer;
      font-weight: bold;
    }

    .sub12-btn1 {
      background: #0754df;
      color: white;
    }

    .sub12-btn2 {
      background: white;
      color: #102b5c;
    }

    .sub13-search-box {
      background: white;
      width: 90%;
      margin: -45px auto 0;
      position: relative;
      border-radius: 12px;
      padding: 20px;
      display: flex;
      justify-content: space-between;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.12);
    }

    .sub13-item {
      width: 23%;
      border-right: 1px solid #e5e5e5;
      padding: 0 15px;
    }

    .sub13-item h4 {
      font-size: 13px;
      margin-bottom: 9px;
    }

    .sub13-item p {
      font-size: 12px;
      color: #8b95a7;
    }

    .sub13-btn {
      background: #063f9e;
      color: white;
      border: none;
      padding: 0 24px;
      border-radius: 7px;
      font-weight: bold;
      cursor: pointer;
    }

    .sub14-destination {
      padding: 65px;
    }

    .sub14-title-row {
      display: flex;
      justify-content: space-between;
      margin-bottom: 25px;
    }

    .sub14-title-row a {
      color: #0754df;
      font-size: 14px;
      font-weight: bold;
      cursor: pointer;
    }

    .sub14-cards,
    .sub32-cards {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .sub14-card {
      background: white;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 3px 12px rgba(0, 0, 0, 0.1);
      cursor: pointer;
      transition: 0.3s;
    }

    .sub14-card:hover {
      transform: translateY(-7px);
    }

    .sub14-card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
    }

    .sub14-card-content {
      padding: 13px;
    }

    .sub14-card-content h3 {
      font-size: 14px;
      margin-bottom: 7px;
    }

    .sub14-card-content p {
      font-size: 12px;
      color: #64748b;
      font-weight: bold;
    }

    .main2-about {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 45px 70px;
      gap: 50px;
    }

    .sub21-about-text {
      width: 45%;
    }

    .sub21-about-text h1,
    .sub41-contact-info h1 {
      font-size: 32px;
      margin-bottom: 12px;
    }

    .sub21-line {
      width: 70px;
      height: 3px;
      background: #79a9ff;
      margin-bottom: 25px;
      position: relative;
    }

    .sub21-line::after {
      content: "✈";
      position: absolute;
      right: -20px;
      top: -12px;
      font-size: 22px;
      color: #0755d9;
    }

    .sub21-about-text p {
      color: #4b5563;
      font-size: 15px;
      line-height: 1.8;
      margin-bottom: 18px;
    }

    .sub22-about-image {
      width: 50%;
    }

    .sub22-about-image img {
      width: 100%;
      height: 240px;
      object-fit: cover;
      border-radius: 12px;
    }

    .sub23-why-travel {
      border-top: 1px solid #eeeeee;
      padding: 25px 60px 35px;
    }

    .sub23-why-travel h2 {
      text-align: center;
      margin-bottom: 30px;
    }

    .sub24-features {
      display: flex;
    }

    .sub24-feature {
      width: 25%;
      padding: 10px 18px;
      border-right: 1px solid #eeeeee;
    }

    .sub24-icon {
      width: 38px;
      height: 38px;
      background: #e8f0ff;
      color: #0755d9;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 12px;
    }

    .sub24-feature h3 {
      font-size: 15px;
      margin-bottom: 9px;
    }

    .sub24-feature p {
      font-size: 13px;
      line-height: 1.6;
      color: #4b5563;
    }

    .main3-explore {
      padding: 22px 40px 30px;
      text-align: center;
    }

    .sub31-heading h1 {
      font-size: 28px;
    }

    .sub31-plane {
      color: #0755d9;
      font-size: 20px;
      margin: 5px 0 14px;
    }

    .sub32-categories {
      display: flex;
      justify-content: center;
      gap: 18px;
      margin-bottom: 20px;
    }

    .sub32-categories button {
      width: 80px;
      padding: 8px;
      border: none;
      border-radius: 6px;
      background: #eef1f5;
      color: #536078;
      font-size: 12px;
      font-weight: bold;
      cursor: pointer;
    }

    .sub32-categories button.active {
      background: #064cc9;
      color: white;
    }

    .main4-contact {
      display: flex;
      gap: 40px;
      padding: 30px 65px;
    }

    .sub41-contact-info {
      width: 42%;
      padding-top: 10px;
    }

    .sub41-contact-info > p {
      font-size: 13px;
      color: #4b5563;
      line-height: 1.6;
      margin-bottom: 18px;
    }

    .sub41-contact-item {
      display: flex;
      gap: 12px;
      margin-bottom: 16px;
    }

    .sub41-icon {
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #e8f0ff;
      color: #0755d9;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .sub41-contact-item h3 {
      font-size: 13px;
      margin-bottom: 4px;
    }

    .sub41-contact-item p {
      font-size: 12px;
      color: #5c6678;
    }

    .sub42-contact-form {
      width: 58%;
      background: white;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 3px 14px rgba(0, 0, 0, 0.12);
    }

    .form-group {
      margin-bottom: 10px;
    }

    .form-group label {
      display: block;
      font-size: 11px;
      font-weight: bold;
      margin-bottom: 5px;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      border: 1px solid #dce2eb;
      border-radius: 5px;
      padding: 10px;
      outline: none;
      font-size: 12px;
    }

    .form-group textarea {
      height: 80px;
      resize: none;
    }

    .sub42-btn {
      width: 100%;
      border: none;
      background: #063b9d;
      color: white;
      padding: 11px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }

    .main5-login {
      padding: 20px;
      background: #f4f7fb;
    }

    .main5-title {
      text-align: center;
      margin-bottom: 8px;
    }

    .main5-container {
      max-width: 950px;
      min-height: 540px;
      margin: auto;
      border-radius: 10px;
      overflow: hidden;
      display: flex;
      background:
        linear-gradient(rgba(0, 40, 100, 0.25), rgba(0, 40, 100, 0.25)),
        url("https://static.vecteezy.com/system/resources/thumbnails/034/633/270/small/ai-generated-abstract-forest-bokeh-decoration-pathway-ai-generated-photo.jpg");
      background-size: cover;
      background-position: center;
      padding: 28px;
    }

    .sub51-welcome-box {
      width: 50%;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .sub51-welcome-box h1 {
      font-size: 30px;
      margin-bottom: 15px;
    }

    .sub51-welcome-box p {
      line-height: 1.6;
      max-width: 280px;
    }

    .sub52-login-card {
      width: 48%;
      background: rgba(255, 255, 255, 0.96);
      border-radius: 12px;
      padding: 38px 35px;
      margin-left: auto;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.15);
    }

    .sub52-login-card h2 {
      margin-bottom: 12px;
    }

    .subtitle {
      font-size: 13px;
      color: #6b7280;
      margin-bottom: 25px;
    }

    .options {
      display: flex;
      justify-content: space-between;
      margin-bottom: 22px;
      font-size: 11px;
    }

    .forgot,
    .signup-text a {
      color: #0b55d8;
      text-decoration: none;
      font-weight: bold;
    }

    .sub52-btn {
      width: 100%;
      padding: 13px;
      background: #073b9d;
      color: white;
      border: none;
      border-radius: 6px;
      font-weight: bold;
      cursor: pointer;
    }

    .signup-text {
      text-align: center;
      margin-top: 30px;
      font-size: 12px;
    }

    footer {
      background: #062d66;
      color: white;
      padding: 22px 38px 0;
    }

    .main6-footer {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      padding-bottom: 18px;
    }

    .sub61-footer-box {
      width: 20%;
    }

    .sub61-footer-box h3 {
      font-size: 15px;
      margin-bottom: 11px;
    }

    .sub61-footer-box p,
    .sub61-footer-box a {
      font-size: 12px;
      color: #d8e5ff;
      text-decoration: none;
      line-height: 1.8;
      display: block;
      cursor: pointer;
    }

    .sub63-newsletter {
      display: flex;
      margin-top: 10px;
    }

    .sub63-newsletter input {
      width: 130px;
      padding: 9px;
      border: none;
      outline: none;
      border-radius: 5px 0 0 5px;
      font-size: 11px;
    }

    .sub63-newsletter button {
      border: none;
      background: #0b61dc;
      color: white;
      padding: 9px 11px;
      border-radius: 0 5px 5px 0;
      cursor: pointer;
    }

    .sub64-copyright {
      text-align: center;
      border-top: 1px solid rgba(255, 255, 255, 0.2);
      padding: 12px;
      color: #d8e5ff;
      font-size: 12px;
    }

    @media (max-width: 768px) {
      .sub11-navbar {
        padding: 0 20px;
      }

      .sub11-links {
        display: none;
      }

      .sub12-hero {
        margin: 0;
        border-radius: 0;
        padding: 55px 25px;
      }

      .sub12-hero h1 {
        font-size: 32px;
      }

      .sub13-search-box,
      .main2-about,
      .main4-contact,
      .main5-container {
        flex-direction: column;
      }

      .sub13-item,
      .sub21-about-text,
      .sub22-about-image,
      .sub41-contact-info,
      .sub42-contact-form,
      .sub51-welcome-box,
      .sub52-login-card {
        width: 100%;
      }

      .sub14-cards,
      .sub32-cards {
        grid-template-columns: repeat(2, 1fr);
      }

      .sub24-features {
        flex-direction: column;
      }

      .sub24-feature {
        width: 100%;
        border-bottom: 1px solid #eeeeee;
      }

      .main6-footer {
        flex-wrap: wrap;
      }

      .sub61-footer-box {
        width: 45%;
      }

      .sub52-login-card {
        margin-top: 20px;
      }
    }
  </style>
</head>

<body>

  <div id="home" class="main1 active-main1">
    <nav class="sub11-navbar">
      <div class="sub11-logo" onclick="showPage('home')">✈ Travel India</div>

      <ul class="sub11-links">
        <li><a class="active-link" onclick="showPage('home')">Home</a></li>
        <li><a onclick="showPage('about')">About</a></li>
        <li><a onclick="showPage('explore')">Explore</a></li>
        <li><a onclick="showPage('contact')">Contact</a></li>
      </ul>

      <button class="sub11-login-btn" onclick="showPage('login')">Login</button>
    </nav>

    <div class="sub12-hero">
      <h1>Explore The<br>Beauty of India</h1>
      <p>Discover amazing places at exclusive deals and make your journey unforgettable.</p>
      <button class="sub12-btn1" onclick="showPage('explore')">Explore Now</button>
      <button class="sub12-btn2" onclick="showPage('about')">Learn More</button>
    </div>

    <div class="sub13-search-box">
      <div class="sub13-item">
        <h4>📍 Location</h4>
        <p>Where are you going?</p>
      </div>

      <div class="sub13-item">
        <h4>📅 Check In</h4>
        <p>Add date</p>
      </div>

      <div class="sub13-item">
        <h4>📅 Check Out</h4>
        <p>Add date</p>
      </div>

      <div class="sub13-item">
        <h4>👥 Guests</h4>
        <p>Add guests</p>
      </div>

      <button class="sub13-btn">Search</button>
    </div>

    <div class="sub14-destination">
      <div class="sub14-title-row">
        <h2>Popular Destinations</h2>
        <a onclick="showPage('explore')">View All</a>
      </div>

      <div class="sub14-cards">
        <div class="sub14-card">
          <img src="https://i.pinimg.com/564x/b6/9e/a3/b69ea3c44dd0dde0263ce730bff3c8c5.jpg" alt="Ganpatipule Temple">
          <div class="sub14-card-content">
            <h3>Ganpatipule Temple, Maharashtra</h3>
            <p>From Rs. 1999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTerzqrGFzoRESWibLsa7IAkqeOOZAUlZCtixbeAlapTzbmyGl5wvnaa74&s=10" alt="Taj Mahal">
          <div class="sub14-card-content">
            <h3>Taj Mahal, Agra</h3>
            <p>From Rs. 4999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://s7ap1.scene7.com/is/image/incredibleindia/calangute-beach-goa-7-musthead-hero?qlt=82&ts=1742168166188" alt="Goa Beach">
          <div class="sub14-card-content">
            <h3>Goa Beach, Goa</h3>
            <p>From Rs. 5999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://media.cntraveler.com/photos/643d5d0a5722b1af03793a06/16:9/w_2560%2Cc_limit/Dal%2520Lake_GettyImages-1323846766.jpg" alt="Kashmir">
          <div class="sub14-card-content">
            <h3>Kashmir, India</h3>
            <p>From Rs. 6999</p>
          </div>
        </div>


      </div>
    </div>
  </div>

  <div id="about" class="main1">
    <nav class="sub11-navbar">
      <div class="sub11-logo" onclick="showPage('home')">✈ Travel India</div>

      <ul class="sub11-links">
        <li><a onclick="showPage('home')">Home</a></li>
        <li><a class="active-link" onclick="showPage('about')">About</a></li>
        <li><a onclick="showPage('explore')">Explore</a></li>
        <li><a onclick="showPage('contact')">Contact</a></li>
      </ul>

      <button class="sub11-login-btn" onclick="showPage('login')">Login</button>
    </nav>

    <div class="main2-about">
      <div class="sub21-about-text">
        <h1>About Us</h1>
        <div class="sub21-line"></div>
        <p>At Wanderly, we believe that travel is more than just visiting new places. It is about creating memorable experiences.</p>
        <p>Our mission is to help travelers explore the world with ease, comfort, and the best experiences possible.</p>
      </div>

      <div class="sub22-about-image">
        <img src="https://w0.peakpx.com/wallpaper/163/208/HD-wallpaper-sun-rise-skies-sun-cloud-rise-ocean.jpg" alt="Travel View">
      </div>
    </div>

    <div class="sub23-why-travel">
      <h2>Why Travel With Us?</h2>

      <div class="sub24-features">
        <div class="sub24-feature">
          <div class="sub24-icon">💵</div>
          <h3>Best Prices</h3>
          <p>We offer the best prices and amazing deals for your journey.</p>
        </div>

        <div class="sub24-feature">
          <div class="sub24-icon">🏆</div>
          <h3>Trusted Service</h3>
          <p>Our team is available 24/7 to assist you anytime.</p>
        </div>

        <div class="sub24-feature">
          <div class="sub24-icon">🏨</div>
          <h3>Handpicked Hotels</h3>
          <p>We partner with top-rated hotels for your comfortable stay.</p>
        </div>

        <div class="sub24-feature">
          <div class="sub24-icon">✈</div>
          <h3>Memorable Experiences</h3>
          <p>We help you create memories that last a lifetime.</p>
        </div>
      </div>
    </div>

    <div id="footer-about"></div>
  </div>

  <div id="explore" class="main1">
    <nav class="sub11-navbar">
      <div class="sub11-logo" onclick="showPage('home')">✈ Travel India</div>

      <ul class="sub11-links">
        <li><a onclick="showPage('home')">Home</a></li>
        <li><a onclick="showPage('about')">About</a></li>
        <li><a class="active-link" onclick="showPage('explore')">Explore</a></li>
        <li><a onclick="showPage('contact')">Contact</a></li>
      </ul>

      <button class="sub11-login-btn" onclick="showPage('login')">Login</button>
    </nav>

    <div class="main3-explore">
      <div class="sub31-heading">
        <h1>Explore Destinations</h1>
        <div class="sub31-plane">✈</div>
      </div>

      <div class="sub32-categories">
        <button class="active">All</button>
        <button>Beach</button>
        <button>Mountains</button>
        <button>City</button>
        <button>Temples</button>
      </div>

      <div class="sub32-cards">
        <div class="sub14-card">
          <img src="https://i.pinimg.com/564x/b6/9e/a3/b69ea3c44dd0dde0263ce730bff3c8c5.jpg" alt="Ganpatipule Temple">
          <div class="sub14-card-content">
            <h3>Ganpatipule Temple, Maharashtra</h3>
            <p>From Rs. 1999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTerzqrGFzoRESWibLsa7IAkqeOOZAUlZCtixbeAlapTzbmyGl5wvnaa74&s=10" alt="Taj Mahal">
          <div class="sub14-card-content">
            <h3>Taj Mahal, Agra</h3>
            <p>From Rs. 4999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://s7ap1.scene7.com/is/image/incredibleindia/calangute-beach-goa-7-musthead-hero?qlt=82&ts=1742168166188" alt="Goa Beach">
          <div class="sub14-card-content">
            <h3>Goa Beach, Goa</h3>
            <p>From Rs. 5999</p>
          </div>
        </div>

        <div class="sub14-card">
          <img src="https://media.cntraveler.com/photos/643d5d0a5722b1af03793a06/16:9/w_2560%2Cc_limit/Dal%2520Lake_GettyImages-1323846766.jpg" alt="Kashmir">
          <div class="sub14-card-content">
            <h3>Kashmir, India</h3>
            <p>From Rs. 6999</p>
          </div>
        </div>
        <div class="sub14-card">
            <img src="https://t4.ftcdn.net/jpg/00/59/66/35/360_F_59663502_Q0oCrYRXnIO5R07PehAz03duabpJnM23.jpg">
            <div class="sub14-content">
                <h3>Jaipur, Rajasthan</h3>
                <p>From Rs.8999</p>
            </div>
        </div>
        <div class="sub14-card">
            <img src="https://t4.ftcdn.net/jpg/01/96/02/01/360_F_196020123_gO0XJKP1zWkKjtLQeIRV05dGcIIlIeAo.jpg">
            <div class="sub14-content">
                <h3>Kullu Manali,Shimla</h3>
                <p>From Rs.11999</p>
            </div>
        </div>
        <div class="sub14-card">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTUl7O7MzJ-fTruDRrdoxU1cLVovLnZfik8xaW4-GR7lk5KOq4PLpj-X7M&s=10">
            <div class="sub14-content">
                <h3>Hampi,Karnataka</h3>
                <p>From Rs.5999</p>
            </div>
        </div>
        <div class="sub14-card">
            <img src="https://t3.ftcdn.net/jpg/03/11/74/00/360_F_311740081_PL7ftGHnZL7JMBQpigswigY2xFwSRHJg.jpg">
            <div class="sub14-content">
                <h3>Golden Temple, Amritsar</h3>
                <p>From Rs.4999</p>
            </div>
        </div>
      </div>
    </div>

    <div id="footer-explore"></div>
  </div>

  <div id="contact" class="main1">
    <nav class="sub11-navbar">
      <div class="sub11-logo" onclick="showPage('home')">✈ Travel India</div>

      <ul class="sub11-links">
        <li><a onclick="showPage('home')">Home</a></li>
        <li><a onclick="showPage('about')">About</a></li>
        <li><a onclick="showPage('explore')">Explore</a></li>
        <li><a class="active-link" onclick="showPage('contact')">Contact</a></li>
      </ul>

      <button class="sub11-login-btn" onclick="showPage('login')">Login</button>
    </nav>

    <div class="main4-contact">
      <div class="sub41-contact-info">
        <h1>Get In Touch</h1>
        <div class="sub21-line"></div>
        <p>Have questions or need assistance?<br>We're here to help!</p>

        <div class="sub41-contact-item">
          <div class="sub41-icon">✉</div>
          <div>
            <h3>Email</h3>
            <p>rajeshmarkantewar@gmail.com</p>
          </div>
        </div>

        <div class="sub41-contact-item">
          <div class="sub41-icon">☎</div>
          <div>
            <h3>Phone</h3>
            <p>+91 8767505715</p>
          </div>
        </div>

        <div class="sub41-contact-item">
          <div class="sub41-icon">📍</div>
          <div>
            <h3>Address</h3>
            <p>Hingoli Gate, Nanded</p>
          </div>
        </div>
      </div>

      <div class="sub42-contact-form">
        <form>
          <div class="form-group">
            <label>Your Full Name:</label>
            <input type="text" placeholder="Enter your name">
          </div>

          <div class="form-group">
            <label>Email Address:</label>
            <input type="email" placeholder="Enter your email">
          </div>

          <div class="form-group">
            <label>Subject:</label>
            <input type="text" placeholder="Enter subject">
          </div>

          <div class="form-group">
            <label>Message:</label>
            <textarea placeholder="Write your message..."></textarea>
          </div>

          <button type="button" class="sub42-btn">Send Message</button>
        </form>
      </div>
    </div>

    <div id="footer-contact"></div>
  </div>

  <div id="login" class="main1 main5-login">
    <h2 class="main5-title">LOGIN PAGE</h2>

    <div class="main5-container">
      <div class="sub51-welcome-box">
        <h1>Welcome Back!</h1>
        <p>Login to continue your journey with us and explore the world.</p>
      </div>

      <div class="sub52-login-card">
        <h2>Login</h2>
        <p class="subtitle">Enter your credentials to access your account.</p>

        <form>
          <div class="form-group">
            <label>Email Address:</label>
            <input type="email" placeholder="Enter your email">
          </div>

          <div class="form-group">
            <label>Password:</label>
            <input type="password" placeholder="Enter your password">
          </div>

          <div class="options">
            <label><input type="checkbox"> Remember Me</label>
            <a href="#" class="forgot">Forgot Password?</a>
          </div>

          <button type="button" class="sub52-btn">Login</button>
        </form>

        <p class="signup-text">Don't have an account? <a href="#">Sign Up</a></p>
      </div>
    </div>
  </div>

  <template id="footer-template">
    <footer>
      <div class="main6-footer">
        <div class="sub61-footer-box">
          <h3>Travel India</h3>
          <p>Let's make your next journey your best adventure yet.</p>
        </div>

        <div class="sub61-footer-box">
          <h3>Quick Links</h3>
          <a onclick="showPage('home')">Home</a>
          <a onclick="showPage('about')">About</a>
          <a onclick="showPage('explore')">Explore</a>
          <a onclick="showPage('contact')">Contact</a>
        </div>

        <div class="sub61-footer-box">
          <h3>Top Destinations</h3>
          <a>Taj Mahal, Agra</a>
          <a>Goa Beach, Goa</a>
          <a>Ganpatipule Temple, Maharashtra</a>
          <a>Kashmir, India</a>
        </div>

        <div class="sub61-footer-box">
          <h3>Newsletter</h3>
          <p>Subscribe to get travel updates and offers.</p>

          <div class="sub63-newsletter">
            <input type="email" placeholder="Enter your email">
            <button type="button">➤</button>
          </div>
        </div>
      </div>

      <div class="sub64-copyright">
        © 2026 Travel India. All Rights Reserved.
      </div>
    </footer>
  </template>

  <script>
    const footerTemplate = document.getElementById("footer-template").innerHTML;

    document.getElementById("footer-about").innerHTML = footerTemplate;
    document.getElementById("footer-explore").innerHTML = footerTemplate;
    document.getElementById("footer-contact").innerHTML = footerTemplate;

    function showPage(pageId) {
      const pages = document.querySelectorAll(".main1");

      pages.forEach(function (page) {
        page.classList.remove("active-main1");
      });

      document.getElementById(pageId).classList.add("active-main1");

      window.scrollTo(0, 0);
    }
  </script>

</body>
</html>
