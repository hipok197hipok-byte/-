(<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>По рукам | Услуги в Казахстане</title>
    <style>
        :root {
            --primary: #ffcc00;
            --dark: #222;
            --light: #f4f4f4;
            --success: #25d366;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background: var(--light); color: var(--dark); line-height: 1.6; }
        header { background: var(--dark); color: white; padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 1000; }
        .logo { font-size: 24px; font-weight: bold; color: var(--primary); }
        .lang-btn { background: var(--primary); border: none; padding: 8px 15px; font-weight: bold; cursor: pointer; border-radius: 5px; }
        .hero { text-align: center; padding: 60px 20px; background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1601584115197-04ecc0da31d7?q=80&w=1000') center/cover; color: white; }
        .hero h1 { font-size: 36px; margin-bottom: 10px; }
        .services { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; padding: 40px 20px; max-width: 1200px; margin: 0 auto; }
        .card { background: white; padding: 25px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); text-align: center; }
        .card h3 { margin-bottom: 15px; color: var(--dark); border-bottom: 2px solid var(--primary); padding-bottom: 10px; }
        .cta-container { text-align: center; padding: 40px 20px; background: white; }
        .whatsapp-btn { display: inline-flex; align-items: center; background: var(--success); color: white; text-decoration: none; padding: 15px 30px; font-size: 20px; font-weight: bold; border-radius: 50px; box-shadow: 0 4px 10px rgba(37,211,102,0.4); transition: 0.3s; }
        .whatsapp-btn:hover { transform: translateY(-3px); box-shadow: 0 6px 15px rgba(37,211,102,0.6); }
        footer { background: var(--dark); color: #888; text-align: center; padding: 20px; font-size: 14px; }
    </style>
</head>
<body>

<header>
    <div class="logo">По рукам</div>
    <button class="lang-btn" onclick="toggleLang()" id="langBtn">ҚАЗ</button>
</header>

<section class="hero">
    <h1 id="heroTitle">Грузоперевозки & Сборка мебели</h1>
    <p id="heroSubtitle">Быстро, надежно, аккуратно. Работаем по всему городу.</p>
</section>

<section class="services">
    <div class="card">
        <h3 id="s1Title">Грузоперевозки</h3>
        <p id="s1Desc">Переезды квартир, офисов. Профессиональные грузчики и чистый транспорт.</p>
    </div>
    <div class="card">
        <h3 id="s2Title">Сборка мебели</h3>
        <p id="s2Desc">Качественная сборка и разборка шкафов, кухонь, кроватей любой сложности.</p>
    </div>
    <div class="card">
        <h3 id="s3Title">Демонтаж</h3>
        <p id="s3Desc">Аккуратный демонтаж стен, полов, старой мебели. Вывоз строительного мусора.</p>
    </div>
</section>

<section class="cta-container">
    <a href="https://wa.me/77476054583" target="_blank" class="whatsapp-btn">
        <span id="ctaText">Написать в WhatsApp</span>
    </a>
</section>

<footer>
    <p>© 2026 «По рукам». Все права защищены.</p>
</footer>

<script>
    let currentLang = 'ru';
    const content = {
        ru: {
            btn: 'ҚАЗ',
            title: 'Грузоперевозки & Сборка мебели',
            subtitle: 'Быстро, надежно, аккуратно. Работаем по всему городу.',
            s1T: 'Грузоперевозки', s1D: 'Переезды квартир, офисов. Профессиональные грузчики и чистый транспорт.',
            s2T: 'Сборка мебели', s2D: 'Качественная сборка и разборка шкафов, кухонь, кроватей любой сложности.',
            s3T: 'Демонтаж', s3D: 'Аккуратный демонтаж стен, полов, старой мебели. Вывоз строительного мусора.',
            cta: 'Написать в WhatsApp'
        },
        kk: {
            btn: 'РУС',
            title: 'Жүк тасымалы және Жиһаз жинау',
            subtitle: 'Жылдам, сенімді, ұқыпты. Қала бойынша жұмыс істейміз.',
            s1T: 'Жүк тасымалы', s1D: 'Пәтерлерді, кеңселерді көшіру. Кәсіби тиеушілер мен таза көлік.',
            s2T: 'Жиһаз жинау', s2D: 'Кез келген күрделіліктегі шкафтарды, ас үй жиһаздарын, төсектерді сапалы жинау және бөлшектеу.',
            s3T: 'Демонтаж', s3D: 'Қабырғаларды, едендерді, ескі жиһаздарды ұқыпты бөлшектеу. Құрылыс қоқыстарын шығару.',
            cta: 'WhatsApp-қа жазу'
        }
    };

    function toggleLang() {
        currentLang = currentLang === 'ru' ? 'kk' : 'ru';
        const data = content[currentLang];
        
        document.getElementById('langBtn').innerText = data.btn;
        document.getElementById('heroTitle').innerText = data.title;
        document.getElementById('heroSubtitle').innerText = data.subtitle;
        document.getElementById('s1Title').innerText = data.s1T;
        document.getElementById('s1Desc').innerText = data.s1D;
        document.getElementById('s2Title').innerText = data.s2T;
        document.getElementById('s2Desc').innerText = data.s2D;
        document.getElementById('s3Title').innerText = data.s3T;
        document.getElementById('s3Desc').innerText = data.s3D;
        document.getElementById('ctaText').innerText = data.cta;
    }
</script>

</body>
</html>
)
