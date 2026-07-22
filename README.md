# rom-one-ui-8.5-Samsung-a51-Android-16
 
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dong ROM - Samsung A51</title>
<style>
    :root{
        --bg:#0d0f11;
        --panel:#16191c;
        --panel-alt:#1c2024;
        --line:#262b30;
        --accent:#00c3ff;
        --accent-dim:#0098cc;
        --text:#eaf2f5;
        --text-dim:#9aa7ad;
        --warn:#ffb020;
        --danger:#ff5b5b;
        --ok:#3ddc84;
    }

    *{box-sizing:border-box;}

    body{
        margin:0;
        font-family:'Segoe UI',Arial,sans-serif;
        background:
            radial-gradient(circle at 15% 0%, rgba(0,195,255,0.08), transparent 45%),
            var(--bg);
        color:var(--text);
        min-height:100vh;
    }

    .topbar{
        background:var(--panel-alt);
        border-bottom:1px solid var(--line);
        padding:8px 16px;
        text-align:center;
        font-size:13px;
        color:var(--accent);
        letter-spacing:.5px;
    }

    header{
        background:linear-gradient(180deg,#151a1d,#101315);
        padding:38px 20px 30px;
        text-align:center;
        border-bottom:1px solid var(--line);
    }

    .device-tag{
        display:inline-block;
        font-size:12px;
        letter-spacing:2px;
        text-transform:uppercase;
        color:var(--text-dim);
        border:1px solid var(--line);
        padding:5px 14px;
        border-radius:999px;
        margin-bottom:14px;
    }

    h1{
        margin:0 0 6px;
        font-size:clamp(24px,5vw,34px);
        color:#fff;
        letter-spacing:.5px;
    }
    h1 span{color:var(--accent);}

    header p.sub{
        margin:4px 0 0;
        color:var(--text-dim);
        font-size:15px;
    }

    html{scroll-behavior:smooth;}

    nav{
        display:flex;
        justify-content:center;
        gap:8px;
        background:var(--panel-alt);
        border-bottom:1px solid var(--line);
        padding:10px;
        position:sticky;
        top:0;
        z-index:10;
    }

    nav .tab-btn{
        background:transparent;
        border:1px solid var(--line);
        color:var(--text-dim);
        padding:9px 18px;
        border-radius:8px;
        cursor:pointer;
        font-size:14px;
        font-weight:600;
        transition:.2s;
        display:inline-block;
    }

    nav .tab-btn:hover{
        border-color:var(--accent);
        color:var(--accent);
        background:rgba(0,195,255,0.08);
    }

    .container{
        width:92%;
        max-width:920px;
        margin:auto;
        padding:26px 0 60px;
    }

    .card{
        background:var(--panel);
        border:1px solid var(--line);
        padding:22px 24px;
        margin:20px 0;
        border-radius:14px;
    }

    .card h2{
        margin-top:0;
        font-size:19px;
        color:#fff;
        display:flex;
        align-items:center;
        gap:8px;
    }

    .spec-grid{
        display:grid;
        grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
        gap:10px;
        margin:16px 0;
    }

    .spec{
        background:var(--panel-alt);
        border:1px solid var(--line);
        border-radius:10px;
        padding:10px 12px;
    }
    .spec b{
        display:block;
        font-size:11px;
        color:var(--text-dim);
        text-transform:uppercase;
        letter-spacing:1px;
        margin-bottom:3px;
    }
    .spec span{font-size:14px;}

    p{line-height:1.6; color:#dfe6e9;}

    button.dl{
        background:var(--accent);
        color:#04222b;
        border:none;
        padding:12px 22px;
        border-radius:8px;
        cursor:pointer;
        font-size:15px;
        font-weight:700;
        margin-top:6px;
    }
    button.dl:hover{background:var(--accent-dim); color:#fff;}

    a{text-decoration:none;}

    .badge{
        display:inline-block;
        font-size:11px;
        font-weight:700;
        padding:3px 9px;
        border-radius:999px;
        letter-spacing:.5px;
    }
    .badge.stable{background:rgba(61,220,132,.15); color:var(--ok); border:1px solid rgba(61,220,132,.4);}
    .badge.beta{background:rgba(255,176,32,.15); color:var(--warn); border:1px solid rgba(255,176,32,.4);}

    .steps{
        list-style:none;
        margin:0;
        padding:0;
        counter-reset:step;
        border-left:2px solid var(--line);
        margin-left:14px;
    }

    .steps li{
        position:relative;
        padding:0 0 26px 28px;
        counter-increment:step;
    }

    .steps li::before{
        content:counter(step);
        position:absolute;
        left:-15px;
        top:0;
        width:28px;
        height:28px;
        background:var(--panel);
        border:2px solid var(--accent);
        color:var(--accent);
        border-radius:50%;
        display:flex;
        align-items:center;
        justify-content:center;
        font-size:13px;
        font-weight:700;
    }

    .steps li h3{
        margin:0 0 6px;
        font-size:16px;
        color:#fff;
    }

    .steps li p{margin:0; font-size:14px;}

    .steps li code{
        background:var(--panel-alt);
        border:1px solid var(--line);
        padding:2px 7px;
        border-radius:5px;
        font-size:13px;
        color:var(--accent);
    }

    .warn-box{
        background:rgba(255,176,32,.08);
        border:1px solid rgba(255,176,32,.35);
        border-radius:10px;
        padding:16px 18px;
        margin:20px 0;
    }
    .warn-box b{color:var(--warn);}

    .danger-box{
        background:rgba(255,91,91,.08);
        border:1px solid rgba(255,91,91,.35);
        border-radius:10px;
        padding:16px 18px;
        margin:20px 0;
    }
    .danger-box b{color:var(--danger);}

    footer{
        text-align:center;
        padding:26px 20px;
        color:var(--text-dim);
        border-top:1px solid var(--line);
        font-size:13px;
    }
</style>
</head>
<body>

<div class="topbar">📦 ROM PORT — SAMSUNG GALAXY A51 (SM-A515F) · ANDROID 16</div>

<header>
    <div class="device-tag">Unofficial Build · Community Port</div>
    <h1>📱 Dong <span>ROM</span></h1>
    <p class="sub">ROM port cho Samsung Galaxy A51 — chạy nền tảng Android 16, miễn phí</p>
</header>

<nav>
    <a href="#tai-xuong" class="tab-btn">⬇️ Tải xuống</a>
    <a href="#huong-dan" class="tab-btn">🛠️ Hướng dẫn cài đặt</a>
</nav>

<div class="container">

    <div class="card">
        <h2>ℹ️ Giới thiệu</h2>
        <p>
            Đây là bản ROM port dựa trên nền tảng <b>Android 16</b>, được port từ
            <b>Samsung Galaxy S23 FE</b> về cho <b>Samsung Galaxy A51 (SM-A515F)</b>. ROM tập trung
            vào sự ổn định, mượt mà và giữ nguyên các tính năng cốt lõi của Android gốc, phù hợp cho
            người dùng muốn trải nghiệm phiên bản Android mới nhất trên thiết bị đã hết hỗ trợ cập
            nhật chính hãng.
        </p>
    </div>

    <div id="tai-xuong">
    <div class="card">
        <h2>🚀 One UI 8.5 — Samsung Galaxy A51 <span class="badge stable">Ổn định</span></h2>

            <div class="spec-grid">
                <div class="spec"><b>Model</b><span>SM-A515F</span></div>
                <div class="spec"><b>Port từ</b><span>Samsung S23 FE</span></div>
                <div class="spec"><b>Android</b><span>16</span></div>
                <div class="spec"><b>Phiên bản</b><span>V1.0</span></div>
                <div class="spec"><b>Kernel</b><span>Có sẵn KernelSU</span></div>
                <div class="spec"><b>Root mặc định</b><span>Không (tự bật khi cần)</span></div>
                <div class="spec"><b>OTA</b><span>Không hỗ trợ</span></div>
            </div>

            <p>
                ROM ổn định, <b>không hỗ trợ cập nhật OTA</b> (phải flash thủ công qua TWRP khi có bản mới),
                phù hợp dùng hằng ngày (daily driver). ROM đã tích hợp sẵn <b>KernelSU</b> — máy không root
                mặc định, nhưng chỉ cần cập nhật app KernelSU lên bản mới nhất là có thể root máy, và bật
                quyền Root riêng cho từng ứng dụng theo nhu cầu.
            </p>

            <a href="https://pixeldrain.com/u/rjCbtuzu">
                <button class="dl">⬇️ Tải ROM</button>
            </a>
            <p style="font-size:13px;color:var(--text-dim);margin-top:10px;">
                <b>Cách tải:</b> bấm nút trên để mở Pixeldrain → bấm nút <code>Download</code>
                màu tím ở giữa trang để tải file <code>.zip</code> về máy.
            </p>
        </div>

        <div class="card">
            <h2>🩹 TWRP Recovery <span class="badge stable">Mới nhất</span></h2>
            <p>Bản Recovery mới nhất dành riêng cho A51, dùng để flash ROM, backup và khôi phục dữ liệu.</p>
            <a href="https://drive.google.com/file/d/1H-iS1de9sUiQhZObG9VVl26D6gnoQmO6/view">
                <button class="dl">⬇️ Tải TWRP</button>
            </a>
            <p style="font-size:13px;color:var(--text-dim);margin-top:10px;">
                <b>Cách tải:</b> bấm nút trên để mở Google Drive → bấm biểu tượng
                <code>⬇️ Tải xuống</code> ở góc trên bên phải trang.
            </p>
        </div>

        <div class="card">
            <h2>🧩 Module</h2>
            <p>Module bổ sung cho ROM, tải về và cài đặt theo hướng dẫn kèm theo trong link.</p>
            <a href="https://t.me/icedumbfiles/497">
                <button class="dl">⬇️ Tải Module</button>
            </a>
            <p style="font-size:13px;color:var(--text-dim);margin-top:10px;">
                <b>Cách tải:</b> bấm nút trên để mở kênh Telegram → nhấn vào file đính kèm trong
                tin nhắn rồi chọn <code>Tải xuống</code> (cần cài app Telegram nếu mở trên điện thoại).
            </p>
        </div>

        <div class="warn-box">
            <b>⚠️ Lưu ý:</b> Đây là ROM port không chính thức (unofficial). Hãy sao lưu (backup) toàn bộ
            dữ liệu trước khi flash. Người dùng tự chịu trách nhiệm với thiết bị của mình.
        </div>
    </div>

    <div id="huong-dan">
        <div class="card">
            <h2>🛠️ Hướng dẫn cài đặt ROM cho Samsung A51</h2>
            <p>Làm theo đúng thứ tự các bước bên dưới. Không tắt nguồn hoặc rút cáp giữa chừng khi đang flash.</p>
        </div>

        <div class="danger-box">
            <b>🚫 Trước khi bắt đầu:</b>
            <p style="margin-top:8px;">
                Flash ROM sẽ xoá toàn bộ dữ liệu trên máy (factory reset). Quá trình này có rủi ro
                "brick" thiết bị nếu thực hiện sai bước. Hãy sao lưu ảnh, danh bạ, tin nhắn quan trọng
                sang máy tính hoặc tài khoản đám mây trước khi tiếp tục.
            </p>
        </div>

        <div class="card">
            <h2>📋 Chuẩn bị</h2>
            <ol class="steps">
                <li>
                    <h3>Sạc pin trên 60%</h3>
                    <p>Đảm bảo máy không tắt nguồn đột ngột trong lúc flash.</p>
                </li>
                <li>
                    <h3>Tải đầy đủ file cần thiết</h3>
                    <p>Tải ROM, <code>TWRP Recovery</code>, và Module (nếu cần) từ trang chủ ở trên,
                    lưu vào máy tính.</p>
                </li>
                <li>
                    <h3>Cài Odin trên máy tính</h3>
                    <p>Dùng công cụ <code>Odin</code> (Windows) để flash Recovery vào máy.</p>
                </li>
                <li>
                    <h3>Bật chế độ nhà phát triển</h3>
                    <p>Vào <code>Cài đặt → Giới thiệu điện thoại</code>, chạm liên tục vào
                    "Số hiệu bản dựng" 7 lần, sau đó bật <code>Mở khoá OEM</code> và
                    <code>Gỡ lỗi USB</code> trong mục Tuỳ chọn nhà phát triển.</p>
                </li>
            </ol>
        </div>

        <div class="card">
            <h2>🔓 Bước 1 — Mở khoá Bootloader</h2>
            <ol class="steps">
                <li>
                    <h3>Vào chế độ Download</h3>
                    <p>Tắt máy, sau đó nhấn giữ <code>Volume Down + Power</code> để vào Download Mode,
                    nhấn Volume Up để xác nhận.</p>
                </li>
                <li>
                    <h3>Unlock bootloader</h3>
                    <p>Trong Download Mode, nhấn Volume Up để mở khoá bootloader. Máy sẽ tự khởi động
                    lại và reset dữ liệu.</p>
                </li>
            </ol>
        </div>

        <div class="card">
            <h2>💾 Bước 2 — Flash TWRP Recovery</h2>
            <ol class="steps">
                <li>
                    <h3>Mở Odin, vào lại Download Mode</h3>
                    <p>Kết nối điện thoại với máy tính bằng cáp USB.</p>
                </li>
                <li>
                    <h3>Nạp file TWRP vào Odin</h3>
                    <p>Chọn file TWRP <code>.tar</code> vào mục <code>AP</code> trong Odin.</p>
                </li>
                <li>
                    <h3>Nhấn Start</h3>
                    <p>Chờ đến khi Odin báo <code>PASS</code>, sau đó giữ
                    <code>Volume Up + Power</code> ngay khi màn hình tắt để vào thẳng TWRP,
                    tránh để máy tự boot vào hệ điều hành cũ (sẽ ghi đè TWRP).</p>
                </li>
            </ol>
        </div>

        <div class="card">
            <h2>📲 Bước 3 — Flash ROM Android 16</h2>
            <ol class="steps">
                <li>
                    <h3>Copy file ROM vào máy</h3>
                    <p>Trong TWRP, chọn <code>Mount</code> để kết nối máy với máy tính, copy file
                    ROM <code>.zip</code> vào bộ nhớ máy.</p>
                </li>
                <li>
                    <h3>Wipe dữ liệu</h3>
                    <p>Chọn <code>Wipe → Advanced Wipe</code>, tick chọn
                    <code>Dalvik/ART Cache, Cache, System, Data</code> rồi vuốt để xác nhận.</p>
                </li>
                <li>
                    <h3>Flash ROM</h3>
                    <p>Chọn <code>Install</code>, chọn file ROM vừa copy, vuốt để xác nhận flash.</p>
                </li>
                <li>
                    <h3>Reboot System</h3>
                    <p>Quay lại menu chính TWRP, chọn <code>Reboot → System</code>. Lần khởi động
                    đầu tiên có thể mất 3–5 phút, đây là điều bình thường.</p>
                </li>
            </ol>
        </div>

        <div class="warn-box">
            <b>💡 Mẹo:</b> Nếu máy bị treo logo quá lâu (trên 10 phút), vào lại TWRP và Wipe Cache/Dalvik
            một lần nữa rồi reboot lại. Nếu vẫn không lên, cần flash lại ROM gốc Samsung qua Odin để khôi phục.
        </div>
    </div>

</div>

<footer>
    © 2026 Dong ROM · ROM port cộng đồng cho Samsung Galaxy A51 · Không liên kết với Samsung
</footer>

</body>
</html>
    
        
    

        
