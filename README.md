<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RoV Random Box</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #09090d;
  color: white;
}

header {
  text-align: center;
  padding: 35px 15px;
  background: linear-gradient(135deg,#160d27,#32105c);
}

.logo {
  font-size: 34px;
  font-weight: bold;
  color: #c084fc;
}

header p {
  color: #bbb;
}

.container {
  max-width: 700px;
  margin: auto;
  padding: 25px 15px;
}

.boxes {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 18px;
}

.box {
  background: #15151d;
  border: 1px solid #35204d;
  border-radius: 18px;
  padding: 25px 18px;
  text-align: center;
}

.box-icon {
  font-size: 60px;
}

.box h2 {
  margin: 12px 0;
}

.price {
  font-size: 27px;
  color: #c084fc;
  font-weight: bold;
  margin: 15px 0;
}

button {
  width: 100%;
  padding: 14px;
  border: none;
  border-radius: 10px;
  background: linear-gradient(135deg,#7c3aed,#a855f7);
  color: white;
  font-size: 17px;
  font-weight: bold;
}

button:active {
  transform: scale(.97);
}

.result {
  display: none;
  margin-top: 25px;
  padding: 20px;
  background: #15151d;
  border-radius: 15px;
  text-align: center;
}

.code {
  margin-top: 12px;
  padding: 15px;
  background: #08080b;
  border-radius: 10px;
  color: #86efac;
  font-size: 18px;
  font-weight: bold;
}

@media(max-width:500px) {
  .boxes {
    grid-template-columns: 1fr;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">🎁 RoV RANDOM BOX</div>
  <p>สุ่มรหัส RoV</p>
</header>

<div class="container">

  <div class="boxes">

    <div class="box">
      <div class="box-icon">🎁</div>
      <h2>กล่องสุ่ม 25 บาท</h2>
      <div class="price">฿25</div>
      <button onclick="buy(25)">
        ซื้อกล่อง
      </button>
    </div>

    <div class="box">
      <div class="box-icon">🎁</div>
      <h2>กล่องสุ่ม 50 บาท</h2>
      <div class="price">฿50</div>
      <button onclick="buy(50)">
        ซื้อกล่อง
      </button>
    </div>

  </div>

  <div id="result" class="result">
    <h2>🎉 ผลการสุ่ม</h2>
    <p id="message"></p>
    <div class="code" id="code"></div>
  </div>

</div>

<script>

function buy(price) {

  /*
    ตอนนี้เป็นระบบทดลอง
    ยังไม่ได้เชื่อมระบบชำระเงินจริง
  */

  const codes = [
    "ROV-DEMO-001",
    "ROV-DEMO-002",
    "ROV-DEMO-003",
    "ROV-DEMO-004"
  ];

  const random =
    codes[Math.floor(Math.random() * codes.length)];

  document.getElementById("result").style.display = "block";

  document.getElementById("message").innerText =
    "กล่องสุ่ม " + price + " บาท";

  document.getElementById("code").innerText =
    random;

  window.scrollTo({
    top: document.body.scrollHeight,
    behavior: "smooth"
  });
}

</script>

</body>
</html># my-shop
