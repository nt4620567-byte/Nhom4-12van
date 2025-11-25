# Nhom4-12van
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nhóm 4 - Bài tập & Thành viên</title>
<style>
  :root{
    --accent:#60a5fa; --bg:#f5f8ff; --card:#ffffff; --muted:#475569; --radius:14px; --maxw:980px;
  }
  *{box-sizing:border-box;}
  body{
    margin:0; font-family:Inter,ui-sans-serif,system-ui,Segoe UI,Roboto,"Helvetica Neue",Arial;
    background: linear-gradient(180deg,var(--bg),#e6eefb);
    color:#0b1220; padding:20px; display:flex; justify-content:center;
  }
  .wrap{width:100%; max-width:var(--maxw);}
  header{display:flex; align-items:center; gap:16px; margin-bottom:22px;}
  .logo{width:86px;height:86px;border-radius:18px;background:linear-gradient(135deg,var(--accent),#7dd3fc);
        display:flex;align-items:center;justify-content:center;font-weight:700;color:#04202a;font-size:18px;}
  h1{margin:0;font-size:26px;}
  p.lead{margin:4px 0 0;color:var(--muted);}
  
  .grid{display:grid; grid-template-columns:1fr 360px; gap:20px;}
  @media(max-width:880px){.grid{grid-template-columns:1fr}.sidebar{order:-1}}

  /* CARD THÀNH VIÊN */
  .member-card{
    display:flex; gap:16px; background:#60a5fa; border-radius:16px;
    padding:18px; margin-bottom:20px; color:#fff; background-size:cover; background-position:center;
  }
  .mc-avatar-img{width:70px;height:70px;border-radius:50%;object-fit:cover;}
  .mc-avatar{width:70px;height:70px;border-radius:50%;background:rgba(0,0,0,0.2);
             display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff;}
  .mc-content h3{margin:0;font-size:18px;}
  .mc-content .mc-role{font-size:14px;}
  .mc-content .mc-about{font-size:14px;margin-top:6px;}

  .card{background:var(--card); padding:18px; border-radius:var(--radius); box-shadow:0 8px 28px rgba(2,6,23,0.06);}
  .section-title{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px;}
  .members{display:flex; flex-direction:column; gap:12px;}
  .list-links{display:grid; grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;}
  .link-btn{display:flex;align-items:center;gap:10px;padding:10px 12px;
    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    border-radius:10px; text-decoration:none; color:inherit; border:1px solid rgba(255,255,255,0.03);}
  .link-btn small{color:var(--muted);}
  .sidebar .card + .card{margin-top:14px;}
  form .row{display:flex; gap:8px;margin-bottom:10px;}
  form input[type=text],form input[type=email],form textarea,form select{
    width:100%; padding:10px 12px; border-radius:10px; border:1px solid rgba(255,255,255,0.04); background:transparent; color:inherit; outline:none
  }
  form textarea{min-height:86px;resize:vertical;}
  button.primary{background:linear-gradient(90deg,var(--accent),#60a5fa); color:#04202a; border:none; padding:10px 14px; border-radius:10px; font-weight:700; cursor:pointer;}
  .footer-note{color:var(--muted); font-size:13px; margin-top:12px;}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <div class="logo">G4</div>
    <div>
      <h1>Nhóm 4</h1>
      <p class="lead">Trang giới thiệu & bài tập</p>
    </div>
  </header>

  <main class="grid">
    <section>
      <!-- CARD THÀNH VIÊN -->
      <div class="card">
        <div class="section-title"><h2>Thành viên</h2></div>
        <div class="members" id="members"></div>
      </div>

      <!-- DANH SÁCH BÀI TẬP -->
      <div class="card" style="margin-top:16px">
        <div class="section-title"><h2>Bài tập & tài liệu</h2></div>
        <div class="list-links" id="links"></div>
      </div>
    </section>

    <!-- FORM GỬI Ý KIẾN -->
    <aside class="sidebar">
      <div class="card">
        <div class="section-title"><h2>Form gửi ý kiến</h2></div>
        <form id="contactForm" onsubmit="return handleSubmit(event)">
          <div class="row"><input type="text" id="name" placeholder="Họ & tên" required></div>
          <div class="row"><input type="email" id="email" placeholder="Email (không bắt buộc)"></div>
          <div class="row"><select id="topic">
            <option value="phanhoi">Phản hồi</option>
            <option value="nopbai">Nộp bài</option>
            <option value="yeucau">Yêu cầu</option>
          </select></div>
          <div class="row"><textarea id="message" placeholder="Nội dung" required></textarea></div>
          <div class="row"><button class="primary" type="submit">Gửi</button></div>
        </form>
      </div>
    </aside>
  </main>
  <footer style="margin-top:22px; text-align:center; color:var(--muted)">© Nhóm 4 • Demo Web</footer>
</div>

<script>
// Dữ liệu thành viên
<style>
/* Tiêu đề */
#wp-products h1 {
    text-align:center;
    color:#243b9a;
    padding: 0 30px;
    margin-top: 40px;
    font-size: 40px;
    font-weight: 700;
}

/* Container */
.container {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
}

/* Khung thẻ */
.card {
    width: 330px;
    background: white;
    padding: 25px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
    transition: 0.3s;
}
.card:hover {
    transform: translateY(-5px);
}

/* Avatar */
.avatar {
    width: 150px;
    height: 150px;
    border-radius: 15px;
    object-fit: cover;
    margin-bottom: 10px;
}

/* Tên */
.card a {
    text-decoration: none;
    font-size: 20px;
    font-weight: 600;
    color: #1a365f;
}
</style>


<!-- Tiêu đề -->
<div id="wp-products">
  <h1>THÀNH VIÊN</h1>
</div>

<!-- Khung chứa thẻ -->
<div class="container" id="member-container"></div>


<script>
// Dữ liệu thành viên
const members = [
  {name:'Nguyễn Huỳnh Đăng Thư', cls:'12 Văn', about:'Tổng hợp nội dung, luôn chill 😎',
   photo:"Đăng Thư.png" class="avatar">, bg:null},

  {name:'Trần Lê Yến Như', cls:'12 Văn', about:'Mang vibe riêng đầy năng lượng ✨',
   photo:"Yến Như.png" class="avatar">, bg:null},

  {name:'Nguyễn Phạm Quế Anh', cls:'12 Văn', about:'Chuyên thiết kế slide & hình ảnh 🎨',
   photo:"Quế Anh.png" class="avatar">, bg:null},

  {name:'Nguyễn Huỳnh Ngọc Châu', cls:'12 Văn', about:'Chịu trách nhiệm kiểm tra bài 📝',
   photo:"Ngọc Châu.png" class="avatar">, bg:null},

  {name:'Đỗ Quốc Việt', cls:'12 Văn', about:'Tìm kiếm tài liệu & tổng hợp 💻',
   photo:"Quốc Việt.png" class="avatar">, bg:null}
];

// Avatar mặc định nếu không có ảnh
const defaultAvatar = "https://cdn-icons-png.flaticon.com/512/6858/6858504.png";


// Tạo giao diện
const container = document.getElementById("member-container");

members.forEach(mem => {
  const card = document.createElement("div");
  card.className = "card";

  card.innerHTML = `
      <img src="${mem.photo ? mem.photo : defaultAvatar}" class="avatar">
      <a href="#" target="_blank">${mem.name}</a>
  `;

  container.appendChild(card);
});
</script>
];

const membersEl = document.getElementById('members');
members.forEach(m=>{
  const card = document.createElement('div');
  card.className='member-card';
  if(m.bg) card.style.backgroundImage=`url(${m.bg})`;
  const avatarHTML = m.photo ? `<img class="mc-avatar-img" src="${m.photo}" alt="${m.name}">` :
    `<div class="mc-avatar">${m.name.split(' ').slice(-1)[0][0]}${m.name.split(' ')[0][0]}</div>`;
  card.innerHTML = `
    ${avatarHTML}
    <div class="mc-content">
      <h3>${m.name}</h3>
      <p class="mc-role">Lớp ${m.cls}</p>
      <p class="mc-about">${m.about}</p>
    </div>`;
  membersEl.appendChild(card);
});

// Dữ liệu bài tập
const links = [
  {title:'Bài 7', href:'https://docs.google.com/document/d/1m_pAeJTqHiUTKwysgXKJ3bCzX8lwi2Yv1XZQs52rP88/edit?usp=drivesdk'},
  {title:'Bài 8', href:'https://docs.google.com/document/d/1MrnnoU4JN_IzSy4xH1nbMDgYQD1JE3fLebK19yrAiR8/edit?usp=drivesdk'},
  {title:'Bài 9', href:'https://docs.google.com/document/d/1FTtAe2Iq_p9j4Z45Em5o9oa_pmdBA1fSOLckO9ltf7I/edit?usp=drivesdk'},
  {title:'Bài 10', href:'https://docs.google.com/document/d/17cf397J36QDESuapkWCTt8-URsjQ4KTPS0GA-4v0QHU/edit?usp=drivesdk'},
  {title:'Bài 11',href:'https://docs.google.com/document/d/11w6pyc9h3xqF6wHZlIJ2K9O7fVp22r7-esO0zK-Ziiw/edit?usp=drivesdk'},
  {title:'Bài 12',href:'https://docs.google.com/document/d/13vb090tUJtHBMC0W6Ib7LANkDbnA5mFGVnMKD1hAOqw/edit?usp=drivesdk'}
];
const linksEl = document.getElementById('links');
links.forEach(l=>{
  const a = document.createElement('a'); a.className='link-btn'; a.href=l.href; a.target='_blank';
  a.innerHTML=`<div style="width:44px;height:44px;border-radius:8px;background:rgba(255,255,255,0.02);display:flex;align-items:center;justify-content:center;font-weight:700">${l.title.split(' ')[1]||l.title}</div>
    <div><div style="font-weight:600">${l.title}</div><small>Mở liên kết</small></div>`;
  linksEl.appendChild(a);
});

// Form xử lý demo
function handleSubmit(e){
  e.preventDefault();
  const name=document.getElementById('name').value.trim();
  const email=document.getElementById('email').value.trim();
  const topic=document.getElementById('topic').value;
  const message=document.getElementById('message').value.trim();
  if(!name||!message){ alert('Vui lòng điền tên và nội dung.'); return false;}
  alert(`Cám ơn ${name}!\nChủ đề: ${topic}\nEmail: ${email||'(không có)'}\nNội dung: ${message.substring(0,120)}${message.length>120?'...':''}`);
  document.getElementById('contactForm').reset();
  return false;
}
</script>
</body>
</html>
