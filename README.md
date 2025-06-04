<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>مدیریت ترافیک - زیرو فورتی فور</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Vazir:wght@400;700&family=Inter:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Vazir', sans-serif;
      background: linear-gradient(135deg, #2a1b3d 0%, #1e2a44 100%);
      color: #e5e7eb;
      line-height: 1.8;
    }
    .section-card {
      background: #1f2937;
      border-radius: 12px;
      padding: 24px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
      margin-bottom: 24px;
      animation: slideIn 0.5s ease-out;
    }
    .code-block {
      background: #111827;
      border-radius: 8px;
      padding: 16px;
      position: relative;
      margin-bottom: 16px;
      overflow-x: auto;
      font-family: 'Inter', monospace;
    }
    .copy-btn {
      background: linear-gradient(90deg, #7c3aed, #db2777);
      color: white;
      padding: 8px 16px;
      border-radius: 6px;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.2s;
      position: absolute;
      top: 8px;
      left: 8px;
    }
    .copy-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    .cake-animation {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 3rem;
      animation: pop 0.6s ease-out;
      display: none;
    }
    @keyframes slideIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes pop {
      0% { transform: translate(-50%, -50%) scale(0); opacity: 0; }
      50% { transform: translate(-50%, -50%) scale(1.3); opacity: 1; }
      100% { transform: translate(-50%, -50%) scale(1); opacity: 0; }
    }
    .logo {
      white-space: pre;
      text-align: center;
      color: #a78bfa;
      font-family: 'Inter', monospace;
    }
    h1, h2, h3 {
      color: #d1d5db;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col items-center py-12 px-4">

  <div class="cake-animation" id="cake">کپی شد</div>

  <header class="text-center mb-12">
    <div class="logo text-lg">
      ____   _  _   _  _  
     |  _ \ | || | | || | 
     | | | || || |_| || | 
     | |_| ||__   _||__ | 
     |____/    |_|    |_| 

        0   4   4        
    </div>
    <h1 class="text-4xl font-bold mt-4">مدیریت ترافیک</h1>
    <p class="text-lg text-gray-400">توسط زیرو فورتی فور</p>
  </header>

  <main class="max-w-4xl w-full">

    <!-- معرفی -->
    <section class="section-card">
      <h2 class="text-2xl font-bold mb-4">درباره مدیریت ترافیک</h2>
      <p class="text-gray-300">
        اسکریپت <strong>مدیریت ترافیک</strong> یک ابزار قدرتمند مبتنی بر پایتون است که برای مدیریت دقیق ترافیک شبکه طراحی شده است. این ابزار با حفظ نسبت آپلود به دانلود (پیش‌فرض 15:1)، انتخاب دینامیک آدرس‌های IP، و رابط کاربری جذاب، انتخابی ایده‌آل برای اتوماسیون شبکه است.
      </p>
      <ul class="list-disc list-inside text-gray-300 mt-4">
        <li>حفظ نسبت آپلود به دانلود 15:1.</li>
        <li>انتخاب دینامیک IP از رنج‌های تعریف‌شده در JSON.</li>
        <li>پایگاه داده SQLite برای ثبت ترافیک و درخواست‌ها.</li>
        <li>رابط کاربری خط فرمان (CLI) با رنگ‌های جذاب.</li>
        <li>طراحی اختصاصی توسط زیرو فورتی فور با تمرکز بر دقت و عملکرد.</li>
      </ul>
    </section>

    <!-- راهنمای نصب -->
    <section class="section-card">
      <h2 class="text-2xl font-bold mb-4">راهنمای نصب</h2>

      <div class="mb-8">
        <h3 class="text-xl font-semibold mb-2">گام ۱: حذف نصب قبلی</h3>
        <p class="text-gray-400 mb-2">برای نصب تمیز، ابتدا نصب‌های قبلی را حذف کنید.</p>
        <div class="code-block">
<pre class="text-blue-300" id="code1">sudo systemctl stop traffic_manager.service
sudo systemctl disable traffic_manager.service
sudo rm -rf /var/www/traffic_manager
sudo rm -f /etc/systemd/system/traffic_manager.service
sudo rm -f /usr/local/bin/menu
sudo rm -f /var/log/traffic_manager.log
sudo rm -f /tmp/traffic_manager_test.log
sudo rm -f /tmp/pip_install.log
sudo systemctl daemon-reload
sudo systemctl reset-failed</pre>
          <button class="copy-btn" onclick="copyCode('code1')">کپی</button>
        </div>
      </div>

      <div class="mb-8">
        <h3 class="text-xl font-semibold mb-2">گام ۲: آپلود فایل‌ها</h3>
        <p class="text-gray-400 mb-2">فایل‌ها را در <code class="text-blue-500">https://0-4-4.com/upload/</code> آپلود کنید.</p>
        <div class="code-block">
<pre class="text-blue-300" id="code2">curl -I https://0-4-4.com/upload/ip_ranges.json</pre>
          <button class="copy-btn" onclick="copyCode('code2')">کپی</button>
        </div>
      </div>

      <div class="mb-8">
        <h3 class="text-xl font-semibold mb-2">گام ۳: اجرای نصب</h3>
        <div class="code-block">
<pre class="text-blue-300" id="code3">sudo curl https://0-4-4.com/upload/setup.sh | sudo bash</pre>
          <button class="copy-btn" onclick="copyCode('code3')">کپی</button>
        </div>
      </div>

      <div class="mb-8">
        <h3 class="text-xl font-semibold mb-2">گام ۴: اجرای منو</h3>
        <div class="code-block">
<pre class="text-blue-300" id="code4">menu</pre>
          <button class="copy-btn" onclick="copyCode('code4')">کپی</button>
        </div>
      </div>
    </section>

    <!-- حذف اسکریپت -->
    <section class="section-card">
      <h2 class="text-2xl font-bold mb-4">حذف کامل اسکریپت</h2>
      <div class="code-block">
<pre class="text-blue-300" id="code5">sudo systemctl stop traffic_manager.service
sudo systemctl disable traffic_manager.service
sudo rm -rf /var/www/traffic_manager
sudo rm -f /etc/systemd/system/traffic_manager.service
sudo rm -f /usr/local/bin/menu
sudo rm -f /var/log/traffic_manager.log
sudo rm -f /tmp/traffic_manager_test.log
sudo rm -f /tmp/pip_install.log
sudo systemctl daemon-reload
sudo systemctl reset-failed</pre>
        <button class="copy-btn" onclick="copyCode('code5')">کپی</button>
      </div>
    </section>

    <!-- نحوه استفاده -->
    <section class="section-card">
      <h2 class="text-2xl font-bold mb-4">نحوه‌ی اجرا و استفاده</h2>
      <ul class="list-disc list-inside text-gray-300 mb-4">
        <li>اجرای منو: <code class="text-blue-500">menu</code></li>
        <li>نمایش آمار ترافیک: گزینه ۱</li>
        <li>تنظیم نسبت آپلود به دانلود: گزینه ۲</li>
        <li>نمایش آپتایم سرویس: گزینه ۳</li>
        <li>بررسی وضعیت سرویس: گزینه ۴</li>
        <li>فعال/غیرفعال کردن سرویس: گزینه ۵</li>
        <li>خروج از منو: گزینه ۶</li>
      </ul>
    </section>

  </main>

  <script>
    function copyCode(id) {
      const codeElement = document.getElementById(id);
      const text = codeElement.innerText;
      navigator.clipboard.writeText(text).then(() => {
        const cake = document.getElementById('cake');
        cake.style.display = 'block';
        setTimeout(() => {
          cake.style.display = 'none';
        }, 800);
      });
    }
  </script>
</body>
</html>
