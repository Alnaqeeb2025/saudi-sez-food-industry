<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عرض استثماري - مجموعة بن عوض النقيب</title>
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

        body {
            font-family: 'Tajawal', sans-serif;
            margin: 0;
            background-color: var(--bg-body);
            color: var(--text-dark);
            line-height: 1.8;
            padding-bottom: 0;
        }

        /* --- الهيدر الفخم --- */
        header {
            background: linear-gradient(135deg, var(--primary), #003322);
            color: var(--white);
            padding: 5rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 8px solid var(--gold);
        }

        header::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background-image: url('https://www.transparenttextures.com/patterns/cubes.png');
            opacity: 0.1;
        }

        .header-content { position: relative; z-index: 2; }
        
        header h1 { 
            margin: 0; 
            font-size: 2.8rem; 
            font-weight: 800; 
            margin-bottom: 15px;
            letter-spacing: -1px;
        }

        .dedication {
            background-color: rgba(255,255,255,0.1);
            display: inline-block;
            padding: 10px 30px;
            border-radius: 50px;
            border: 1px solid var(--gold);
            margin-bottom: 20px;
        }

        .dedication h2 {
            margin: 0;
            font-size: 1.5rem;
            color: var(--gold-light);
            font-weight: 700;
        }

        /* --- الحاويات والبطاقات --- */
        .container { 
            max-width: 1200px; 
            margin: -60px auto 0; 
            padding: 0 20px 60px;
            position: relative; 
            z-index: 10; 
        }

        .card {
            background: var(--white);
            border-radius: 20px;
            padding: 2.5rem;
            margin-bottom: 2.5rem;
            box-shadow: 0 15px 30px rgba(0,0,0,0.05);
            border-top: 5px solid transparent;
        }

        .card:hover { transform: translateY(-5px); box-shadow: 0 20px 40px rgba(0,0,0,0.1); }

        .section-title {
            text-align: center;
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 30px;
            position: relative;
            font-weight: 800;
        }

        /* --- الجدول --- */
        .table-container { overflow-x: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; min-width: 900px; background: white; }
        th { background: var(--primary); color: white; padding: 18px; text-align: right; font-size: 1.1rem; }
        td { padding: 15px; border-bottom: 1px solid #eee; color: var(--text-dark); vertical-align: middle; }
        tr:last-child td { border-bottom: none; }
        tr:nth-child(even) { background-color: #f8fafc; }
        
        .badge {
            display: inline-block;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 0.85rem;
            font-weight: bold;
            margin-bottom: 5px;
        }
        .badge-sector { background: #e0f2fe; color: #0369a1; }
        .badge-infra { background: #f0fdf4; color: #15803d; }

        /* --- التوصية الاستثمارية --- */
        .recommendation { border-top-color: var(--gold); background: linear-gradient(to bottom, #ffffff, #fffdf7); }
        .rec-header { display: flex; align-items: center; gap: 15px; margin-bottom: 20px; border-bottom: 2px solid #eee; padding-bottom: 15px; }
        .rec-icon { font-size: 2rem; color: var(--gold); }
        .rec-title { color: var(--primary); font-size: 1.8rem; margin: 0; font-weight: 800; }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .feature-box {
            background: white;
            padding: 20px;
            border-radius: 12px;
            border: 1px solid #eee;
            border-right: 4px solid var(--primary);
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }
        .feature-box h4 { margin: 0 0 10px 0; color: var(--primary); font-size: 1.2rem; }

        /* --- قسم التمويل --- */
        .funding-section { border-top-color: var(--primary); }
        .loans-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        .loan-card {
            background: #fff;
            border: 1px solid #e2e8f0;
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        .loan-card::before {
            content: '';
            position: absolute;
            top: 0; right: 0; width: 100%; height: 5px;
            background: var(--gold);
        }
        .loan-icon { font-size: 2.5rem; color: var(--primary); margin-bottom: 15px; }
        .fee-badge {
            background: #fee2e2;
            color: #991b1b;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            display: inline-block;
            margin-top: 10px;
        }

        /* --- قسم الروابط الحكومية (جديد) --- */
        .gov-links-section {
            text-align: center;
        }
        .gov-links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
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
            padding: 20px;
            text-decoration: none;
            color: var(--text-dark);
            transition: all 0.3s ease;
        }
        .gov-link-card:hover {
            background: var(--white);
            border-color: var(--gold);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }
        .gov-icon {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 10px;
        }
        .gov-name {
            font-weight: bold;
            font-size: 1rem;
        }

        /* --- الأزرار --- */
        .btn-link {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            color: var(--primary);
            text-decoration: none;
            font-weight: bold;
            padding: 8px 15px;
            border: 1px solid var(--primary);
            border-radius: 50px;
            font-size: 0.9rem;
        }
        .btn-link:hover { background: var(--primary); color: white; }

        .btn-main {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background-color: var(--primary);
            color: white;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 4px 15px rgba(0,86,63,0.3);
            margin-top: 20px;
        }
        .btn-main:hover { background-color: var(--gold); transform: translateY(-3px); }

        /* --- الفوتر --- */
        footer {
            background-color: #1a202c;
            color: #a0aec0;
            text-align: center;
            padding: 40px 20px;
            margin-top: 0;
            border-top: 5px solid var(--gold);
        }
        .creator-badge {
            background: rgba(255,255,255,0.1);
            padding: 5px 20px;
            border-radius: 30px;
            color: var(--gold);
            font-weight: bold;
            font-size: 1.1rem;
            display: inline-block;
            margin-bottom: 15px;
            border: 1px solid rgba(197, 160, 89, 0.3);
        }

        @media (max-width: 768px) {
            header h1 { font-size: 1.8rem; }
            td, th { padding: 10px; font-size: 0.9rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-content">
            <div class="dedication">
                <h2>إهداء إلى مجموعة بن عوض النقيب</h2>
            </div>
            <h1>فرص الاستثمار الصناعي في المملكة</h1>
            <p style="font-size: 1.3rem; margin-top: 15px; font-weight: 500; color: var(--gold-light);">
                مقارنة بين المدن الاقتصادية في المملكة العربية السعودية لتأسيس مصانع المواد الغذائية
            </p>
        </div>
    </header>

    <div class="container">

        <section class="card">
            <h2 class="section-title">تحليل المناطق الاقتصادية والمزايا التنافسية</h2>
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
                                • 5% ضريبة دخل (20 عاماً)<br>
                                • 0% ضريبة قيمة مضافة<br>
                                • تأجيل الرسوم الجمركية
                            </td>
                            <td>
                                <span class="badge badge-infra">طاقة رخيصة (2.4 جيجاوات)</span><br>
                                <span class="badge badge-infra">خيارات مياه متعددة</span>
                            </td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" class="btn-link">زيارة <i class="fas fa-external-link-alt"></i></a></td>
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
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" class="btn-link">زيارة <i class="fas fa-external-link-alt"></i></a></td>
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
                            <td><a href="https://www.rcjy.gov.sa" target="_blank" class="btn-link">زيارة <i class="fas fa-external-link-alt"></i></a></td>
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
                            <td><a href="https://www.silz.gaca.gov.sa" target="_blank" class="btn-link">زيارة <i class="fas fa-external-link-alt"></i></a></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section class="card recommendation">
            <div class="rec-header">
                <i class="fas fa-crown rec-icon"></i>
                <div>
                    <h2 class="rec-title">ترشيح المنطقة الأنسب: جازان (JCPDI)</h2>
                    <p style="margin: 5px 0 0 0; color: #666;">الخيار الاستراتيجي لمجموعة بن عوض النقيب</p>
                </div>
            </div>
            
            <p style="font-size: 1.1rem; margin-bottom: 25px;">
                لماذا تم ترشيح جازان؟ لأنها المنطقة الوحيدة التي تدمج بين <strong>الاستهداف القطاعي للأغذية</strong> وبين <strong>أقل تكلفة تشغيلية</strong> في المملكة.
            </p>

            <div class="features-grid">
                <div class="feature-box">
                    <h4><i class="fas fa-utensils"></i> التخصص في الأغذية</h4>
                    <p>ورد في وثائق الهيئة صراحةً أن "معالجة الأغذية" قطاع رئيسي مستهدف، مما يعني بنية تحتية (مستودعات، تبريد، صرف) جاهزة لهذا النشاط.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-money-bill-wave"></i> السيولة الفورية</h4>
                    <p>الإعفاء من ضريبة القيمة المضافة (0%) وتأجيل الرسوم الجمركية يوفر سيولة نقدية فورية للمجموعة عند استيراد الآلات والمواد الخام.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-globe-africa"></i> بوابة التصدير</h4>
                    <p>موقعها على البحر الأحمر يجعلها الأقرب للأسواق الأفريقية، مما يقلل تكاليف الشحن ويسرع وصول المنتجات الغذائية (قصيرة الصلاحية).</p>
                </div>
            </div>

            <div style="text-align: center;">
                <a href="https://www.investjcpdi.com" target="_blank" class="btn-main">
                    البدء في إجراءات الاستثمار بمنطقة جازان
                    <i class="fas fa-arrow-left"></i>
                </a>
            </div>
        </section>

        <section class="card funding-section">
            <h2 class="section-title">مصادر التمويل في المملكة (بدون فوائد ربوية)</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto 30px auto;">
                تتميز المملكة بوجود صناديق تنموية تدعم القطاع الصناعي والغذائي برسوم إدارية رمزية أو مقابل خدمات، وليس بنظام الفوائد التجارية المركبة.
            </p>

            <div class="loans-grid">
                <div class="loan-card">
                    <i class="fas fa-industry loan-icon"></i>
                    <h3>صندوق التنمية الصناعية (SIDF)</h3>
                    <p>يقدم قروضاً للمصانع تصل إلى <strong>75%</strong> من تكلفة المشروع.</p>
                    <hr style="margin: 15px 0; border: 0; border-top: 1px dashed #ddd;">
                    <p style="font-size: 0.9rem; color: #555;"><strong>التكلفة:</strong> رسوم تقييم ومتابعة (مقابل خدمات) وليست فائدة سنوية.</p>
                    <span class="fee-badge">رسوم إدارية فقط</span>
                </div>

                <div class="loan-card">
                    <i class="fas fa-seedling loan-icon"></i>
                    <h3>صندوق التنمية الزراعية (ADF)</h3>
                    <p>مخصص لمشاريع <strong>"الأمن الغذائي"</strong> واستيراد المواد الخام الزراعية.</p>
                    <hr style="margin: 15px 0; border: 0; border-top: 1px dashed #ddd;">
                    <p style="font-size: 0.9rem; color: #555;"><strong>التكلفة:</strong> رسوم خدمات أو هوامش ربح منخفضة جداً ومدعومة.</p>
                    <span class="fee-badge">أولوية قصوى للأغذية</span>
                </div>

                <div class="loan-card">
                    <i class="fas fa-hand-holding-usd loan-icon"></i>
                    <h3>حوافز المنطقة الاقتصادية</h3>
                    <p>دعم مالي غير مباشر عبر الإعفاءات.</p>
                    <hr style="margin: 15px 0; border: 0; border-top: 1px dashed #ddd;">
                    <p style="font-size: 0.9rem; color: #555;">تأجيل جمركي + إعفاء ضريبي يوفر السيولة التشغيلية (Working Capital).</p>
                    <span class="fee-badge" style="background: #dcfce7; color: #166534;">توفير كاش فوري</span>
                </div>
            </div>
        </section>

        <section class="card gov-links-section">
            <h2 class="section-title" style="font-size: 1.6rem;">الوصول المباشر للجهات الرسمية</h2>
            <div class="gov-links-grid">
                
                <a href="https://site.ecza.gov.sa/ar" target="_blank" class="gov-link-card">
                    <i class="fas fa-university gov-icon"></i>
                    <span class="gov-name">هيئة المدن (ECZA)</span>
                </a>

                <a href="https://www.sidf.gov.sa/ar/Pages/default.aspx" target="_blank" class="gov-link-card">
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
