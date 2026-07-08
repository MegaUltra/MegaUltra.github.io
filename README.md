# MegaUltra / OFFICIAL PROJECT
By => DachNima & DachAshkan
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MegaUltra Hacking Group</title>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Reset & Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0a0a0a;
            color: #00ffcc;
            font-family: 'Courier New', monospace;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        /* پس‌زمینه ماتریکسی */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(0deg, rgba(0, 255, 200, 0.02) 0px, rgba(0, 255, 200, 0.02) 2px, transparent 2px, transparent 6px);
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            background: rgba(10, 10, 20, 0.85);
            backdrop-filter: blur(8px);
            border: 1px solid #00ffcc;
            box-shadow: 0 0 40px rgba(0, 255, 200, 0.2), inset 0 0 20px rgba(0, 255, 200, 0.1);
            padding: 30px 25px;
            border-radius: 20px;
            position: relative;
            z-index: 1;
            transition: all 0.3s ease;
        }

        /* هدر نئونی */
        .header {
            text-align: center;
            border-bottom: 2px solid #00ffcc;
            padding-bottom: 20px;
            margin-bottom: 30px;
            position: relative;
        }

        .header h1 {
            font-size: 4rem;
            font-weight: 900;
            letter-spacing: 6px;
            text-shadow: 0 0 20px #00ffcc, 0 0 40px #00ffaa, 0 0 80px #00ff88;
            color: #00ffcc;
            animation: neonPulse 1.8s infinite alternate;
            word-break: break-word;
        }

        @keyframes neonPulse {
            0% { text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffaa; }
            100% { text-shadow: 0 0 30px #00ffcc, 0 0 60px #00ffaa, 0 0 100px #00ff66; }
        }

        .version-badge {
            display: inline-block;
            background: #00ffcc20;
            border: 1px solid #00ffcc;
            padding: 6px 18px;
            border-radius: 40px;
            font-size: 1rem;
            color: #00ffcc;
            letter-spacing: 2px;
            backdrop-filter: blur(4px);
            margin-top: 10px;
        }

        .owners {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin: 15px 0 5px;
            font-size: 1.2rem;
            color: #aaffdd;
        }

        .owners i {
            color: #ffdd55;
            margin-left: 8px;
        }

        .owners span {
            background: #00ffcc10;
            padding: 6px 16px;
            border-radius: 30px;
            border: 1px dashed #00ffcc;
        }

        /* بخش آپلود و فایل‌ها */
        .upload-section {
            background: #0f0f1a;
            padding: 25px;
            border-radius: 16px;
            border: 1px solid #00ffcc55;
            margin-bottom: 35px;
            box-shadow: inset 0 0 30px #00ffcc08;
        }

        .upload-box {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
            justify-content: center;
        }

        .upload-box input[type="file"] {
            display: none;
        }

        .upload-box label {
            background: #00ffcc22;
            border: 2px solid #00ffcc;
            padding: 12px 28px;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
            color: #00ffcc;
            backdrop-filter: blur(4px);
            font-size: 1rem;
        }

        .upload-box label:hover {
            background: #00ffcc;
            color: #0a0a0a;
            box-shadow: 0 0 30px #00ffcc;
        }

        .upload-box button {
            background: transparent;
            border: 2px solid #ffaa00;
            color: #ffaa00;
            padding: 12px 32px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            transition: 0.3s;
            backdrop-filter: blur(4px);
        }

        .upload-box button:hover {
            background: #ffaa00;
            color: #0a0a0a;
            box-shadow: 0 0 30px #ffaa00;
        }

        /* لیست فایل‌ها */
        .file-list {
            margin-top: 30px;
        }

        .file-list h2 {
            color: #ffdd77;
            border-right: 4px solid #00ffcc;
            padding-right: 14px;
            margin-bottom: 20px;
            font-size: 1.8rem;
            text-shadow: 0 0 10px #00ffcc55;
        }

        .file-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 18px;
        }

        .file-card {
            background: #11111e;
            border: 1px solid #00ffcc44;
            border-radius: 14px;
            padding: 16px 18px;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 12px;
            backdrop-filter: blur(2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.6);
        }

        .file-card:hover {
            border-color: #00ffcc;
            transform: scale(1.02);
            box-shadow: 0 0 25px #00ffcc33;
        }

        .file-card i {
            font-size: 2rem;
            color: #00ffcc;
            width: 40px;
            text-align: center;
        }

        .file-card .info {
            flex: 1;
        }

        .file-card .info .name {
            font-weight: bold;
            color: #ccffdd;
            font-size: 1rem;
        }

        .file-card .info .size {
            font-size: 0.8rem;
            color: #88aacc;
        }

        .file-card .download-btn {
            background: none;
            border: 1px solid #00ffcc;
            color: #00ffcc;
            padding: 6px 14px;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
            font-size: 0.85rem;
        }

        .file-card .download-btn:hover {
            background: #00ffcc;
            color: #0a0a0a;
        }

        /* فوتر */
        .footer {
            margin-top: 40px;
            text-align: center;
            border-top: 1px solid #00ffcc33;
            padding-top: 25px;
            font-size: 0.9rem;
            color: #88ddbb;
            letter-spacing: 1px;
        }

        .footer i {
            color: #ff4466;
        }

        /* ریسپانسیو */
        @media (max-width: 700px) {
            .header h1 {
                font-size: 2.8rem;
            }
            .owners {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            .upload-box {
                flex-direction: column;
                width: 100%;
            }
            .upload-box label,
            .upload-box button {
                width: 100%;
                text-align: center;
            }
            .file-grid {
                grid-template-columns: 1fr;
            }
        }

        /* اسکرول بار */
        ::-webkit-scrollbar {
            width: 8px;
            background: #0a0a0a;
        }
        ::-webkit-scrollbar-thumb {
            background: #00ffcc;
            border-radius: 10px;
        }
    </style>
</head>
<body>

<div class="container">

    <!-- Header -->
    <div class="header">
        <h1>⚡MegaUltra⚡</h1>
        <div class="version-badge">
            <i class="fas fa-code"></i> Version 1.0
        </div>
        <div class="owners">
            <span><i class="fas fa-crown"></i> DachAshkan</span>
            <span><i class="fas fa-crown"></i> DachNima</span>
        </div>
        <p style="margin-top: 12px; color: #88ddcc; font-size: 0.95rem;">
            <i class="fas fa-shield-alt"></i> هک &amp; کد · امنیت · آزادی
        </p>
    </div>

    <!-- Upload Section -->
    <div class="upload-section">
        <div class="upload-box">
            <label for="fileInput">
                <i class="fas fa-upload"></i> انتخاب فایل / کد
            </label>
            <input type="file" id="fileInput" multiple>
            <button id="uploadBtn"><i class="fas fa-cloud-upload-alt"></i> آپلود به سرور</button>
        </div>
        <p style="color: #669988; font-size: 0.8rem; margin-top: 12px; text-align: center;">
            <i class="fas fa-lock"></i> فایل‌های آپلود شده در حافظه مرورگر ذخیره می‌شوند (دمو)
        </p>
    </div>

    <!-- File List -->
    <div class="file-list">
        <h2><i class="fas fa-folder-open"></i> مخزن کدها و فایل‌ها</h2>
        <div id="fileGrid" class="file-grid">
            <!-- نمونه فایل‌های پیش‌فرض -->
            <div class="file-card">
                <i class="fas fa-file-code"></i>
                <div class="info">
                    <div class="name">exploit_ssh.py</div>
                    <div class="size">3.2 KB</div>
                </div>
                <button class="download-btn"><i class="fas fa-download"></i></button>
            </div>
            <div class="file-card">
                <i class="fas fa-file-archive"></i>
                <div class="info">
                    <div class="name">tools_2026.zip</div>
                    <div class="size">14.8 MB</div>
                </div>
                <button class="download-btn"><i class="fas fa-download"></i></button>
            </div>
            <div class="file-card">
                <i class="fas fa-file-pdf"></i>
                <div class="info">
                    <div class="name">Hacking_Handbook.pdf</div>
                    <div class="size">2.1 MB</div>
                </div>
                <button class="download-btn"><i class="fas fa-download"></i></button>
            </div>
            <div class="file-card">
                <i class="fas fa-file-alt"></i>
                <div class="info">
                    <div class="name">payload_generator.js</div>
                    <div class="size">1.7 KB</div>
                </div>
                <button class="download-btn"><i class="fas fa-download"></i></button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="footer">
        <i class="fas fa-skull"></i> MegaUltra Underground · <i class="fas fa-terminal"></i> Root Access Only
        <br>
        <span style="font-size: 0.8rem; opacity: 0.7;">© 2026 DachAshkan &amp; DachNima · تمامی حقوق برای هکرهای واقعی محفوظ است</span>
    </div>

</div>

<script>
    (function() {
        // ----- مدیریت آپلود فایل (ذخیره در حافظه مرورگر) -----
        const fileInput = document.getElementById('fileInput');
        const uploadBtn = document.getElementById('uploadBtn');
        const fileGrid = document.getElementById('fileGrid');

        // بارگذاری فایل‌های ذخیره شده از localStorage
        function loadFiles() {
            const stored = localStorage.getItem('megaultra_files');
            if (stored) {
                try {
                    const files = JSON.parse(stored);
                    files.forEach(f => addFileToGrid(f.name, f.size, f.content));
                } catch(e) {}
            }
        }

        // افزودن فایل به گرید (و ذخیره در localStorage)
        function addFileToGrid(name, size, content) {
            // ساخت کارت جدید
            const card = document.createElement('div');
            card.className = 'file-card';

            const icon = document.createElement('i');
            icon.className = 'fas fa-file-code';
            card.appendChild(icon);

            const info = document.createElement('div');
            info.className = 'info';
            const nameDiv = document.createElement('div');
            nameDiv.className = 'name';
            nameDiv.textContent = name;
            const sizeDiv = document.createElement('div');
            sizeDiv.className = 'size';
            sizeDiv.textContent = size;
            info.appendChild(nameDiv);
            info.appendChild(sizeDiv);
            card.appendChild(info);

            const downloadBtn = document.createElement('button');
            downloadBtn.className = 'download-btn';
            downloadBtn.innerHTML = '<i class="fas fa-download"></i>';
            downloadBtn.addEventListener('click', function(e) {
                e.stopPropagation();
                // دانلود فایل (با محتوای ذخیره شده)
                if (content) {
                    const blob = new Blob([content], { type: 'application/octet-stream' });
                    const url = URL.createObjectURL(blob);
                    const a = document.createElement('a');
                    a.href = url;
                    a.download = name;
                    document.body.appendChild(a);
                    a.click();
                    document.body.removeChild(a);
                    URL.revokeObjectURL(url);
                } else {
                    alert('محتوای فایل در دسترس نیست (دمو)');
                }
            });
            card.appendChild(downloadBtn);

            fileGrid.appendChild(card);
        }

        // ذخیره لیست فایل‌ها در localStorage
        function saveFilesToStorage() {
            const cards = fileGrid.querySelectorAll('.file-card');
            const filesArray = [];
            cards.forEach(card => {
                const name = card.querySelector('.name')?.textContent || 'unknown';
                const size = card.querySelector('.size')?.textContent || '0 KB';
                // محتوای ساختگی (برای دمو)
                const content = `MegaUltra File: ${name} - generated by DachAshkan & DachNima`;
                filesArray.push({ name, size, content });
            });
            localStorage.setItem('megaultra_files', JSON.stringify(filesArray));
        }

        // آپلود فایل‌های انتخاب شده
        uploadBtn.addEventListener('click', function() {
            if (fileInput.files.length === 0) {
                alert('لطفاً حداقل یک فایل انتخاب کنید.');
                return;
            }

            Array.from(fileInput.files).forEach(file => {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const content = e.target.result;
                    const size = (file.size / 1024).toFixed(1) + ' KB';
                    if (file.size > 1024*1024) {
                        const sizeMB = (file.size / (1024*1024)).toFixed(1) + ' MB';
                        addFileToGrid(file.name, sizeMB, content);
                    } else {
                        addFileToGrid(file.name, size, content);
                    }
                    saveFilesToStorage();
                };
                reader.readAsText(file);
            });

            // ریست اینپوت
            fileInput.value = '';
        });

        // بارگذاری اولیه
        loadFiles();

        // در صورت تغییر گرید (برای دمو) هر بار ذخیره شود
        // (در عمل با آپلود جدید ذخیره می‌شود)

        // اضافه کردن قابلیت حذف با دابل کلیک (برای ادمین‌ها)
        fileGrid.addEventListener('dblclick', function(e) {
            const card = e.target.closest('.file-card');
            if (card) {
                if (confirm('آیا فایل مورد نظر حذف شود؟ (فقط برای ادمین)')) {
                    card.remove();
                    saveFilesToStorage();
                }
            }
        });

        // نمایش پیام خوش‌آمدگویی در کنسول (هکری)
        console.log('%cMegaUltra Hacking Group', 'font-size:24px; color:#00ffcc; font-weight:bold;');
        console.log('%cOwners: DachAshkan & DachNima', 'font-size:16px; color:#ffaa00;');
        console.log('%cVersion 1.0 - Ready for action', 'font-size:14px; color:#88ddbb;');
    })();
</script>

</body>
</html>
