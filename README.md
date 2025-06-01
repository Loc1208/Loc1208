DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lời Tỏ Tình Dễ Thương</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(#ffdde1, #ee9ca7);
      overflow: hidden;
      font-family: 'Arial', sans-serif;
    }

    .falling-text, .heart {
      position: absolute;
      animation: fall 8s linear infinite;
      opacity: 0;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100px);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      100% {
        transform: translateY(110vh);
        opacity: 0;
      }
    }

    .heart {
      color: red;
      font-size: 24px;
      animation-duration: 6s;
    }
  </style>
</head>
<body>

<script>
  const messages = [
    "Anh yêu em 💕",
    "Làm người yêu anh nha? 😳",
    "Mỗi ngày đều muốn nhìn thấy em 😊",
    "Em là người duy nhất trong tim anh 💓",
    "Không có em, anh như mất phương hướng 🧭",
    "Cười lên đi, em đẹp lắm 😍",
    "Yêu em là điều đúng đắn nhất anh từng làm ❤️",
    "Mỗi lần gặp em, tim anh lại loạn nhịp 💘",
    "Em là giấc mơ anh không muốn tỉnh lại 💭",
    "Điều ước duy nhất của anh: Có em bên cạnh 🎁",
    "Anh nhớ em nhiều lắm 😔",
    "Hãy nắm tay anh đến cuối con đường nhé 🤝",
    "Em là mặt trời trong ngày mưa của anh 🌞",
    "Em có biết anh thích em đến mức nào không? 🥺",
    "Anh hứa sẽ luôn làm em cười 😄"
  ];

  function createMessage(text) {
    const msg = document.createElement('div');
    msg.className = 'falling-text';
    msg.textContent = text;
    msg.style.left = Math.random() * 90 + '%';
    msg.style.top = '-50px';
    msg.style.fontSize = (16 + Math.random() * 10) + 'px';
    document.body.appendChild(msg);

    setTimeout(() => msg.remove(), 10000);
  }

  function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.textContent = '❤️';
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.top = '-30px';
    heart.style.fontSize = (20 + Math.random() * 20) + 'px';
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 7000);
  }

  setInterval(() => {
    const randomMsg = messages[Math.floor(Math.random() * messages.length)];
    createMessage(randomMsg);
  }, 700);

  setInterval(() => {
    createHeart();
  }, 500);
</script>

</body>
</html>
