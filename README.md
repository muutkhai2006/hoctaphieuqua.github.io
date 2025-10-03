<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cách Học Tập Hiệu Quả Cho Sinh Viên</title>
  <meta name="description" content="Tóm tắt chiến lược học tập hiệu quả: mục tiêu SMART, Pomodoro, Active Recall, Spaced Repetition, ghi chú Cornell, học nhóm, sức khỏe và quản lý số." />
  <style>
    :root{
      --accent:#2563eb;
      --accent-2:#0ea5e9;
      --bg:#0b1220;
      --card:#0f172a;
      --text:#e5e7eb;
      --muted:#94a3b8;
      --ok:#10b981;
      --warn:#f59e0b;
      --danger:#ef4444;
      --ring:rgba(37,99,235,.35);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:system-ui,-apple-system,Segoe UI,Roboto,Inter,Helvetica,Arial,sans-serif;
      color:var(--text);
      background:
        radial-gradient(1200px 600px at 10% -10%, rgba(37,99,235,.15), transparent 60%),
        radial-gradient(900px 500px at 90% 10%, rgba(14,165,233,.12), transparent 60%),
        linear-gradient(180deg,#0a0f1d 0%, #0b1220 60%, #0b1220 100%);
      line-height:1.6;
    }
    .wrap{
      max-width:980px;
      margin:0 auto;
      padding:24px;
    }
    header.hero{
      border:1px solid rgba(148,163,184,.2);
      background:linear-gradient(180deg,rgba(15,23,42,.7),rgba(15,23,42,.45));
      border-radius:20px;
      padding:28px;
      backdrop-filter: blur(6px);
      box-shadow: 0 20px 50px rgba(2,6,23,.45);
      position:relative;
      overflow:hidden;
    }
    .chip{
      display:inline-flex;gap:8px;align-items:center;
      background:rgba(37,99,235,.15);
      border:1px solid rgba(37,99,235,.35);
      color:#cfe0ff;
      padding:6px 10px;border-radius:999px;
      font-size:14px;
    }
    h1{font-size:clamp(28px,4.6vw,40px);margin:12px 0 8px;line-height:1.15}
    p.lead{color:var(--muted);font-size:clamp(15px,2.2vw,18px);margin:0}
    .grid{
      display:grid;
      grid-template-columns:repeat(12,1fr);
      gap:18px;
      margin-top:24px;
    }
    .card{
      background:var(--card);
      border:1px solid rgba(148,163,184,.15);
      border-radius:16px;
      padding:18px;
      box-shadow:0 10px 30px rgba(2,6,23,.35);
    }
    .span-6{grid-column:span 6}
    .span-4{grid-column:span 4}
    .span-8{grid-column:span 8}
    .span-12{grid-column:span 12}
    @media (max-width:900px){
      .span-6,.span-4,.span-8,.span-12{grid-column:1 / -1}
    }
    h2{font-size:22px;margin:0 0 8px}
    .muted{color:var(--muted)}
    ul.clean{margin:8px 0 0 0;padding:0;list-style:none;display:grid;gap:8px}
    ul.clean li{display:flex;gap:10px;align-items:flex-start}
    .tick{font-weight:700;color:var(--ok)}
    .warn{color:var(--warn);font-weight:700}
    .bad {color:var(--danger);font-weight:700}
    .pill{
      display:inline-block;
      padding:4px 10px;border-radius:999px;
      border:1px solid rgba(148,163,184,.25);
      color:#dbeafe;background:rgba(30,64,175,.25);
      font-size:12px;margin-right:8px
    }
    .kbd{
      border:1px solid rgba(148,163,184,.35);
      background:rgba(15,23,42,.7);
      padding:2px 6px;border-radius:6px;font-family:ui-monospace,SFMono-Regular,Menlo,monospace
    }
    .progress{
      height:10px;border-radius:999px;background:#111827;border:1px solid rgba(148,163,184,.2);
      overflow:hidden
    }
    .progress>div{
      height:100%;
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      width:0%
    }
    .steps{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
    .step{
      flex:1 1 220px;background:rgba(148,163,184,.08);
      border:1px dashed rgba(148,163,184,.25);border-radius:12px;padding:10px
    }
    .footnotes{font-size:14px;color:var(--muted)}
    .bar{
      display:flex;gap:8px;margin-top:8px
    }
    .bar div{
      flex:1;height:8px;border-radius:6px;background:rgba(148,163,184,.18)
    }
    .bar div.on{background:linear-gradient(90deg,#22c55e,#84cc16)}
    .cta{
      display:flex;gap:12px;flex-wrap:wrap;margin-top:14px
    }
    .btn{
      display:inline-flex;align-items:center;gap:10px;
      background:linear-gradient(180deg,#1e3a8a,#1d4ed8);
      border:1px solid rgba(37,99,235,.65);
      padding:10px 14px;border-radius:12px;color:white;
      text-decoration:none;cursor:pointer;font-weight:600
    }
    .btn.secondary{
      background:transparent;border-color:rgba(148,163,184,.35);
      color:#cbd5e1
    }
    .btn:focus,.btn:hover{
      outline: none; box-shadow:0 0 0 6px var(--ring)
    }
    .checklist{
      display:grid;gap:8px;margin-top:8px
    }
    .item{
      display:flex;gap:10px;align-items:center;justify-content:space-between;
      padding:10px;border:1px solid rgba(148,163,184,.2);border-radius:12px;
      background:rgba(15,23,42,.6)
    }
    .item label{display:flex;gap:10px;align-items:center;cursor:pointer}
    .item input{width:18px;height:18px}
    .small{font-size:12px;color:var(--muted)}
    .to-top{
      position:fixed;right:16px;bottom:16px;z-index:50;
      opacity:0;transform:translateY(10px);
      transition:.2s ease;pointer-events:none
    }
    .to-top.show{opacity:1;transform:none;pointer-events:auto}
    footer{margin:24px 0 8px;text-align:center;color:var(--muted);font-size:14px}
  </style>
</head>
<body>
  <div class="wrap">
    <header class="hero">
      <span class="chip">📚 Lộ trình học thông minh cho sinh viên</span>
      <h1>Cách Học Tập Hiệu Quả: Ngắn gọn – Dễ áp dụng – Bền bỉ</h1>
      <p class="lead">Tập trung vào 7 mảnh ghép: mục tiêu <b>SMART</b>, kỹ thuật <b>Pomodoro</b>, <b>Active Recall</b>, <b>Spaced Repetition</b>, ghi chú <b>Cornell</b>, học nhóm thông minh, và sức khỏe – <i>vì não cũng cần “bảo trì”.</i></p>
      <div class="cta">
        <a class="btn" href="#plan">Bắt đầu lập kế hoạch</a>
        <a class="btn secondary" href="#tips">Xem mẹo nhanh</a>
      </div>
    </header>

    <section id="plan" class="grid">
      <article class="card span-8">
        <h2>1) Đặt mục tiêu theo SMART</h2>
        <p class="muted">Cụ thể – Đo được – Khả thi – Thực tế – Có hạn.</p>
        <ul class="clean">
          <li><span class="tick">✓</span><b>Cụ thể:</b> “Hoàn thành 200 câu SQL cơ bản” thay vì “Học SQL”.</li>
          <li><span class="tick">✓</span><b>Đo được:</b> Theo dõi số câu/ngày & điểm quiz.</li>
          <li><span class="tick">✓</span><b>Khả thi:</b> Vừa sức thời gian & nền tảng.</li>
          <li><span class="tick">✓</span><b>Thực tế:</b> Bám sát đề cương & lịch kiểm tra.</li>
          <li><span class="tick">✓</span><b>Hạn chót:</b> Chia mốc tuần/ngày để tiến độ “chạy”.</li>
        </ul>
        <div class="steps">
          <div class="step"><span class="pill">Ví dụ</span>“Tuần này hoàn tất Chương 3–4 CSDL + 2 bài lab.”</div>
          <div class="step">Chia mục tiêu lớn → công việc 25–50 phút.</div>
          <div class="step">Cuối ngày: rà soát 5′ để cập nhật tiến độ.</div>
        </div>
        <div style="margin-top:12px">
          <div class="small">Tiến độ hôm nay</div>
          <div class="progress" aria-label="Tiến độ">
            <div id="progressBar"></div>
          </div>
        </div>
      </article>

      <aside class="card span-4">
        <h2>Checklist khởi động</h2>
        <div class="checklist">
          <div class="item">
            <label><input type="checkbox" class="ck" /> Mục tiêu ngày đã rõ ràng</label>
            <span class="small">SMART</span>
          </div>
          <div class="item">
            <label><input type="checkbox" class="ck" /> Tắt thông báo 60 phút</label>
            <span class="small">Deep Work</span>
          </div>
          <div class="item">
            <label><input type="checkbox" class="ck" /> Sẵn tài liệu/đề cương</label>
            <span class="small">Chuẩn bị</span>
          </div>
          <div class="item">
            <label><input type="checkbox" class="ck" /> Nước + ghi chú</label>
            <span class="small">Focus kit</span>
          </div>
        </div>
      </aside>
    </section>

    <section id="tips" class="grid" style="margin-top:6px">
      <article class="card span-6">
        <h2>2) Kỹ thuật Pomodoro 25–5</h2>
        <p class="muted">25′ tập trung, 5′ nghỉ; 4 phiên nghỉ dài 15–20′.</p>
        <ul class="clean">
          <li><span class="tick">✓</span><b>Trước khi bắt đầu:</b> bật hẹn giờ, dọn nhiễu.</li>
          <li><span class="tick">✓</span><b>Trong 25′:</b> chỉ 1 việc duy nhất.</li>
          <li><span class="tick">✓</span><b>Nghỉ 5′:</b> đi lại, giãn cổ vai, không TikTok.</li>
        </ul>
        <div class="bar" aria-hidden="true">
          <div class="on"></div><div class="on"></div><div></div><div></div><div></div>
        </div>
      </article>

      <article class="card span-6">
        <h2>3) Active Recall & Spaced Repetition</h2>
        <p class="muted">Tự kéo kiến thức ra khỏi trí nhớ và nhắc lại theo lịch.</p>
        <ul class="clean">
          <li><span class="tick">✓</span><b>Active Recall:</b> tự đặt câu hỏi, che đáp án rồi trả lời.</li>
          <li><span class="tick">✓</span><b>Spaced:</b> nhắc lại sau 1–3–7–14 ngày.</li>
          <li><span class="warn">●</span><b>Tránh:</b> đọc lại thụ động, tô highlight quá đà.</li>
        </ul>
      </article>

      <article class="card span-4">
        <h2>4) Ghi chú Cornell</h2>
        <p class="muted">Trang ghi chú chia 3 vùng: Key | Notes | Summary.</p>
        <ul class="clean">
          <li><span class="tick">✓</span>Trái: từ khóa/câu hỏi</li>
          <li><span class="tick">✓</span>Phải: nội dung chính</li>
          <li><span class="tick">✓</span>Dưới: tóm tắt 3–5 dòng</li>
        </ul>
      </article>

      <article class="card span-4">
        <h2>5) Học nhóm “thông minh”</h2>
        <ul class="clean">
          <li><span class="tick">✓</span>Mỗi buổi 1 mục tiêu rõ ràng.</li>
          <li><span class="tick">✓</span>Đổi vai: 1 người giải thích, 1 người chất vấn.</li>
          <li><span class="tick">✓</span>Kết thúc: mỗi người viết lại “điều học được”.</li>
        </ul>
      </article>

      <article class="card span-4">
        <h2>6) Quản lý “số” & môi trường</h2>
        <ul class="clean">
          <li><span class="tick">✓</span>Chặn mạng xã hội trong giờ học.</li>
          <li><span class="tick">✓</span>Màn hình, bàn ghế ở tầm mắt; ánh sáng đủ.</li>
          <li><span class="bad">×</span>Đa nhiệm nhiều cửa sổ cùng lúc.</li>
        </ul>
      </article>

      <article class="card span-12">
        <h2>7) Sức khỏe học đường</h2>
        <ul class="clean">
          <li><span class="tick">✓</span>Ngủ 7–8h; hạn chế thức khuya trước bài thi.</li>
          <li><span class="tick">✓</span>Uống nước, vận động nhẹ mỗi 60–90′.</li>
          <li><span class="tick">✓</span>Bữa ăn cân bằng: protein, rau, tinh bột chậm.</li>
        </ul>
        <p class="footnotes">Gợi ý nhịp ngày: 2–3 khối học sâu (Deep Work) × 60–90′ + luyện tập ngắn 15–30′ vào chiều/tối để nhắc lại.</p>
      </article>
    </section>

    <section class="grid" style="margin-top:6px">
      <article class="card span-8">
        <h2>Mẫu lịch “1 tuần chuẩn”</h2>
        <p class="muted">Tùy biến theo học phần và lịch thi của bạn.</p>
        <ul class="clean">
          <li><span class="pill">Sáng</span> 2 phiên Pomodoro cho môn khó nhất.</li>
          <li><span class="pill">Chiều</span> Lab/thực hành + làm bài tập.</li>
          <li><span class="pill">Tối</span> 20′ nhắc lại (Spaced) + 10′ điều chỉnh kế hoạch.</li>
        </ul>
      </article>
      <aside class="card span-4">
        <h2>Tài nguyên nhanh</h2>
        <ul class="clean">
          <li><span class="kbd">Ctrl</span> + <span class="kbd">F</span> tìm từ khóa nhanh trong PDF.</li>
          <li><span class="kbd">Alt</span> + <span class="kbd">Tab</span> chuyển cửa sổ tập trung.</li>
          <li>Đặt “chế độ máy bay” cho giờ Deep Work.</li>
        </ul>
      </aside>
    </section>

    <footer>
      © 2025 – Gợi ý học tập cho sinh viên. Chúc bạn học tốt!
    </footer>
  </div>

  <a id="toTop" class="btn to-top" href="#top" aria-label="Lên đầu trang">⬆ Lên đầu</a>

  <script>
    // Tiến độ minh họa: dựa số mục đã tick trong checklist
    const checks = document.querySelectorAll('.ck');
    const bar = document.getElementById('progressBar');
    function updateProgress(){
      const total = checks.length;
      const done = [...checks].filter(c=>c.checked).length;
      const percent = Math.round((done/total)*100);
      bar.style.width = percent + '%';
      bar.setAttribute('aria-valuenow', percent);
      bar.title = percent + '%';
    }
    checks.forEach(c=>c.addEventListener('change', updateProgress));
    updateProgress();

    // Nút lên đầu trang
    const toTop = document.getElementById('toTop');
    const onScroll = () => {
      if(window.scrollY > 250){
        toTop.classList.add('show');
      }else{
        toTop.classList.remove('show');
      }
    };
    window.addEventListener('scroll', onScroll);

    // Cuộn mượt cho các anchor
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id = a.getAttribute('href');
        const el = document.querySelector(id);
        if(el){
          e.preventDefault();
          el.scrollIntoView({behavior:'smooth', block:'start'});
          history.pushState(null,'',id);
        }
      })
    });
  </script>
</body>
</html>
