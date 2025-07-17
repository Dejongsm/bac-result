<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>نتيجتك في البكالوريا 2025</title>
  <style>
    body {
      direction: rtl;
      font-family: 'Cairo', sans-serif;
      background-color: #f7f7f7;
      text-align: center;
      padding: 40px;
    }

    h1 {
      color: #006400;
      font-size: 28px;
    }

    input, button {
      padding: 10px;
      margin: 10px;
      font-size: 18px;
    }

    #resultBox {
      margin-top: 30px;
      background-color: #ffffff;
      padding: 20px;
      border: 2px solid #cccccc;
      border-radius: 10px;
      box-shadow: 0px 0px 10px #aaaaaa;
      display: none;
    }

    .mabrouk {
      color: green;
      font-size: 22px;
    }

    .rassib {
      color: red;
      font-size: 22px;
    }

    .ayah {
      margin-top: 20px;
      font-style: italic;
      color: #444;
    }

    .name {
      font-weight: bold;
      font-size: 20px;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>

  <h1>📋 نتيجة البكالوريا 2025</h1>

  <p>أدخل رقم التسجيل واسمك الكامل لمشاهدة نتيجتك الرسمية:</p>

  <input type="text" id="name" placeholder="الاسم الكامل">
  <input type="text" id="matricule" placeholder="رقم التسجيل">
  <br>
  <button onclick="showResult()">عرض النتيجة</button>

  <div id="resultBox">
    <div class="name" id="studentName"></div>
    <div id="moyenneText"></div>
    <div class="ayah" id="ayahText"></div>
  </div>

  <script>
    const ayatSuccess = [
      "قُلْ بِفَضْلِ اللَّهِ وَبِرَحْمَتِهِ فَبِذَٰلِكَ فَلْيَفْرَحُوا – يونس:58",
      "وَقُلِ ٱعْمَلُوا فَسَيَرَى ٱللَّهُ عَمَلَكُمْ – التوبة:105",
      "إِنَّ مَعَ الْعُسْرِ يُسْرًا – الشرح:6",
      "وَمَا تَوْفِيقِي إِلَّا بِاللَّهِ – هود:88",
      "فَصَبْرٌ جَمِيلٌ ۖ وَاللَّهُ الْمُسْتَعَانُ – يوسف:18"
    ];

    const ayatFail = [
      "لَا تَحْزَنْ إِنَّ اللَّهَ مَعَنَا – التوبة:40",
      "وَعَسَى أَنْ تَكْرَهُوا شَيْئًا وَهُوَ خَيْرٌ لَّكُمْ – البقرة:216",
      "إِنَّ مَعَ الْعُسْرِ يُسْرًا – الشرح:6",
      "فَإِنَّ مَعَ الْعُسْرِ يُسْرًا – الشرح:5",
      "وَلَا تَهِنُوا وَلَا تَحْزَنُوا وَأَنتُمُ الْأَعْلَوْنَ – آل عمران:139"
    ];

    function getRandomAyah(success) {
      const list = success ? ayatSuccess : ayatFail;
      return list[Math.floor(Math.random() * list.length)];
    }

    function generateMoyenne() {
      // معدل بين 5.00 و 19.90
      return (Math.random() * 14.90 + 5).toFixed(2);
    }

    function showResult() {
      const name = document.getElementById("name").value.trim();
      const matricule = document.getElementById("matricule").value.trim();

      if (name === "" || matricule === "") {
        alert("يرجى إدخال الاسم ورقم التسجيل.");
        return;
      }

      const moyenne = parseFloat(generateMoyenne());
      const resultDiv = document.getElementById("resultBox");
      const moyenneText = document.getElementById("moyenneText");
      const ayahText = document.getElementById("ayahText");
      const studentName = document.getElementById("studentName");

      studentName.textContent = "📌 الاسم: " + name;

      if (moyenne >= 10) {
        moyenneText.innerHTML = `<span class="mabrouk">✅ ناجح! معدلك: ${moyenne}</span>`;
        ayahText.textContent = getRandomAyah(true);
      } else {
        moyenneText.innerHTML = `<span class="rassib">❌ راسب! معدلك: ${moyenne}</span>`;
        ayahText.textContent = getRandomAyah(false);
      }

      resultDiv.style.display = "block";
    }
  </script>

</body>
</html>
