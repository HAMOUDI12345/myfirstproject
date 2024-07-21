<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stop & Shop</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; color: #333; margin: 0; padding: 20px; text-align: center; }
        header { background-color: #0073e6; color: white; padding: 10px 0; }
        h1 { margin: 0; }
        .container { max-width: 800px; margin: 20px auto; padding: 20px; background: white; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .special-offers { margin-top: 20px; }
        .special-offers img { max-width: 80%; height: auto; }
        .opening-date { margin-top: 10px; font-size: 1.2em; color: #555; }
        .login-buttons { margin-top: 20px; }
        .login-buttons a { display: inline-block; padding: 10px 20px; margin: 10px; text-decoration: none; color: white; background-color: #0073e6; border-radius: 4px; }
        .login-buttons a:hover { background-color: #005bb5; }
        .social-links { margin-top: 20px; }
        .social-links a { display: inline-block; margin: 0 10px; text-decoration: none; color: white; padding: 10px 20px; border-radius: 4px; }
        .whatsapp { background-color: #25D366; }
        .facebook { background-color: #3b5998; }
        .tiktok { background-color: #000000; }
        .status { margin-top: 20px; font-size: 1.5em; }
        .open { color: #66ff66; } /* أخضر فاتح */
        .closed { color: red; }
    </style>
</head>
<body>
<header>
    <h1>Stop & Shop</h1>
    <p>حاروف-حي البيدر -الشارع العام</p>
    <p>⏰ ساعات العمل: 8:00 صباحًا - 10:00 مساءً</p>
    <p class="status" id="store-status">مفتوح</p>
    <p id="current-time" class="open"></p>
</header>
<div class="container">
    <h2>مرحبًا بكم في Stop & Shop</h2>
    <div class="special-offers">
        <img src="st2.jpg" alt="صورة السوبر ماركت">
        <div class="opening-date">تاريخ افتتاح السوبر ماركت: 1 يناير 2024</div>
    </div>
    <div class="login-buttons">
        <a href="(stp).html">تسجيل دخول الموظفين</a>
        <a href="(stp1).html">تسجيل دخول الزبائن</a>
        <a href="special-offers.html">العروض الخاصة</a>
    </div>
   
    <div class="social-links">
        <a href="https://chat.whatsapp.com/HuYvdmUf6SpHCzGYK6zkhg" class="whatsapp">WhatsApp</a>
        <a href="https://www.facebook.com/share/SmxyVzbwcnpCYz8x/?mibextid=qi2Omg" class="facebook">Facebook</a>
        <a href="https://www.tiktok.com/@stopandshop75?_t=8o2On8R300z&_r=1" class="tiktok">TikTok</a>
    </div>
</div>
<footer>
    <p>📍 Harouf, Al baydar, Main Street</p>
</footer>

<script>
    function updateTimeAndStatus() {
        const now = new Date();
        const hours = now.getHours();
        const minutes = now.getMinutes();
        const timeString = now.toLocaleTimeString('ar-EG', { hour: '2-digit', minute: '2-digit' });
        
        document.getElementById('current-time').textContent = `الوقت الحالي: ${timeString} / Current Time: ${timeString}`;
        
        const statusElement = document.getElementById('store-status');
        const currentTimeElement = document.getElementById('current-time');
        
        if (hours >= 8 && hours < 22) {
            statusElement.textContent = 'مفتوح / Open';
            statusElement.classList.remove('closed');
            statusElement.classList.add('open');
            currentTimeElement.classList.remove('closed');
            currentTimeElement.classList.add('open');
        } else {
            statusElement.textContent = 'مغلق / Closed';
            statusElement.classList.remove('open');
            statusElement.classList.add('closed');
            currentTimeElement.classList.remove('open');
            currentTimeElement.classList.add('closed');
        }
    }

    setInterval(updateTimeAndStatus, 1000);
    updateTimeAndStatus(); // استدعاء الوظيفة مرة واحدة عند التحميل
</script>

</body>
</html>




