<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Đếm Ngược Tết 2026 - Tùng hẹ hẹ</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            background: radial-gradient(circle, #b71c1c, #2a0000);
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-family: 'Segoe UI', Arial, sans-serif;
            overflow: hidden;
            color: #ffd700;
        }

        /* TRANG TRÍ CỐ ĐỊNH (KHÔNG RƠI) */
        .decor {
            position: absolute;
            font-size: 3.5rem;
            z-index: 5;
            pointer-events: none;
        }
        .t-l { top: 20px; left: 20px; }
        .t-r { top: 20px; right: 20px; }
        .b-l { bottom: 20px; left: 20px; }
        .b-r { bottom: 20px; right: 20px; }

        h1 {
            font-size: 1.8rem;
            text-transform: uppercase;
            margin-bottom: 40px;
            letter-spacing: 2px;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
        }

        .countdown {
            display: flex;
            gap: 15px;
            z-index: 10;
        }

        .box {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        /* KHUNG CHỨA SỐ */
        .num-card {
            background-color: #d32f2f;
            width: 60px; 
            height: 75px; 
            border-radius: 8px;
            border: 2px solid #ffd700;
            box-shadow: 0 5px 15px rgba(0,0,0,0.4);
            position: relative;
            overflow: hidden; /* Cắt phần số đang rơi */
        }

        .num {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: bold;
            color: white;
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* Trạng thái số cũ bay xuống dưới */
        .num-old { transform: translateY(100%); }
        /* Trạng thái số mới nằm giữa */
        .num-current { transform: translateY(0); }
        /* Trạng thái số tiếp theo đợi ở trên */
        .num-next { transform: translateY(-100%); }

        .label {
            font-size: 0.7rem;
            font-weight: bold;
            text-transform: uppercase;
            color: #ffd700;
        }

        .cre {
            margin-top: 60px;
            font-size: 1.1rem;
            font-weight: bold;
        }

        /* HOA MAI RƠI (DUY NHẤT RƠI) */
        .flower {
            position: absolute;
            top: -10%;
            z-index: 1;
            animation: fall linear infinite;
        }
        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }
    </style>
</head>
<body>

    <div class="decor t-l">🌸</div>
    <div class="decor t-r">🌼</div>
    <div class="decor b-l">🧧</div>
    <div class="decor b-r">🍉</div>

    <h1>TẾT BÍNH NGỌ 2026</h1>

    <div class="countdown">
        <div class="box">
            <div class="num-card" id="d-card"><div class="num num-current">00</div></div>
            <div class="label">Ngày</div>
        </div>
        <div class="box">
            <div class="num-card" id="h-card"><div class="num num-current">00</div></div>
            <div class="label">Giờ</div>
        </div>
        <div class="box">
            <div class="num-card" id="m-card"><div class="num num-current">00</div></div>
            <div class="label">Phút</div>
        </div>
        <div class="box">
            <div class="num-card" id="s-card"><div class="num num-current">00</div></div>
            <div class="label">Giây</div>
        </div>
    </div>

    <div class="cre">By: <strong>Tùng hẹ hẹ</strong> 🧧</div>

    <script>
        const target = new Date("Feb 17, 2026 00:00:00").getTime();

        function update() {
            const now = new Date().getTime();
            const diff = target - now;

            const d = Math.floor(diff / (1000 * 60 * 60 * 24));
            const h = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const m = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const s = Math.floor((diff % (1000 * 60)) / 1000);

            animate("d", d);
            animate("h", h);
            animate("m", m);
            animate("s", s);
        }

        function animate(id, value) {
            const card = document.getElementById(id + "-card");
            const currentNum = card.querySelector(".num-current");
            const valStr = value < 10 ? "0" + value : value;

            if (currentNum.innerText !== String(valStr)) {
                // Tạo số mới nằm đợi ở trên
                const nextNum = document.createElement("div");
                nextNum.classList.add("num", "num-next");
                nextNum.innerText = valStr;
                card.appendChild(nextNum);

                // Chạy hiệu ứng sau 1 frame
                setTimeout(() => {
                    currentNum.classList.replace("num-current", "num-old");
                    nextNum.classList.replace("num-next", "num-current");
                }, 20);

                // Xóa số cũ sau khi ẩn hẳn
                setTimeout(() => {
                    currentNum.remove();
                }, 500);
            }
        }

        setInterval(update, 1000);
        update();

        // Hiệu ứng hoa rơi
        function createFlower() {
            const f = document.createElement('div');
            f.className = 'flower';
            f.innerHTML = Math.random() > 0.5 ? '🌸' : '🌼';
            f.style.left = Math.random() * 100 + 'vw';
            f.style.animationDuration = Math.random() * 3 + 2 + 's';
            f.style.fontSize = Math.random() * 10 + 15 + 'px';
            document.body.appendChild(f);
            setTimeout(() => f.remove(), 5000);
        }
        setInterval(createFlower, 400);
    </script>
</body>
</html>

