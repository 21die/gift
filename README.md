# gift
giftexport
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>NFT Gifts Shop</title>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding: 30px;
      background-color: #f4f4f4;
    }
    button {
      padding: 15px 25px;
      font-size: 18px;
      background-color: #0088cc;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>🎁 NFT Подарки</h1>
  <p>Нажмите кнопку ниже, чтобы купить подарок за Stars</p>
  <button onclick="buyGift()">Купить за Stars</button>

  <script>
    Telegram.WebApp.ready();

    function buyGift() {
      Telegram.WebApp.openInvoice({
        slug: "example_gift_slug", // Заменишь позже на реальный slug
        callback: (status) => {
          if (status === 'paid') {
            alert("🎉 Покупка успешна!");
          } else {
            alert("❌ Покупка не удалась");
          }
        }
      });
    }
  </script>
</body>
</html>
