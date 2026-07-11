index.html<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>أكاديمية الشاطبي لتعليم القرآن والقراءات</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Aref+Ruqaa:wght@400;700&family=Tajawal:wght@300;400;500;700;900&display=swap" rel="stylesheet">
<style>
  :root{
    --parchment:#F4ECD8;
    --parchment-deep:#E8DBB8;
    --ink:#241B12;
    --emerald:#16433A;
    --emerald-deep:#0D2B25;
    --gold:#B88A3D;
    --gold-bright:#D4AF63;
    --thread:rgba(184,138,61,.35);
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--parchment);
    background-image:
      radial-gradient(ellipse at 10% 0%, rgba(184,138,61,.08), transparent 50%),
      radial-gradient(ellipse at 90% 100%, rgba(22,67,58,.06), transparent 50%);
    color:var(--ink);
    font-family:'Tajawal',sans-serif;
    overflow-x:hidden;
  }
  .display{font-family:'Aref Ruqaa',serif;}

  body::before{
    content:"";position:fixed;inset:0;pointer-events:none;opacity:.05;
    background-image:repeating-linear-gradient(0deg,transparent,transparent 2px,#000 2px,#000 3px);
    z-index:1;
  }

  header{
    position:sticky;top:0;z-index:50;
    background:linear-gradient(180deg,rgba(244,236,216,.97),rgba(244,236,216,.9));
    backdrop-filter:blur(6px);border-bottom:1px solid var(--thread);
  }
  .nav-wrap{
    max-width:1180px;margin:0 auto;
    display:flex;align-items:center;justify-content:space-between;
    padding:16px 28px;
  }
  .brand{display:flex;align-items:center;gap:12px;}
  .brand-mark{
    width:42px;height:42px;border-radius:50%;
    background:radial-gradient(circle at 30% 30%,var(--gold-bright),var(--gold) 70%);
    display:flex;align-items:center;justify-content:center;
    font-family:'Aref Ruqaa',serif;color:var(--emerald-deep);font-weight:700;font-size:20px;
    box-shadow:0 2px 8px rgba(0,0,0,.2);
  }
  .brand-text{font-family:'Aref Ruqaa',serif;font-size:22px;color:var(--emerald-deep);font-weight:700;}
  nav ul{display:flex;gap:28px;list-style:none;}
  nav a{color:var(--ink);text-decoration:none;font-size:15px;font-weight:500;opacity:.8;transition:opacity .2s;}
  nav a:hover{opacity:1;color:var(--gold);}
  .nav-cta{
    background:var(--emerald-deep);color:var(--parchment);
    padding:9px 22px;border-radius:3px;font-size:14px;font-weight:700;
    border:1px solid var(--gold);cursor:pointer;text-decoration:none;
  }
  .menu-toggle{display:none;font-size:24px;background:none;border:none;color:var(--emerald-deep);cursor:pointer;}

  .hero{
    position:relative;z-index:2;max-width:980px;margin:0 auto;
    padding:90px 28px 60px;text-align:center;
  }
  .hero-eyebrow{
    display:inline-flex;align-items:center;gap:10px;
    font-size:13px;letter-spacing:.12em;color:var(--gold);margin-bottom:28px;font-weight:700;
  }
  .hero-eyebrow::before,.hero-eyebrow::after{content:"";width:30px;height:1px;background:var(--gold);}
  .hero h1{
    font-family:'Aref Ruqaa',serif;font-size:clamp(40px,7vw,68px);
    line-height:1.25;color:var(--emerald-deep);margin-bottom:22px;
  }
  .ayah{
    font-family:'Aref Ruqaa',serif;font-size:clamp(20px,3vw,28px);color:var(--gold);
    border-top:1px solid var(--thread);border-bottom:1px solid var(--thread);
    padding:22px 10px;margin:34px auto 18px;max-width:680px;line-height:2;
  }
  .ayah span{font-size:13px;color:var(--ink);opacity:.55;font-family:'Tajawal';display:block;margin-top:10px;}
  .hero p.lead{font-size:17px;color:var(--ink);opacity:.75;max-width:560px;margin:0 auto;line-height:1.9;}

  .section-head{
    max-width:1180px;margin:0 auto;padding:0 28px;
    display:flex;align-items:baseline;gap:18px;margin-bottom:8px;
  }
  .section-num{font-family:'Aref Ruqaa',serif;font-size:46px;color:var(--gold);opacity:.5;line-height:1;}
  .section-titles h2{font-family:'Aref Ruqaa',serif;font-size:32px;color:var(--emerald-deep);}
  .section-titles p{font-size:14px;color:var(--ink);opacity:.6;margin-top:4px;}

  .khazana{max-width:1180px;margin:60px auto 100px;padding:0 28px;}

  .catalog{
    display:grid;grid-template-columns:repeat(5,1fr);gap:0;
    border:1px solid var(--thread);border-radius:4px;overflow:hidden;
    background:rgba(255,252,242,.5);
  }
  .card{
    position:relative;padding:34px 18px 26px;border-left:1px solid var(--thread);
    min-height:260px;display:flex;flex-direction:column;
    transition:background .25s,transform .25s;
  }
  .catalog .card:first-child{border-left:none;}
  .card:hover{background:rgba(184,138,61,.08);transform:translateY(-4px);}
  .card .tab{
    position:absolute;top:0;right:18px;width:34px;height:14px;
    background:var(--gold);border-radius:0 0 4px 4px;opacity:.85;
  }
  .card .num{font-family:'Aref Ruqaa',serif;font-size:13px;color:var(--gold);letter-spacing:.1em;margin-bottom:16px;margin-top:6px;}
  .card .icon{font-size:30px;margin-bottom:14px;}
  .card h3{font-size:16px;font-weight:700;color:var(--emerald-deep);line-height:1.5;margin-bottom:8px;}
  .card .desc{font-size:13px;color:var(--ink);opacity:.6;line-height:1.7;flex-grow:1;}
  .reg-btn{
    display:inline-block;margin-top:14px;
    background:var(--emerald-deep);color:var(--gold-bright);
    font-size:13px;font-weight:700;padding:8px 16px;border-radius:3px;
    text-decoration:none;border:1px solid var(--gold);transition:opacity .2s;
    text-align:center;
  }
  .reg-btn:hover{opacity:.85;}

  .emerald-band{
    background:linear-gradient(135deg,var(--emerald-deep),var(--emerald));
    color:var(--parchment);padding:70px 28px;text-align:center;position:relative;
  }
  .emerald-band::before,.emerald-band::after{
    content:"";position:absolute;left:0;right:0;height:6px;
    background:repeating-linear-gradient(90deg,var(--gold) 0 14px,transparent 14px 28px);
  }
  .emerald-band::before{top:0;}
  .emerald-band::after{bottom:0;}
  .emerald-band h2{font-family:'Aref Ruqaa',serif;font-size:30px;margin-bottom:14px;}
  .emerald-band p{opacity:.8;max-width:520px;margin:0 auto 26px;font-size:15px;}
  .btn-light{
    background:var(--gold-bright);color:var(--emerald-deep);
    padding:13px 34px;border-radius:3px;font-weight:700;
    border:none;cursor:pointer;font-size:15px;text-decoration:none;display:inline-block;
  }

  footer{
    max-width:1180px;margin:0 auto;padding:50px 28px 30px;
    display:flex;justify-content:space-between;flex-wrap:wrap;gap:20px;
    font-size:13px;color:var(--ink);opacity:.55;
  }

  @media(max-width:880px){
    .catalog{grid-template-columns:repeat(2,1fr);}
    .card{border-left:1px solid var(--thread);}
    .catalog .card:nth-child(odd){border-left:none;}
    nav ul,.nav-cta{display:none;}
    .menu-toggle{display:block;}
  }
  @media(max-width:480px){
    .catalog{grid-template-columns:1fr;}
    .catalog .card{border-left:none !important;border-top:1px solid var(--thread);}
    .catalog .card:first-child{border-top:none;}
  }
</style>
</head>
<body>

<header>
  <div class="nav-wrap">
    <div class="brand">
      <div class="brand-mark">ش</div>
      <div class="brand-text">أكاديمية الشاطبي</div>
    </div>
    <nav>
      <ul>
        <li><a href="#halaqat">الحلقات</a></li>
        <li><a href="#kutub">الكتب</a></li>
        <li><a href="#about">عن الأكاديمية</a></li>
        <li><a href="#contact">تواصل</a></li>
      </ul>
    </nav>
    <a href="register.html?p=hifz" class="nav-cta">سجل الآن</a>
    <button class="menu-toggle">☰</button>
  </div>
</header>

<section class="hero">
  <div class="hero-eyebrow">تعليم القرآن والقراءات</div>
  <h1>أكاديمية الشاطبي<br>لتعليم القرآن والقراءات</h1>
  <p class="lead">منصة جامعة بين حلقات الحفظ والإقراء، ومكتبة موثّقة للمتون والشروح، على نهج العلماء المتقدمين في علم القراءات.</p>
  <div class="ayah">
    ﴿ وَنُنَزِّلُ مِنَ الْقُرْآنِ مَا هُوَ شِفَاءٌ وَرَحْمَةٌ لِلْمُؤْمِنِينَ ﴾
    <span>سورة الإسراء — الآية 82</span>
  </div>
</section>

<!-- الحلقات -->
<div class="khazana" id="halaqat">
  <div class="section-head">
    <div class="section-num">01</div>
    <div class="section-titles">
      <h2>قسم الحلقات</h2>
      <p>برامج تعليمية مباشرة بإشراف معلمين متخصصين</p>
    </div>
  </div>
  <div class="catalog">
    <div class="card">
      <div class="tab"></div>
      <div class="num">حلقة ١</div>
      <div class="icon">📖</div>
      <h3>برنامج حفظ القرآن</h3>
      <div class="desc">تأسيس وحفظ منظّم بمتابعة يومية ومراجعة دورية.</div>
      <a href="register.html?p=hifz" class="reg-btn">سجل الآن ←</a>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">حلقة ٢</div>
      <div class="icon">🌿</div>
      <h3>برنامج إتقان حفظ القرآن</h3>
      <div class="desc">لمن أتمّ الحفظ ويريد الضبط والتثبيت والربط.</div>
      <a href="register.html?p=itqan" class="reg-btn">سجل الآن ←</a>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">حلقة ٣</div>
      <div class="icon">🕊️</div>
      <h3>برنامج تعلم القراءات إفرادًا</h3>
      <div class="desc">دراسة كل قراءة على حدة وفق أصولها وفرشها.</div>
      <a href="register.html?p=ifrad" class="reg-btn">سجل الآن ←</a>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">حلقة ٤</div>
      <div class="icon">🪶</div>
      <h3>برنامج تعلم القراءات جمعًا</h3>
      <div class="desc">جمع القراءات بطريقة الجمع المعروفة عند المشايخ.</div>
      <a href="register.html?p=jam3" class="reg-btn">سجل الآن ←</a>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">حلقة ٥</div>
      <div class="icon">📜</div>
      <h3>حفظ المتون</h3>
      <div class="desc">حفظ الشاطبية والجزرية والتحفة وغيرها من المتون.</div>
      <a href="register.html?p=mutoon" class="reg-btn">سجل الآن ←</a>
    </div>
  </div>
</div>

<!-- الكتب -->
<div class="khazana" id="kutub">
  <div class="section-head">
    <div class="section-num">02</div>
    <div class="section-titles">
      <h2>قسم الكتب</h2>
      <p>مكتبة موثّقة للمتون والشروح وكتب القراءات</p>
    </div>
  </div>
  <div class="catalog">
    <div class="card">
      <div class="tab"></div>
      <div class="num">باب ١</div>
      <div class="icon">📗</div>
      <h3>كتب التجويد</h3>
      <div class="desc">أحكام النون الساكنة والتنوين، المدود، الصفات.</div>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">باب ٢</div>
      <div class="icon">📘</div>
      <h3>كتب المتشابهات</h3>
      <div class="desc">رصد دقيق للمتشابه اللفظي بين آيات القرآن.</div>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">باب ٣</div>
      <div class="icon">📙</div>
      <h3>كتب القراءات إفرادًا</h3>
      <div class="desc">مصنفات في كل قراءة من القراءات العشر منفردة.</div>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">باب ٤</div>
      <div class="icon">📕</div>
      <h3>كتب القراءات جمعًا</h3>
      <div class="desc">مصنفات في طرق جمع القراءات العشر وتحقيقها.</div>
    </div>
    <div class="card">
      <div class="tab"></div>
      <div class="num">باب ٥</div>
      <div class="icon">📓</div>
      <h3>كتب المتون</h3>
      <div class="desc">الشاطبية والجزرية والتحفة بشروحها المعتمدة.</div>
    </div>
  </div>
</div>

<div class="emerald-band" id="contact">
  <h2>ابدأ رحلتك في حفظ كتاب الله وإتقان القراءات</h2>
  <p>سجّل الآن وانضم إلى حلقاتنا، أو تصفّح مكتبتنا التي تنمو أسبوعيًا بكتب ومتون جديدة.</p>
  <a href="register.html?p=hifz" class="btn-light">سجّل الآن</a>
</div>

<footer>
  <div>© أكاديمية الشاطبي لتعليم القرآن والقراءات — المقرئ عبدالعزيز السلمي</div>
  <div>alshatibi-academy.com</div>
</footer>

</body>
</html>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>التسجيل — أكاديمية الشاطبي</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Aref+Ruqaa:wght@400;700&family=Tajawal:wght@300;400;500;700;900&display=swap" rel="stylesheet">
<style>
:root{
  --parchment:#F4ECD8;--ink:#241B12;--emerald:#16433A;
  --emerald-deep:#0D2B25;--gold:#B88A3D;--gold-bright:#D4AF63;
  --thread:rgba(184,138,61,.35);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{background:var(--parchment);color:var(--ink);font-family:'Tajawal',sans-serif;min-height:100vh;}
header{
  background:linear-gradient(180deg,rgba(244,236,216,.97),rgba(244,236,216,.9));
  backdrop-filter:blur(6px);border-bottom:1px solid var(--thread);
  padding:16px 24px;display:flex;align-items:center;justify-content:space-between;
}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none;}
.brand-mark{
  width:40px;height:40px;border-radius:50%;
  background:radial-gradient(circle at 30% 30%,var(--gold-bright),var(--gold));
  display:flex;align-items:center;justify-content:center;
  font-family:'Aref Ruqaa',serif;color:var(--emerald-deep);font-weight:700;font-size:18px;
}
.brand-text{font-family:'Aref Ruqaa',serif;font-size:18px;color:var(--emerald-deep);}
.back-link{color:var(--gold);text-decoration:none;font-size:14px;font-weight:600;}
.sup-card{max-width:720px;margin:30px auto 0;padding:0 18px;}
.sup-inner{
  background:linear-gradient(135deg,var(--emerald-deep),var(--emerald));
  border-radius:8px;padding:22px 28px;display:flex;align-items:center;gap:16px;
}
.sup-icon{font-size:36px;flex-shrink:0;}
.sup-info h3{font-family:'Aref Ruqaa',serif;font-size:18px;color:var(--gold-bright);margin-bottom:4px;}
.sup-info p{color:rgba(244,236,216,.8);font-size:13px;}
.ijaza{display:inline-block;margin-top:6px;background:rgba(212,175,99,.2);border:1px solid rgba(212,175,99,.4);color:var(--gold-bright);font-size:11px;padding:3px 10px;border-radius:20px;}
.page-hero{text-align:center;padding:36px 18px 20px;}
.program-badge{
  display:inline-block;background:var(--emerald-deep);color:var(--gold-bright);
  font-family:'Aref Ruqaa',serif;font-size:15px;padding:6px 20px;border-radius:20px;margin-bottom:14px;
}
.page-hero h1{font-family:'Aref Ruqaa',serif;font-size:clamp(22px,5vw,34px);color:var(--emerald-deep);}
.form-wrap{max-width:720px;margin:0 auto 80px;padding:0 18px;}
.form-card{background:rgba(255,252,242,.7);border:1px solid var(--thread);border-radius:8px;padding:30px 28px;}
.sec-title{
  font-family:'Aref Ruqaa',serif;font-size:16px;color:var(--emerald-deep);
  border-bottom:1px solid var(--thread);padding-bottom:8px;margin:0 0 20px;
  display:flex;align-items:center;gap:8px;
}
.sec-title span{color:var(--gold);}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:20px;}
.full{grid-column:1/-1;}
.field label{display:block;font-size:12px;font-weight:700;color:var(--emerald-deep);margin-bottom:6px;}
.req{color:var(--gold);margin-right:2px;}
.field input,.field select,.field textarea{
  width:100%;padding:10px 13px;background:rgba(244,236,216,.5);
  border:1px solid var(--thread);border-radius:4px;
  font-family:'Tajawal',sans-serif;font-size:14px;color:var(--ink);
  outline:none;transition:border-color .2s;appearance:none;
}
.field input:focus,.field select:focus,.field textarea:focus{border-color:var(--gold);}
.field textarea{min-height:80px;resize:vertical;}
.gender-row{display:flex;gap:8px;}
.g-btn{
  flex:1;padding:10px;border:1px solid var(--thread);border-radius:4px;
  background:rgba(244,236,216,.5);cursor:pointer;font-family:'Tajawal',sans-serif;
  font-size:14px;text-align:center;transition:all .2s;
}
.g-btn.active{background:var(--emerald-deep);color:var(--parchment);border-color:var(--emerald-deep);}
.submit-btn{
  width:100%;padding:14px;margin-top:24px;
  background:linear-gradient(135deg,var(--emerald-deep),var(--emerald));
  color:var(--parchment);font-family:'Aref Ruqaa',serif;font-size:17px;
  border:none;border-radius:4px;cursor:pointer;border-bottom:3px solid var(--gold);transition:opacity .2s;
}
.submit-btn:hover{opacity:.9;}
.submit-btn:disabled{opacity:.6;cursor:not-allowed;}
.form-note{text-align:center;font-size:11px;color:var(--ink);opacity:.5;margin-top:12px;}
.success-msg{display:none;text-align:center;padding:50px 20px;}
.success-msg .icon{font-size:54px;margin-bottom:16px;}
.success-msg h2{font-family:'Aref Ruqaa',serif;color:var(--emerald-deep);font-size:24px;margin-bottom:10px;}
.success-msg p{color:var(--ink);opacity:.7;font-size:14px;line-height:1.8;}
.qiraat-extra{display:none;}
@media(max-width:560px){
  .grid{grid-template-columns:1fr;}
  .form-card{padding:20px 16px;}
  .sup-inner{flex-direction:column;text-align:center;}
}
</style>
</head>
<body>
<header>
  <a href="index.html" class="brand">
    <div class="brand-mark">ش</div>
    <div class="brand-text">أكاديمية الشاطبي</div>
  </a>
  <a href="index.html" class="back-link">← الرئيسية</a>
