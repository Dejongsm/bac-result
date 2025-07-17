<style>
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: #f5f7fa;
  color: #333;
}

header {
  background-color: #1e88e5;
  color: white;
  padding: 20px 0;
  text-align: center;
  font-size: 24px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.container {
  max-width: 700px;
  margin: 30px auto;
  padding: 20px;
  background: white;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

input[type="text"] {
  width: 100%;
  padding: 12px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 8px;
  margin-bottom: 20px;
}

button {
  background-color: #1e88e5;
  color: white;
  padding: 12px 20px;
  font-size: 16px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  width: 100%;
  transition: background 0.3s ease;
}

button:hover {
  background-color: #1565c0;
}

.result-card {
  background: #e3f2fd;
  padding: 15px 20px;
  margin: 20px 0;
  border-left: 6px solid #1e88e5;
  border-radius: 12px;
}

@media screen and (max-width: 600px) {
  .container {
    margin: 10px;
    padding: 15px;
  }
}
</style>
<header>
  نتائج شهادة البكالوريا 2025
</header>

<div class="container">
  <input type="text" placeholder="أدخل رقم التسجيل أو الاسم..." id="searchInput">
  <button onclick="search()">بحث</button>

  <div id="resultsArea">
    <div class="result-card">
      <h3>الاسم: محمد أمين</h3>
      <p>رقم التسجيل: 123456</p>
      <p>الشعبة: علوم تجريبية</p>
      <p>المعدل: 16.75</p>
      <p>النتيجة: ناجح مع مرتبة الشرف</p>
    </div>
  </div>
</div>
