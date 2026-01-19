<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>عرض استثماري - مجموعة بن عوض النقيب</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00563F; /* أخضر غامق ملكي */
            --primary-light: #007A5E;
            --gold: #C5A059; /* ذهبي فخم */
            --bg-presentation: #e0e5ec; /* لون خلفية العرض */
            --white: #ffffff;
            --text-dark: #1A202C;
        }

        * { box-sizing: border-box; transition: all 0.3s ease; }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: var(--bg-presentation);
            color: var(--text-dark);
            margin: 0;
            padding: 20px 0;
            line-height: 1.6;
        }

        /* --- حاوية العرض (مساحة الشرائح) --- */
        .presentation-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* --- تصميم الشريحة (Slide Design) --- */
        .slide {
            background: var(--white);
            width: 100%;
            min-height: 600px; /* ارتفاع أدنى للشريحة */
            margin-bottom: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
            border: 1px solid #fff;
            display: flex;
            flex-direction: column;
        }

        /* شريط علوي للشريحة (Header Strip) */
        .slide-header {
            background: linear-gradient(90deg, var(--primary), #003322);
            color: white;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 5px solid var(--gold);
        }

        .slide-title { font-size: 1.4rem; font-weight: 800; margin: 0; }
        .slide-logo { font-size: 1rem; opacity: 0.8; font-weight: bold; }

        /* محتوى الشريحة */
        .slide-content {
            padding: 40px;
            flex-grow: 1;
        }

        /* رقم الشريحة */
        .slide-number {
            position: absolute;
            bottom: 15px;
            left: 20px;
            font-weight: bold;
            color: #ccc;
            font-size: 1.2rem;
        }

        /* --- الشريحة 1: الغلاف --- */
        .cover-slide {
            text-align: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--primary), #002b1d);
            color: white;
            border: none;
        }
        .cover-slide h1 { font-size: clamp(2rem, 5vw, 3.5rem); margin-bottom: 20px; line-height: 1.2; }
        .cover-slide p { font-size: 1.2rem; opacity: 0.9; margin-top: 10px; }
        .dedication-box {
            border: 2px solid var(--gold);
            padding: 10px 30px;
            border-radius: 50px;
            display: inline-block;
            margin-bottom: 30px;
            background: rgba(255,255,255,0.05);
        }

        /* --- الجدول (Slide 2) --- */
        .table-wrapper { overflow-x: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; min-width: 900px; }
        th { background: var(--primary); color: white; padding: 12px; font-size: 0.95rem; }
        td { padding: 12px; border-bottom: 1px solid #eee; font-size: 0.9rem; vertical-align: top; }
        ul.tbl-list { margin: 0; padding-right: 15px; list-style: disc; }
        ul.tbl-list li { margin-bottom: 5px; }
        
        .btn-visit {
            background: var(--primary); color: white; text-decoration: none;
            padding: 5px 15px; border-radius: 20px; font-size: 0.8rem; display: inline-block;
        }

        /* --- التوصية (Slide 3) --- */
        .rec-box {
            border: 2px solid var(--primary);
            border-radius: 15px;
            padding: 30px;
            background: #f9fffb;
            text-align: center;
        }
        .features-row {
            display: flex;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        .feature-item {
            flex: 1;
            min-width: 250px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border-top: 4px solid var(--gold);
        }

        /* --- التمويل (Slide 4) - التصميم الجديد --- */
        .finance-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        .finance-card {
            background: #fff;
            border: 1px solid #eee;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.03);
            position: relative;
            transition: transform 0.3s;
        }
        .finance-card:hover { transform: translateY(-5px); }
        .fin-icon { font-size: 2.5rem; color: var(--primary); margin-bottom: 15px; }
        .fin-title { color: var(--primary); font-size: 1.3rem; font-weight: bold; margin-bottom: 15px; border-bottom: 2px solid var(--gold); padding-bottom: 10px; display: inline-block;}
        
        .req-list {
            margin: 10px 0;
            padding-right: 20px;
            font-size: 0.9rem;
            color: #555;
            background: #f8fafc;
            padding: 15px 25px 15px 10px;
            border-radius: 10px;
        }
        .req-list li { margin-bottom: 8px; }

        /* --- الروابط (Slide 5) --- */
        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }
        .link-btn {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 30px;
            background: #f8fafc;
            border-radius: 15px;
            text-decoration: none;
            color: var(--text-dark);
            border: 1px solid #e2e8f0;
            transition: 0.3s;
        }
        .link-btn:hover { background: var(--white); border-color: var(--gold); transform: scale(1.05); }
        .link-icon { font-size: 2rem; color: var(--primary); margin-bottom: 15px; }

        /* --- الفوتر --- */
        footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
        }

        /* تجاوب الجوال */
        @media (max-width: 768px) {
            .slide { min-height: auto; margin-bottom: 20px; border-radius: 10px;}
            .slide-content { padding: 20px; }
            .cover-slide h1 { font-size: 1.8rem; }
            .slide-title { font-size: 1.1rem; }
        }
    </style>