</header>

<div class="sup-card">
  <div class="sup-inner">
    <div class="sup-icon">🎓</div>
    <div class="sup-info">
      <h3>المقرئ عبدالعزيز السلمي</h3>
      <p>المشرف على أكاديمية الشاطبي لتعليم القرآن الكريم والقراءات</p>
      <span class="ijaza">مجاز بالقراءات العشر الصغرى والكبرى</span>
    </div>
  </div>
</div>

<div class="page-hero">
  <div class="program-badge" id="programBadge">استمارة التسجيل</div>
  <h1 id="pageTitle">التسجيل في الأكاديمية</h1>
</div>

<div class="form-wrap">
<div class="form-card" id="formCard">
  <form id="regForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="hidden" name="البرنامج" id="programField">

    <div class="sec-title"><span>①</span> البيانات الشخصية</div>
    <div class="grid">
      <div class="field">
        <label><span class="req">*</span>الاسم الكامل</label>
        <input type="text" name="الاسم_الكامل" placeholder="أدخل اسمك الكامل" required>
      </div>
      <div class="field">
        <label><span class="req">*</span>العمر</label>
        <input type="number" name="العمر" placeholder="مثال: 18" min="5" max="80" required>
      </div>
      <div class="field">
        <label><span class="req">*</span>الجنس</label>
        <div class="gender-row">
          <div class="g-btn active" onclick="selectGender(this,'ذكر')">ذكر</div>
          <div class="g-btn" onclick="selectGender(this,'أنثى')">أنثى</div>
        </div>
        <input type="hidden" name="الجنس" id="genderInput" value="ذكر">
      </div>
      <div class="field">
        <label><span class="req">*</span>المرحلة الدراسية</label>
        <select name="المرحلة_الدراسية" required>
          <option value="">اختر المرحلة</option>
          <option>ابتدائي</option><option>متوسط</option><option>ثانوي</option>
          <option>جامعي</option><option>متخرج</option><option>لا أدرس حالياً</option>
        </select>
      </div>
    </div>

    <div class="sec-title"><span>②</span> المستوى القرآني</div>
    <div class="grid">
      <div class="field">
        <label><span class="req">*</span>كم تحفظ من القرآن؟</label>
        <select name="مقدار_الحفظ" required>
          <option value="">اختر</option>
          <option>لا أحفظ شيئاً</option>
          <option>بعض السور القصيرة</option>
          <option>جزء عمّ (الجزء الثلاثون)</option>
          <option>من 1 إلى 5 أجزاء</option>
          <option>من 5 إلى 15 جزءاً</option>
          <option>من 15 إلى 25 جزءاً</option>
          <option>من 25 جزءاً إلى ختمة كاملة</option>
          <option>حافظ للقرآن كاملاً</option>
        </select>
      </div>
      <div class="field">
        <label><span class="req">*</span>هل سبق أن التحقت بحلقة تحفيظ؟</label>
        <select name="سبق_الالتحاق" required>
          <option value="">اختر</option>
          <option>نعم، لا أزال فيها</option>
          <option>نعم، أتممتها</option>
          <option>نعم، لكنني تركتها</option>
          <option>لا، هذه أول مرة</option>
        </select>
      </div>

      <!-- أسئلة القراءات الإضافية -->
      <div class="field qiraat-extra" id="qRiwayaMutaalama">
        <label><span class="req">*</span>ما الرواية التي تعلمتها؟</label>
        <select name="الرواية_المتعلمة">
          <option value="">اختر الرواية</option>
          <option>حفص عن عاصم</option><option>ورش عن نافع</option>
          <option>قالون عن نافع</option><option>البزي عن ابن كثير</option>
          <option>قنبل عن ابن كثير</option><option>الدوري عن أبي عمرو</option>
          <option>السوسي عن أبي عمرو</option><option>هشام عن ابن عامر</option>
          <option>ابن ذكوان عن ابن عامر</option><option>شعبة عن عاصم</option>
          <option>خلف عن حمزة</option><option>خلاد عن حمزة</option>
          <option>الدوري عن الكسائي</option><option>الليث عن الكسائي</option>
          <option>رويس عن يعقوب</option><option>روح عن يعقوب</option>
          <option>ابن وردان عن أبي جعفر</option><option>ابن جماز عن أبي جعفر</option>
          <option>إسحاق عن خلف</option><option>إدريس عن خلف</option>
          <option>لم أتعلم رواية بعد</option>
        </select>
      </div>

      <div class="field qiraat-extra" id="qRiwayaMarghouba">
        <label><span class="req">*</span>ما الرواية التي ترغب في تعلمها؟</label>
        <select name="الرواية_المرغوبة">
          <option value="">اختر الرواية</option>
          <option>حفص عن عاصم</option><option>ورش عن نافع</option>
          <option>قالون عن نافع</option><option>البزي عن ابن كثير</option>
          <option>قنبل عن ابن كثير</option><option>الدوري عن أبي عمرو</option>
          <option>السوسي عن أبي عمرو</option><option>هشام عن ابن عامر</option>
          <option>ابن ذكوان عن ابن عامر</option><option>شعبة عن عاصم</option>
          <option>خلف عن حمزة</option><option>خلاد عن حمزة</option>
          <option>الدوري عن الكسائي</option><option>الليث عن الكسائي</option>
          <option>رويس عن يعقوب</option><option>روح عن يعقوب</option>
          <option>ابن وردان عن أبي جعفر</option><option>ابن جماز عن أبي جعفر</option>
          <option>إسحاق عن خلف</option><option>إدريس عن خلف</option>
        </select>
      </div>

      <div class="field qiraat-extra" id="qSabaqJam">
        <label><span class="req">*</span>هل سبق أن جمعت القراءات؟</label>
        <select name="سبق_الجمع">
          <option value="">اختر</option>
          <option>نعم، جمعت رواية أو أكثر</option>
          <option>لا، هذه أول مرة في الجمع</option>
          <option>أنا في مرحلة الإفراد الآن</option>
        </select>
      </div>
    </div>

    <div class="sec-title"><span>③</span> بيانات الالتحاق</div>
    <div class="grid">
      <div class="field">
        <label><span class="req">*</span>عدد الحصص في الأسبوع التي ترغبها</label>
        <select name="عدد_الحصص_أسبوعياً" required>
          <option value="">اختر</option>
          <option>حصة واحدة</option><option>حصتان</option>
          <option>ثلاث حصص</option><option>أربع حصص أو أكثر</option>
        </select>
      </div>
      <div class="field full">
        <label>ملاحظات إضافية</label>
        <textarea name="ملاحظات" placeholder="أي معلومات إضافية تريد إضافتها..."></textarea>
      </div>
    </div>

    <button type="submit" class="submit-btn" id="submitBtn">تقديم طلب التسجيل ←</button>
    <p class="form-note">سيتم التواصل معك خلال 48 ساعة من تقديم الطلب</p>
  </form>

  <div class="success-msg" id="successMsg">
    <div class="icon">✅</div>
    <h2>تم استلام طلبك بنجاح</h2>
    <p>جزاك الله خيراً، سيتم التواصل معك خلال 48 ساعة.<br>نسأل الله أن يجعلك من حفاظ كتابه وعباده الصالحين.</p>
  </div>
