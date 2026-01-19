<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>عرض استثماري - فرص الاستثمار الصناعي</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00563F; /* أخضر غامق ملكي */
            --primary-light: #007A5E;
            --gold: #C5A059; /* ذهبي فخم */
            --gold-light: #E5C585;
            --bg-body: #F7F9FC;
            --white: #ffffff;
            --text-dark: #1A202C;
            --text-gray: #4A5568;
        }

        * { box-sizing: border-box; transition: all 0.3s ease; }

        html, body {
            width: 100%;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: var(--bg-body);
            color: var(--text-dark);
            line-height: 1.8;
            -webkit-font-smoothing: antialiased;
        }

        /* --- الهيدر الفخم --- */
        header {
            background: linear-gradient(135deg, var(--primary), #003322);
            color: var(--white);
            padding: 4rem 1.5rem;
            text-align: center;
            position: relative;
            width: 100%;
            border-bottom: 6px solid var(--gold);
        }

        header::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background-image: url('https://www.transparenttextures.com/patterns/cubes.png');
            opacity: 0.08;
            background-size: auto;
            background-repeat: repeat;
        }

        .header-content { position: relative; z-index: 2; max-width: 100%; }
        
        header h1 { 
            margin: 0; 
            font-size: clamp(1.8rem, 5vw, 2.8rem);
            font-weight: 800; 
            margin-bottom: 15px;
            line-height: 1.3;
        }

        /* --- الحاويات والبطاقات --- */
        .container { 
            max-width: 1200px; 
            margin: -40px auto 0; 
            padding: 0 15px 40px;
            position: relative; 
            z-index: 10; 
            width: 100%;
        }

        .card {
            background: var(--white);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            border-top: 4px solid transparent;
            width: 100%;
            overflow: hidden;
        }

        .section-title {
            text-align: center;
            font-size: clamp(1.5rem, 4vw, 2rem);
            color: var(--primary);
            margin-bottom: 25px;
            position: relative;
            font-weight: 800;
        }

        /* --- الجدول متجاوب --- */
        .table-container { 
            width: 100%;
            overflow-x: auto;
            border-radius: 10px; 
            box-shadow: 0 0 10px rgba(0,0,0,0.05); 
            -webkit-overflow-scrolling: touch;
            padding-bottom: 5px;
            background: white;
        }
        
        .scroll-hint {
            display: none;
            text-align: center;
            font-size: 0.8rem;
            color: #888;
            margin-top: 8px;
            animation: fadeIn 2s infinite;
        }
        @keyframes fadeIn { 0%,100% {opacity:0.6} 50% {opacity:1} }

        table { width: 100%; border-collapse: collapse; min-width: 800px; }
        th { background: var(--primary); color: white; padding: 15px; text-align: right; font-size: 1rem; white-space: nowrap; }
        td { padding: 12px; border-bottom: 1px solid #eee; color: var(--text-dark); vertical-align: middle; }
        tr:nth-child(even) { background-color: #f8fafc; }
        
        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-bottom: 3px;
            white-space: nowrap;
        }
        .badge-sector { background: #e0f2fe; color: #0369a1; }
        .badge-infra { background: #f0fdf4; color: #15803d; }

        /* --- التوصية الاستثمارية --- */
        .recommendation { border-top-color: var(--gold); background: linear-gradient(to bottom, #ffffff, #fffdf7); }
        .rec-header { 
            display: flex; 
            align-items: center; 
            gap: 15px; 
            margin-bottom: 20px; 
            border-bottom: 2px solid #eee; 
            padding-bottom: 15px; 
            flex-wrap: wrap;
            justify-content: center;
        }
        .rec-icon { font-size: 2rem; color: var(--gold); }
        .rec-title { color: var(--primary); font-size: clamp(1.2rem, 4vw, 1.8rem); margin: 0; font-weight: 800; text-align: center;}

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        .feature-box {
            background: white;
            padding: 20px;
            border-radius: 12px;
            border: 1px solid #eee;
            border-right: 4px solid var(--primary);
        }

        /* --- قسم التمويل --- */
        .funding-section { border-top-color: var(--primary); }
        .loans-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .loan-card {
            background: #fff;
            border: 1px solid #e2e8f0;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            position: relative;
        }
        .loan-card::before {
            content: '';
            position: absolute;
            top: 0; right: 0; width: 100%; height: 5px;
            background: var(--gold);
        }
        .fee-badge {
            background: #fee2e2;
            color: #991b1b;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            display: inline-block;
            margin-top: 10px;
        }

        /* --- الروابط الحكومية --- */
        .gov-links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        .gov-link-card {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: #f8fafc;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            padding: 15px;
            text-decoration: none;
            color: var(--text-dark);
            text-align: center;
            height: 100%;
        }
        .gov-icon { font-size: 1.5rem; color: var(--primary); margin-bottom: 8px; }
        .gov-name { font-weight: bold; font-size: 0.85rem; }

        /* --- الأزرار --- */
        .btn-link {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            color: var(--primary);
            text-decoration: none;
            font-weight: bold;
            padding: 6px 12px;
            border: 1px solid var(--primary);
            border-radius: 50px;
            font-size: 0.85rem;
            white-space: nowrap;
        }
        .btn-link:hover { background: var(--primary); color: white; }

        .btn-main {
            display: inline-flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            background-color: var(--primary);
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1rem;
            box-shadow: 0 4px 15px rgba(0,86,63,0.3);
            margin-top: 20px;
            width: fit-content;
        }
        .btn-main:hover { background-color: var(--gold); transform: translateY(-3px); }

        /* --- الفوتر --- */
        footer {
            background-color: #1a202c;
            color: #a0aec0;
            text-align: center;
            padding: 30px 15px;
            border-top: 5px solid var(--gold);
            width: 100%;
            position: relative;
        }
        .creator-badge {
            background: rgba(255,255,255,0.1);
            padding: 5px 15px;
            border-radius: 30px;
            color: var(--gold);
            font-weight: bold;
            font-size: 1rem;
            display: inline-block;
            margin-bottom: 10px;
            border: 1px solid rgba(197, 160, 89, 0.3);
        }

        /* --- تحسينات خاصة للجوال --- */
        @media (max-width: 768px) {
            .container { padding: 0 15px 40px; margin-top: -30px; }
            .card { padding: 1.5rem 1rem; } 
            .rec-header { flex-direction: column; text-align: center; gap: 10px; }
            .btn-main { width: 100%; } 
            .scroll-hint { display: block; }
            
            header, footer {
                width: 100vw;
                box-sizing: border-box;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-content">
            <h1>فرص الاستثمار الصناعي في المملكة</h1>
            <p style="font-size: clamp(1rem, 3vw, 1.3rem); margin-top: 15px; font-weight: 500; color: var(--gold-light); line-height: 1.6;">
                مقارنة بين المدن الاقتصادية في المملكة العربية السعودية لتأسيس مصانع المواد الغذائية
            </p>
        </div>
    </header>

    <div class="container">

        <section class="card">
            <h2 class="section-title">تحليل المناطق الاقتصادية</h2>
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>المنطقة</th>
                            <th width="30%">القطاعات المستهدفة</th>
                            <th>المزايا المالية والضريبية</th>
                            <th>البنية التحتية والمرافق</th>
                            <th>الموقع الرسمي</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr style="background-color: #f0fdf4;">
                            <td style="font-weight: bold; color: var(--primary);">
                                <i class="fas fa-star" style="color: var(--gold);"></i> منطقة جازان (JCPDI)
                            </td>
                            <td>
                                <span class="badge badge-sector">معالجة الأغذية</span><br>
                                <span class="badge badge-sector">تحويل المعادن</span>
                            </td>
                            <td>
                                • 5% ضريبة دخل<br>
                                • 0% ضريبة قيمة مضافة<br>
                                • تأجيل الرسوم الجمركية
                            </td>
                            <td>
                                <span class="badge badge-infra">طاقة رخيصة</span><br>
                                <span class="badge badge-infra">خيارات مياه متعددة</span>
                            </td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>مدينة الملك عبدالله (KAEC)</td>
                            <td>
                                <span class="badge badge-sector">السلع الاستهلاكية</span><br>
                                <span class="badge badge-sector">صناعة السيارات</span>
                            </td>
                            <td>
                                • 5% ضريبة دخل<br>
                                • إعفاء جمركي للمعدات
                            </td>
                            <td>
                                <span class="badge badge-infra">ميناء الملك عبدالله</span><br>
                                <span class="badge badge-infra">شبكة غاز طبيعي</span>
                            </td>
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>رأس الخير (Ras Al-Khair)</td>
                            <td>
                                <span class="badge badge-sector">الصناعات البحرية</span><br>
                                <span class="badge badge-sector">منصات الحفر</span>
                            </td>
                            <td>
                                • 5% ضريبة دخل<br>
                                • 0% ضريبة استقطاع
                            </td>
                            <td>
                                <span class="badge badge-infra">أكبر حوض بناء سفن</span><br>
                                <span class="badge badge-infra">صناعات تعدينية ثقيلة</span>
                            </td>
                            <td><a href="https://www.rcjy.gov.sa" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>
                        <tr>
                            <td>الرياض اللوجستية (RISLZ)</td>
                            <td>
                                <span class="badge badge-sector">الخدمات اللوجستية</span><br>
                                <span class="badge badge-sector">التجميع الخفيف</span>
                            </td>
                            <td>
                                • إعفاء ضريبي لمدة 50 عاماً<br>
                                • 0% ضريبة دخل
                            </td>
                            <td>
                                <span class="badge badge-infra">موقع جوي استراتيجي</span><br>
                                <span class="badge badge-infra">بنية رقمية متقدمة</span>
                            </td>
                            <td><a href="https://www.silz.gaca.gov.sa" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="scroll-hint"><i class="fas fa-arrows-left-right"></i> اسحب الجدول يميناً ويساراً لعرض باقي التفاصيل</div>
        </section>

        <section class="card recommendation">
            <div class="rec-header">
                <i class="fas fa-crown rec-icon"></i>
                <div>
                    <h2 class="rec-title">ترشيح المنطقة الأنسب: جازان (JCPDI)</h2>
                    <p style="margin: 5px 0 0 0; color: #666; font-size: 0.95rem; text-align: center;">الخيار الاستراتيجي لمجموعة بن عوض النقيب</p>
                </div>
            </div>
            
            <p style="font-size: 1rem; margin-bottom: 25px; line-height: 1.7;">
                لماذا تم ترشيح جازان؟ لأنها المنطقة الوحيدة التي تدمج بين <strong>الاستهداف القطاعي للأغذية</strong> وبين <strong>أقل تكلفة تشغيلية</strong> في المملكة.
            </p>

            <div class="features-grid">
                <div class="feature-box">
                    <h4><i class="fas fa-utensils" style="color:var(--primary)"></i> التخصص في الأغذية</h4>
                    <p style="font-size:0.9rem">ورد في وثائق الهيئة صراحةً أن "معالجة الأغذية" قطاع رئيسي مستهدف، مما يعني بنية تحتية جاهزة.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-money-bill-wave" style="color:var(--primary)"></i> السيولة الفورية</h4>
                    <p style="font-size:0.9rem">الإعفاء من ضريبة القيمة المضافة وتأجيل الرسوم الجمركية يوفر سيولة نقدية فورية عند الاستيراد.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-globe-africa" style="color:var(--primary)"></i> بوابة التصدير</h4>
                    <p style="font-size:0.9rem">موقعها على البحر الأحمر يجعلها الأقرب للأسواق الأفريقية، مما يقلل تكاليف الشحن.</p>
                </div>
            </div>

            <div style="text-align: center;">
                <a href="https://www.investjcpdi.com" target="_blank" class="btn-main">
                    البدء في إجراءات الاستثمار
                    <i class="fas fa-arrow-left"></i>
                </a>
            </div>
        </section>

        <section class="card funding-section">
            <h2 class="section-title">مصادر التمويل (بدون فوائد ربوية)</h2>
            <p style="text-align: center; font-size: 0.95rem; color: #555; margin-bottom: 25px;">
                تتميز المملكة بوجود صناديق تنموية تدعم القطاع الصناعي والغذائي برسوم إدارية رمزية.
            </p>

            <div class="loans-grid">
                <div class="loan-card">
                    <i class="fas fa-industry loan-icon"></i>
                    <h3>صندوق التنمية الصناعية (SIDF)</h3>
                    <p style="font-size: 0.9rem;">يقدم قروضاً للمصانع تصل إلى <strong>75%</strong> من تكلفة المشروع.</p>
                    <span class="fee-badge">رسوم إدارية فقط</span>
                </div>

                <div class="loan-card">
                    <i class="fas fa-seedling loan-icon"></i>
                    <h3>صندوق التنمية الزراعية (ADF)</h3>
                    <p style="font-size: 0.9rem;">مخصص لمشاريع <strong>"الأمن الغذائي"</strong> واستيراد المواد الخام.</p>
                    <span class="fee-badge">أولوية قصوى للأغذية</span>
                </div>

                <div class="loan-card">
                    <i class="fas fa-hand-holding-usd loan-icon"></i>
                    <h3>حوافز المنطقة الاقتصادية</h3>
                    <p style="font-size: 0.9rem;">دعم مالي غير مباشر عبر الإعفاءات الجمركية والضريبية.</p>
                    <span class="fee-badge" style="background: #dcfce7; color: #166534;">توفير كاش فوري</span>
                </div>
            </div>
        </section>

        <section class="card gov-links-section">
            <h2 class="section-title" style="font-size: 1.5rem;">الوصول المباشر للجهات الرسمية</h2>
            <div class="gov-links-grid">
                
                <a href="https://site.ecza.gov.sa/ar" target="_blank" class="gov-link-card">
                    <i class="fas fa-university gov-icon"></i>
                    <span class="gov-name">هيئة المدن (ECZA)</span>
                </a>

                <a href="https://www.sidf.gov.sa/ar" target="_blank" class="gov-link-card">
                    <i class="fas fa-cogs gov-icon"></i>
                    <span class="gov-name">الصندوق الصناعي (SIDF)</span>
                </a>

                <a href="https://www.adf.gov.sa/ar/Pages/default.aspx" target="_blank" class="gov-link-card">
                    <i class="fas fa-leaf gov-icon"></i>
                    <span class="gov-name">الصندوق الزراعي (ADF)</span>
                </a>

                <a href="https://misa.gov.sa/ar" target="_blank" class="gov-link-card">
                    <i class="fas fa-briefcase gov-icon"></i>
                    <span class="gov-name">وزارة الاستثمار (MISA)</span>
                </a>

                <a href="https://investsaudi.sa/ar/" target="_blank" class="gov-link-card">
                    <i class="fas fa-rocket gov-icon"></i>
                    <span class="gov-name">برنامج المستثمر الاستراتيجي</span>
                </a>

            </div>
        </section>

    </div>

    <footer>
        <span class="creator-badge">إعداد / نصار منصور الغريب</span>
        <p>تم إعداد هذا العرض بناءً على البيانات الرسمية لهيئة المدن والمناطق الاقتصادية الخاصة (ECZA) والصناديق التنموية.</p>
        <p style="font-size: 0.8rem; margin-top: 10px; opacity: 0.6;">&copy; 2024 جميع الحقوق محفوظة لمجموعة بن عوض النقيب</p>
    </footer>

</body>
</html>
