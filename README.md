<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>NekoCafé</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #47243D;      /* темно-бордовый */
      --secondary: #FFE6D6;    /* светло-персиковый */
      --accent: #FF9494;       /* мягкий розовый */
      --text: #2D1810;         /* темно-коричневый */
      --white: #FFFFFF;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      background-color: var(--primary);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem;
    }

    .main-container {
      background-color: var(--secondary);
      border-radius: 20px;
      padding: 2rem;
      max-width: 800px;
      width: 100%;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    }

    h1 {
      color: var(--text);
      text-align: center;
      font-size: 2.5rem;
      margin-bottom: 2rem;
      font-weight: bold;
      background-color: var(--white);
      padding: 1rem;
      border-radius: 15px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    }

    .menu-title {
      color: var(--text);
      text-align: center;
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      font-weight: bold;
    }

    .menu-item {
      display: flex;
      align-items: center;
      gap: 1rem;
      background-color: var(--white);
      padding: 1rem;
      border-radius: 15px;
      margin-bottom: 1rem;
      transition: transform 0.2s ease;
    }

    .menu-item:hover {
      transform: translateY(-2px);
    }

    .menu-item img {
      width: 50px;
      height: 50px;
      object-fit: contain;
    }

    .menu-item-content {
      flex-grow: 1;
    }

    .menu-item-title {
      font-weight: bold;
      color: var(--text);
      margin-bottom: 0.2rem;
    }

    .menu-item-description {
      font-size: 0.9rem;
      color: #666;
      font-style: italic;
    }

    .menu-item-price {
      color: var(--text);
      font-weight: bold;
      font-size: 1.1rem;
    }

    /* Стили для рейтинга */
    .rating-section {
      margin-top: 2rem;
      text-align: center;
      padding: 1.5rem;
      background-color: var(--white);
      border-radius: 15px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    }

    .rating-title {
      color: var(--text);
      font-size: 1.5rem;
      margin-bottom: 1rem;
      font-weight: bold;
    }

    .rating-stars {
      display: flex;
      justify-content: center;
      gap: 0.5rem;
      margin-bottom: 1rem;
    }

    .rating-stars input[type="radio"] {
      display: none;
    }

    .rating-stars label {
      font-size: 2rem;
      color: var(--accent);
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    .rating-stars label:hover,
    .rating-stars input[type="radio"]:checked ~ label {
      color: #FFD700;
      transform: scale(1.1);
    }

    .rating-message {
      color: var(--text);
      font-style: italic;
      font-size: 0.9rem;
    }

    @media (max-width: 600px) {
      body {
        padding: 1rem;
      }

      .main-container {
        padding: 1rem;
      }

      h1 {
        font-size: 2rem;
      }

      .rating-stars label {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <div class="main-container">
    <h1>Welcome to NekoCafé</h1>
    
    <div class="menu">
      <h2 class="menu-title">Menu</h2>
      
      <div class="menu-item">
        <img src="cheesecake-icon.png" alt="Cheesecake">
        <div class="menu-item-content">
          <div class="menu-item-title">Cheesecake</div>
          <div class="menu-item-description">Get a free strawberry w/ it :3</div>
        </div>
        <div class="menu-item-price">$15.00</div>
      </div>

      <div class="menu-item">
        <img src="coffee-icon.png" alt="Coffee">
        <div class="menu-item-content">
          <div class="menu-item-title">Coffee</div>
          <div class="menu-item-description">Coffee with cat is the best combo :3</div>
        </div>
        <div class="menu-item-price">$7.00</div>
      </div>

      <div class="menu-item">
        <img src="croissant-icon.png" alt="Croissant">
        <div class="menu-item-content">
          <div class="menu-item-title">Croissant</div>
          <div class="menu-item-description">Tastes best with our COFFEE!! meow coffee :3</div>
        </div>
        <div class="menu-item-price">$12.00</div>
      </div>
    </div>

    <div class="rating-section">
      <h3 class="rating-title">Rate our café :3</h3>
      <div class="rating-stars">
        <input type="radio" id="star5" name="rating" value="5">
        <label for="star5">★</label>
        <input type="radio" id="star4" name="rating" value="4">
        <label for="star4">★</label>
        <input type="radio" id="star3" name="rating" value="3">
        <label for="star3">★</label>
        <input type="radio" id="star2" name="rating" value="2">
        <label for="star2">★</label>
        <input type="radio" id="star1" name="rating" value="1">
        <label for="star1">★</label>
      </div>
      <p class="rating-message">Thank you for your feedback! :3</p>
    </div>
  </div>
</body>
</html>