</div>
</div>

<script>
const programs = {
  hifz:   { badge:'برنامج حفظ القرآن',         title:'التسجيل في برنامج حفظ القرآن',         qiraat:false, jam:false },
  itqan:  { badge:'برنامج إتقان حفظ القرآن',    title:'التسجيل في برنامج الإتقان',            qiraat:false, jam:false },
  ifrad:  { badge:'برنامج القراءات إفراداً',    title:'التسجيل في برنامج القراءات إفراداً',   qiraat:true,  jam:false },
  jam3:   { badge:'برنامج القراءات جمعاً',      title:'التسجيل في برنامج القراءات جمعاً',    qiraat:true,  jam:true  },
  mutoon: { badge:'برنامج حفظ المتون',          title:'التسجيل في برنامج حفظ المتون',         qiraat:false, jam:false }
};

function init(){
  const key = new URLSearchParams(window.location.search).get('p') || 'hifz';
  const prog = programs[key] || programs.hifz;
  document.getElementById('programBadge').textContent = prog.badge;
  document.getElementById('pageTitle').textContent = prog.title;
  document.getElementById('programField').value = prog.badge;
  document.title = prog.badge + ' — أكاديمية الشاطبي';
  if(prog.qiraat){
    document.getElementById('qRiwayaMutaalama').style.display = 'block';
    document.getElementById('qRiwayaMarghouba').style.display = 'block';
    document.querySelector('[name="الرواية_المتعلمة"]').required = true;
    document.querySelector('[name="الرواية_المرغوبة"]').required = true;
  }
  if(prog.jam){
    document.getElementById('qSabaqJam').style.display = 'block';
    document.querySelector('[name="سبق_الجمع"]').required = true;
  }
}

function selectGender(btn, val){
  document.querySelectorAll('.g-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  document.getElementById('genderInput').value = val;
}

document.getElementById('regForm').addEventListener('submit', async function(e){
  e.preventDefault();
  const btn = document.getElementById('submitBtn');
  btn.textContent = 'جارٍ الإرسال...';
  btn.disabled = true;
  try{
    const res = await fetch(this.action,{
      method:'POST', body:new FormData(this),
      headers:{'Accept':'application/json'}
    });
    if(res.ok){
      this.style.display='none';
      document.getElementById('successMsg').style.display='block';
    } else {
      btn.textContent = 'حدث خطأ، حاول مجدداً';
      btn.disabled = false;
    }
  } catch(err){
    btn.textContent = 'حدث خطأ، حاول مجدداً';
    btn.disabled = false;
  }
});

init();
</script>
</body>
</html>
