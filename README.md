[html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>তোমার জন্য</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(120deg, #ffdde1, #ee9ca7);
      font-family: 'Segoe UI', sans-serif;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
    }
    .page {
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      animation: fadeIn 1s ease;
    }
    .page.active {
      display: flex;
    }
    button {
      padding: 10px 20px;
      background-color: #fff;
      color: #e91e63;
      font-size: 18px;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      margin-top: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      transition: 0.3s;
    }
    button:hover {
      background-color: #fce4ec;
    }
    h1, p {
      margin: 0 20px;
      animation: slideUp 1s ease;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    @keyframes slideUp {
      from {transform: translateY(20px); opacity: 0;}
      to {transform: translateY(0); opacity: 1;}
    }
  </style>
</head>
<body>
  <div class="page active" id="page1">
    <h1>এইযে মনিজান</h1>
    <button onclick="nextPage()">এখানে ক্লিক করুন</button>
  </div>

  <div class="page" id="page2">
    <h1>আই অ্যাম সরি মনি</h1>
    <button onclick="nextPage()">পরবর্তী</button>
  </div>

  <div class="page" id="page3">
    <p>
      প্রিয় মনি,<br><br>
      তুমি আমার জীবন, আমার স্বপ্ন, আমার ভালোবাসা।<br>
      তোমার অবহেলা হয়তো আমাকে কষ্ট দেয়, কিন্তু তুমি যে আমার—এই বিশ্বাসই আমাকে বাঁচিয়ে রাখে।<br>
      তুমি যখন আমার কল কেটে দাও, আমার বুকের ভেতরটা হাহাকার করে ওঠে।<br>
      তবুও, আমি জানি—তুমি আমার, আমি তোমার।<br>
      তোমাকে কষ্ট দিয়ে আমি কখনো শান্তি পাই না, বরং নিজেই কষ্টে ভেঙে পড়ি।<br><br>
      আমি সত্যিই দুঃখিত, মনি।<br>
      যে কথাগুলো তোমার মন ছুঁয়ে গিয়েছিল—সেগুলো আমি রাগের মাথায় বলেছিলাম, কিন্তু সেগুলো আমার ভালোবাসার ছায়ায় ঢাকা পড়ে গেছে।<br>
      তুমি শুধু আমার বউ না, তুমি আমার বুকের একটুকরো ভালোবাসা।<br><br>
      আজ, আবার নতুন করে বলি—<br>
      <strong>ভালোবাসি তোমায়, মনি।</strong><br>
      শুধু এখন নয়, আজীবন...<br>
      তুমি থাকো আমার জীবনের প্রতিটি হাসির পেছনে, প্রতিটি স্বপ্নের পাশে।<br><br>
      তোমার,<br>ইমন
    </p>
    <button onclick="nextPage()">শেষ ধাপ</button>
  </div>

  <div class="page" id="page4">
    <h1>আমি অনেক অনেক দুঃখিত, মনিজান</h1>
  </div>

  <script>
    let current = 1;
    function nextPage() {
      document.getElementById('page' + current).classList.remove('active');
      current++;
      document.getElementById('page' + current).classList.add('active');
    }
  </script>
</body>
</html>