</head>
<body>

<div class="presentation-container">

    <section class="slide cover-slide">
        <div class="slide-content" style="display: flex; flex-direction: column; justify-content: center; align-items: center;">
            <div class="dedication-box">
                <h2 style="margin:0; font-size:1.2rem; color:var(--gold);">إهداء إلى مجموعة بن عوض النقيب</h2>
            </div>
            <h1>فرص الاستثمار الصناعي في المملكة</h1>
            <p>مقارنة بين المدن الاقتصادية لتأسيس مصانع المواد الغذائية<br>مدعومة بالحوافز الحكومية وحلول التمويل</p>
            <div style="margin-top: 40px; font-size: 0.9rem; opacity: 0.7;">
                إعداد / نصار منصور الغريب
            </div>
        </div>
    </section>

    <section class="slide">
        <div class="slide-header">
            <h2 class="slide-title">1. مقارنة المناطق الاقتصادية (تحليل فني)</h2>
            <span class="slide-logo">دراسة الجدوى</span>
        </div>
        <div class="slide-content">
            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th width="20%">المنطقة</th>
                            <th width="25%">القطاعات المستهدفة</th>
                            <th width="30%">الحوافز والمزايا</th>
                            <th width="15%">البنية التحتية</th>
                            <th>الرابط</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f0fdf4; border-left: 4px solid var(--gold);">
                            <td style="font-weight:bold; color:var(--primary);">منطقة جازان (JCPDI) <i class="fas fa-star" style="color:var(--gold)"></i></td>
                            <td><ul class="tbl-list"><li>معالجة الأغذية</li><li>تحويل المعادن</li><li>الخدمات اللوجستية</li></ul></td>
                            <td><ul class="tbl-list"><li>5% ضريبة دخل</li><li>0% ضريبة قيمة مضافة</li><li>تأجيل الرسوم الجمركية</li></ul></td>
                            <td>ميناء ضخم، طاقة رخيصة، مواد خام</td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" class="btn-visit">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>مدينة الملك عبدالله (KAEC)</td>
                            <td><ul class="tbl-list"><li>السلع الاستهلاكية</li><li>تجميع السيارات</li><li>الأدوية</li></ul></td>
                            <td><ul class="tbl-list"><li>5% ضريبة دخل</li><li>إعفاء جمركي للمعدات</li></ul></td>
                            <td>ميناء عالمي، غاز طبيعي</td>
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" class="btn-visit">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>رأس الخير (Ras Al-Khair)</td>
                            <td><ul class="tbl-list"><li>الصناعات البحرية</li><li>منصات الحفر</li></ul></td>
                            <td><ul class="tbl-list"><li>5% ضريبة دخل</li><li>0% استقطاع</li></ul></td>
                            <td>حوض بناء سفن، تعدين</td>
                            <td><a href="https://www.rcjy.gov.sa" target="_blank" class="btn-visit">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>الرياض اللوجستية (RISLZ)</td>
                            <td><ul class="tbl-list"><li>المنتجات الاستهلاكية</li><li>التجميع الخفيف</li><li>الأدوية</li></ul></td>
                            <td><ul class="tbl-list"><li>إعفاء ضريبي 50 عاماً</li><li>0% ضريبة دخل</li></ul></td>
                            <td>موقع جوي استراتيجي</td>
                            <td><a href="https://www.silz.gaca.gov.sa" target="_blank" class="btn-visit">زيارة</a></td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div style="text-align:center; font-size:0.8rem; color:#888; margin-top:5px;">(اسحب الجدول يميناً ويساراً على الجوال)</div>
        </div>
        <div class="slide-number">01</div>
    </section>

    <section class="slide">
        <div class="slide-header">
            <h2 class="slide-title">2. التوصية الاستراتيجية</h2>
            <span class="slide-logo">مجموعة بن عوض النقيب</span>
        </div>
        <div class="slide-content">
            <div class="rec-box">
                <i class="fas fa-crown" style="font-size:3rem; color:var(--gold); margin-bottom:15px;"></i>
                <h3 style="margin:0 0 10px 0; color:var(--primary);">نرشح: المنطقة الاقتصادية الخاصة بجازان (JCPDI)</h3>
                <p>المنطقة الوحيدة التي تدمج بين الاستهداف القطاعي للأغذية وأقل تكلفة تشغيلية.</p>
                
                <div class="features-row">
                    <div class="feature-item">
                        <i class="fas fa-utensils" style="color:var(--primary); font-size:1.5rem;"></i>
                        <h4>التخصص في الأغذية</h4>
                        <p style="font-size:0.9rem;">بنية تحتية (مستودعات وتبريد) مجهزة خصيصاً لقطاع "معالجة الأغذية" كقطاع رئيسي.</p>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-money-bill-wave" style="color:var(--primary); font-size:1.5rem;"></i>
                        <h4>السيولة الفورية</h4>
                        <p style="font-size:0.9rem;">الإعفاء من ضريبة القيمة المضافة وتأجيل الجمارك يوفر "كاش" فوري عند التأسيس.</p>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-globe-africa" style="color:var(--primary); font-size:1.5rem;"></i>
                        <h4>بوابة التصدير</h4>
                        <p style="font-size:0.9rem;">الأقرب للأسواق الأفريقية عبر البحر الأحمر، مما يقلل تكاليف الشحن وزمن الوصول.</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="slide-number">02</div>
    </section>

    <section class="slide">
        <div class="slide-header">
            <h2 class="slide-title">3. حلول التمويل والدعم المالي</h2>
            <span class="slide-logo">خيارات التمويل</span>
        </div>
        <div class="slide-content">
            <div class="finance-grid">
                
                <div class="finance-card">
                    <i class="fas fa-industry fin-icon"></i><br>
                    <span class="fin-title">صندوق التنمية الصناعي (SIDF)</span>
                    <ul class="req-list">
                        <li><strong>نسبة التمويل:</strong> تصل إلى 75% من رأس المال.</li>
                        <li><strong>الرسوم:</strong> لا تتجاوز 3% (رسوم إدارية).</li>
                        <li><strong>فترة السماح:</strong> لمدة سنتين.</li>
                    </ul>
                    <div style="background:#fffbeb; padding:10px; border-radius:8px; font-size:0.85rem; border:1px dashed var(--gold);">
                        <strong>متطلبات دراسة الجدوى:</strong><br>
                        • القسم الفني والتسويقي والمالي.<br>
                        • القسم المالي يشمل: التكاليف الرأسمالية، تكلفة ما قبل التشغيل (الإنشاءات)، والتكلفة التشغيلية للربع الأول.
                    </div>
                </div>

                <div class="finance-card">
                    <i class="fas fa-ship fin-icon"></i><br>
                    <span class="fin-title">بنك التصدير والاستيراد السعودي</span>
                    <p style="font-size:0.9rem; margin-bottom:10px;">يقدم برامج تمويل للمصدرين وللمستوردين الخارجيين أو الدوليين.</p>
                    <ul class="req-list" style="background:#eef2ff;">
                        <li><strong>نوع التمويل:</strong> عليه فوائد.</li>
                        <li><strong>تحديد الفائدة:</strong> تعتمد على التقديم، الدراسة الائتمانية، نوع المنتج، والبلد المصدر إليه.</li>
                    </ul>
                </div>

                <div class="finance-card">
                    <i class="fas fa-hand-holding-usd fin-icon"></i><br>
                    <span class="fin-title">حوافز المنطقة الاقتصادية</span>
                    <p style="font-size:0.9rem;">دعم مالي غير مباشر يوفر السيولة:</p>
                    <ul class="req-list" style="background:#f0fdf4;">
                        <li>تأجيل دفع الرسوم الجمركية.</li>
                        <li>0% ضريبة قيمة مضافة (توفير 15% كاش).</li>
                        <li>عقود إيجار وطاقة بأسعار مدعومة.</li>
                    </ul>
                </div>

            </div>
        </div>
        <div class="slide-number">03</div>
    </section>

    <section class="slide">
        <div class="slide-header">
            <h2 class="slide-title">4. الوصول المباشر للجهات الرسمية</h2>
            <span class="slide-logo">روابط هامة</span>
        </div>
        <div class="slide-content">
            <div class="links-grid">
                
                <a href="https://site.ecza.gov.sa/ar" target="_blank" class="link-btn">
                    <i class="fas fa-university link-icon"></i>
                    <strong>هيئة المدن (ECZA)</strong>
                </a>

                <a href="https://www.sidf.gov.sa/ar" target="_blank" class="link-btn">
                    <i class="fas fa-cogs link-icon"></i>
                    <strong>الصندوق الصناعي (SIDF)</strong>
                </a>

                <a href="https://saudiexim.gov.sa/ar" target="_blank" class="link-btn">
                    <i class="fas fa-ship link-icon"></i>
                    <strong>بنك التصدير (Saudi EXIM)</strong>
                </a>

                <a href="https://misa.gov.sa/ar" target="_blank" class="link-btn">
                    <i class="fas fa-briefcase link-icon"></i>
                    <strong>وزارة الاستثمار (MISA)</strong>
                </a>

                <a href="https://www.investjcpdi.com" target="_blank" class="link-btn" style="border-color:var(--primary); background:#f0fdf4;">
                    <i class="fas fa-map-marker-alt link-icon"></i>
                    <strong>منطقة جازان (الموقع الرسمي)</strong>
                </a>

            </div>
        </div>
        <div class="slide-number">04</div>
    </section>

</div>

<footer>
    <p>&copy; 2024 جميع الحقوق محفوظة لمجموعة بن عوض النقيب | إعداد: نصار منصور الغريب</p>
</footer>

</body>
</html>
