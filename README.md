<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Business Card</title>
    <style>
        body {
            background-color: #0b0b0f;
            color: white;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }
        .card {
            background-color: #12121a;
            border: 1px solid #222230;
            border-radius: 12px;
            padding: 24px;
            width: 100%;
            max-width: 360px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
        }
        .header {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 20px;
            text-align: center;
            color: #a5b4fc;
        }
        .item {
            display: flex;
            align-items: center;
            margin-bottom: 16px;
            font-size: 16px;
            word-break: break-all;
        }
        .icon {
            margin-right: 12px;
            font-size: 20px;
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="header">Digital Business Card</div>
        <div class="item"><span class="icon">👤</span><span id="name">Loading...</span></div>
        <div class="item"><span class="icon">📞</span><span id="phone">Loading...</span></div>
        <div class="item"><span class="icon">✉️</span><span id="email">Loading...</span></div>
        <div class="item"><span class="icon">💼</span><span id="company">Loading...</span></div>
    </div>

    <script>
        const params = new URLSearchParams(window.location.search);
        document.getElementById('name').textContent = params.get('name') || 'N/A';
        document.getElementById('phone').textContent = params.get('phone') || 'N/A';
        document.getElementById('email').textContent = params.get('email') || 'N/A';
        document.getElementById('company').textContent = params.get('company') || 'N/A';
    </script>
</body>
</html>
