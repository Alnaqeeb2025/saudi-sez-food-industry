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
            padding-bottom: 50px;
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
            padding: 0 20px; 
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

        /* --- التوصية الاستثمارية --- */
        .recommendation { border-top-color: var(--gold); background: linear-gradient(to bottom, #ffffff, #fcfcfc); }
        .rec-header { display: flex; align-items: center; gap: 15px; margin-bottom: 20px; }
        .rec-icon { font-size: 2rem; color: var(--gold); }
        .rec-title { color: var(--primary); font-size: 1.8rem; margin: 0; font-weight: 800; }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .feature-box {
            background: #f0fdf4;
            padding: 20px;
            border-radius: 12px;
            border-right: 4px solid var(--primary);
        }
        .feature-box h4 { margin: 0 0 10px 0; color: var(--primary); font-size: 1.2rem; }

        /* --- قسم التحليل المالي (الإبداعي) --- */
        .financial-analysis { border-top-color: var(--primary); }
        
        .section-title {
            text-align: center;
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 40px;
            position: relative;
            display: inline-block;
            width: 100%;
        }
        
        /* مقارنة السيولة */
        .liquidity-compare {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }
        
        .scenario-box {
            flex: 1;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            position: relative;
        }
        
        .scenario-old { background: #fee2e2; border: 1px solid #fca5a5; opacity: 0.8; }
        .scenario-new { background: #dcfce7; border: 2px solid var(--primary); transform: scale(1.02); box-shadow: 0 10px 20px rgba(0,108,53,0.1); }
        
        .scenario-title { font-weight: bold; margin-bottom: 15px; display: block; font-size: 1.2rem; }
        .money-value { font-size: 2rem; font-weight: 900; display: block; margin: 10px 0; }
        .red-text { color: #dc2626; }
        .green-text { color: var(--primary); }

        /* قسم القروض */
        .loans-info {
            background: #fffbeb;
            border: 1px solid #fcd34d;
            border-radius: 15px;
            padding: 30px;
            margin-top: 30px;
        }
        .loans-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .loan-item { text-align: center; }
        .loan-item i { font-size: 2.5rem; color: var(--gold); margin-bottom: 15px; }
        .loan-item h3 { color: var(--text-dark); margin-bottom: 10px; }

        /* --- الجدول --- */
        .table-container { overflow-x: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.05); }
        table { width: 100%; border-collapse: collapse; min-width: 800px; background: white; }
        th { background: var(--primary); color: white; padding: 18px; text-align: right; }
        td { padding: 15px; border-bottom: 1px solid #eee; color: var(--text-gray); }
        tr:last-child td { border-bottom: none; }
        tr:nth-child(even) { background-color: #f8fafc; }

        /* --- الأزرار --- */
        .action-area { text-align: center; margin-top: 40px; }
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
        }
        .btn-main:hover { background-color: var(--gold); transform: translateY(-3px); }

        /* --- الفوتر --- */
        footer {
            background-color: #1a202c;
            color: #a0aec0;
            text-align: center;
            padding: 40px 20px;
            margin-top: 60px;
            border-top: 5px solid var(--gold);
        }
        .creator-badge {
            background: rgba(255,255,255,0.1);
            padding: 5px 15px;
            border-radius: 20px;
            color: var(--gold);
            font-weight: bold;
            display: inline-block;
            margin-bottom: 10px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
            .liquidity-compare { flex-direction: column; }
            .scenario-new { transform: scale(1); }
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
            <p style="font-size: 1.2rem; opacity: 0.9;">دراسة استراتيجية لتأسيس مصانع المواد الغذائية بأعلى كفاءة مالية وتشغيلية</p>
        </div>
    </header>

    <div class="container">

        <section class="card recommendation">
            <div class="rec-header">
                <i class="fas fa-crown rec-icon"></i>
                <h2 class="rec-title">الخيار الأمثل: المنطقة الاقتصادية الخاصة بجازان (JCPDI)</h2>
            </div>
            <p style="font-size: 1.1rem; margin-bottom: 20px;">
                بناءً على نشاط المجموعة في <strong>"الصناعات الغذائية"</strong>، تتفوق منطقة جازان على كافة المناطق الأخرى لثلاثة أسباب جوهرية:
            </p>
            <div class="features-grid">
                <div class="feature-box">
                    <h4><i class="fas fa-bullseye"></i> التخصص الدقيق</h4>
                    <p>المنطقة الوحيدة المصممة بنيتها التحتية خصيصاً لقطاع "معالجة الأغذية" واستقبال الحبوب والمواد الخام.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-bolt"></i> خفض التكاليف</h4>
                    <p>توفر طاقة كهربائية ضخمة ومياه صناعية بأسعار مدعومة، مما يقلل الفاتورة التشغيلية الشهرية.</p>
                </div>
                <div class="feature-box">
                    <h4><i class="fas fa-ship"></i> بوابة أفريقيا</h4>
                    <p>ميناء صناعي متطور على البحر الأحمر يضمن أسرع وصول لصادرات المجموعة إلى الأسواق الأفريقية.</p>
                </div>
            </div>
        </section>

        <section class="card financial-analysis">
            <h2 class="section-title">لماذا هذا الاستثمار مجدٍ مالياً للمجموعة؟</h2>

            <h3 style="margin-bottom: 20px; color: var(--text-dark);"><i class="fas fa-coins" style="color: var(--gold);"></i> 1. تعزيز السيولة النقدية (Immediate Liquidity)</h3>
            <p style="margin-bottom: 20px;">كيف يؤثر الإعفاء الضريبي (0% VAT) وتأجيل الجمارك على رأس المال العامل عند شراء الآلات ومواد البناء؟</p>
            
            <div class="liquidity-compare">
                <div class="scenario-box scenario-old">
                    <span class="scenario-title">خارج المنطقة الاقتصادية</span>
                    <i class="fas fa-money-bill-wave" style="font-size: 2rem; color: #dc2626; opacity: 0.5;"></i>
                    <p>تدفع 15% ضريبة + رسوم جمركية مقدماً</p>
                    <span class="money-value red-text">-15% كاش</span>
                    <p style="font-size: 0.9rem;">(أموال مجمدة لحين الاسترداد)</p>
                </div>

                <div class="scenario-box scenario-new">
                    <div style="position: absolute; top: -15px; left: 50%; transform: translateX(-50%); background: var(--gold); color: white; padding: 5px 15px; border-radius: 20px; font-weight: bold; font-size: 0.9rem;">ميزة للمجموعة</div>
                    <span class="scenario-title">داخل منطقة جازان (SEZ)</span>
                    <i class="fas fa-check-circle" style="font-size: 2rem; color: var(--primary);"></i>
                    <p>إعفاء كامل وتأجيل للرسوم</p>
                    <span class="money-value green-text">0% مدفوعات</span>
                    <p style="font-size: 0.9rem;"><strong>(السيولة تبقى في حساب المجموعة للتشغيل)</strong></p>
                </div>
            </div>

            <hr style="border: 0; border-top: 1px dashed #ddd; margin: 30px 0;">

            <h3 style="margin-bottom: 20px; color: var(--text-dark);"><i class="fas fa-hand-holding-usd" style="color: var(--gold);"></i> 2. هيكلة التمويل (تكلفة رأسمال منخفضة)</h3>
            <div class="loans-info">
                <p style="text-align: center; font-size: 1.1rem; margin-bottom: 20px;">
                    يمكن للمجموعة الاستفادة من الصناديق الحكومية التي تقدم تمويلاً <strong>بتكلفة إدارية رمزية</strong> وليس بفوائد تجارية ربوية.
                </p>
                <div class="loans-grid">
                    <div class="loan-item">
                        <i class="fas fa-industry"></i>
                        <h3>الصندوق الصناعي (SIDF)</h3>
                        <p>تمويل يصل لـ 75% من تكلفة المصنع.</p>
                        <span style="background: white; padding: 3px 10px; border-radius: 5px; font-size: 0.9rem; color: var(--primary);">رسوم إدارية فقط</span>
                    </div>
                    <div class="loan-item">
                        <i class="fas fa-wheat"></i>
                        <h3>الصندوق الزراعي (ADF)</h3>
                        <p>تمويل خاص لمشاريع "الأمن الغذائي".</p>
                        <span style="background: white; padding: 3px 10px; border-radius: 5px; font-size: 0.9rem; color: var(--primary);">أولوية قصوى</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="card">
            <h2 class="section-title" style="font-size: 1.5rem; margin-bottom: 20px;">مقارنة فنية سريعة</h2>
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>المنطقة</th>
                            <th>الميزة التنافسية للأغذية</th>
                            <th>الحوافز الضريبية</th>
                            <th>المصدر الرسمي</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td style="font-weight: bold; color: var(--primary);">جازان (JCPDI)</td>
                            <td>بيئة مخصصة للأغذية + طاقة رخيصة</td>
                            <td>5% ضريبة دخل + 0% قيمة مضافة</td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" style="color: var(--gold); text-decoration: none;">زيارة الموقع <i class="fas fa-external-link-alt"></i></a></td>
                        </tr>
                        <tr>
                            <td>مدينة الملك عبدالله</td>
                            <td>قربها من جدة وميناء عالمي</td>
                            <td>5% ضريبة دخل</td>
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" style="color: var(--text-gray); text-decoration: none;">زيارة الموقع</a></td>
                        </tr>
                        <tr>
                            <td>الرياض اللوجستية</td>
                            <td>قربها من المطار (توزيع سريع)</td>
                            <td>إعفاء ضريبي 50 عاماً</td>
                            <td><a href="https://www.silz.gaca.gov.sa" target="_blank" style="color: var(--text-gray); text-decoration: none;">زيارة الموقع</a></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <div class="action-area">
            <h3 style="margin-bottom: 20px;">الخطوة القادمة للمجموعة</h3>
            <a href="https://www.investjcpdi.com" target="_blank" class="btn-main">
                البدء في إجراءات منطقة جازان
                <i class="fas fa-arrow-left"></i>
            </a>
            <div style="margin-top: 20px;">
                <a href="https://www.misa.gov.sa" target="_blank" style="color: var(--text-gray); margin: 0 10px;">وزارة الاستثمار</a> | 
                <a href="https://site.ecza.gov.sa/ar" target="_blank" style="color: var(--text-gray); margin: 0 10px;">هيئة المدن والمناطق الاقتصادية</a>
            </div>
        </div>

    </div>

    <footer>
        <span class="creator-badge">إعداد / نصار منصور الغريب</span>
        <p>تم إعداد هذا العرض بناءً على البيانات الرسمية لهيئة المدن والمناطق الاقتصادية الخاصة (ECZA) والصناديق التنموية.</p>
        <p style="font-size: 0.8rem; margin-top: 10px; opacity: 0.6;">&copy; 2024 جميع الحقوق محفوظة لمجموعة بن عوض النقيب</p>
    </footer>

</body>
</html>
