<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عرض استثماري - مجموعة بن عوض النقيب</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #006C35; /* أخضر سعودي */
            --secondary: #CBA258; /* ذهبي */
            --accent: #1e3a8a; /* أزرق داكن */
            --bg-light: #f3f4f6;
            --white: #ffffff;
            --text: #1f2937;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            margin: 0;
            background-color: var(--bg-light);
            color: var(--text);
            line-height: 1.6;
        }

        /* الهيدر المخصص للمجموعة */
        header {
            background: linear-gradient(135deg, var(--primary), #004d25);
            color: var(--white);
            padding: 4rem 1rem;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            border-bottom: 5px solid var(--secondary);
        }

        header h1 { margin: 0; font-size: 2.2rem; font-weight: 900; margin-bottom: 10px; }
        header h2 { margin: 0; font-size: 1.8rem; font-weight: 700; color: var(--secondary); }
        header p { font-size: 1.1rem; opacity: 0.95; margin-top: 15px; max-width: 800px; margin-left: auto; margin-right: auto;}

        /* الحاوية */
        .container { max-width: 1200px; margin: -50px auto 0; padding: 0 20px 50px; position: relative; z-index: 10; }

        /* البطاقات والأقسام */
        .card {
            background: var(--white);
            border-radius: 12px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1);
            transition: transform 0.2s;
        }
        
        .section-title {
            color: var(--primary);
            border-right: 5px solid var(--secondary);
            padding-right: 15px;
            margin-bottom: 20px;
            font-size: 1.5rem;
            font-weight: 700;
        }

        /* الجداول */
        .table-responsive { overflow-x: auto; }
        table { width: 100%; border-collapse: collapse; min-width: 900px; }
        th { background-color: var(--primary); color: var(--white); padding: 15px; text-align: right; }
        td { padding: 15px; border-bottom: 1px solid #e5e7eb; }
        tr:hover { background-color: #f9fafb; }
        
        .source-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        .source-link:hover { text-decoration: underline; }

        /* التوصية */
        .recommendation { border: 2px solid var(--primary); background: #f0fdf4; }
        .recommendation h2 { color: var(--primary); display: flex; align-items: center; gap: 10px; margin-top: 0; }

        /* قسم التمويل */
        .finance-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        .finance-item {
            background: #fff;
            border: 1px solid #e5e7eb;
            border-radius: 8px;
            padding: 20px;
            border-top: 4px solid var(--secondary);
        }
        .finance-item h3 { margin-top: 0; color: #333; }
        .finance-source {
            font-size: 0.9rem;
            color: #666;
            margin-top: 10px;
            display: block;
            font-weight: bold;
        }

        /* أزرار التواصل */
        .btn-contact {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 10px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
            margin-top: 10px;
        }
        .btn-contact:hover { background-color: var(--secondary); transform: translateY(-2px); }

        /* الفوتر المخصص */
        footer { 
            text-align: center; 
            padding: 30px; 
            background-color: #1f2937;
            color: #d1d5db; 
            font-size: 0.95rem; 
            margin-top: 20px;
            border-top: 4px solid var(--secondary);
        }
        .footer-credit {
            font-size: 1.1rem;
            font-weight: bold;
            color: var(--secondary);
            margin-bottom: 10px;
            display: block;
        }
    </style>
</head>
<body>

    <header>
        <h1>فرص الاستثمار الصناعي في المملكة العربية السعودية</h1>
        <h2>إهداء إلى مجموعة بن عوض النقيب</h2>
        <p>دراسة تحليلية لأفضل المناطق الاقتصادية لتأسيس مصانع المواد الغذائية، مدعومة بالحوافز الحكومية وحلول التمويل</p>
    </header>

    <div class="container">

        <section class="card recommendation">
            <h2><i class="fas fa-star" style="color: var(--secondary);"></i> التوصية الاستثمارية: منطقة جازان (JCPDI)</h2>
            <p>بعد تحليل المناطق الاقتصادية، نوصي <strong>مجموعة بن عوض النقيب</strong> باختيار منطقة جازان للأسباب التالية:</p>
            <ul>
                <li><strong>الاستهداف القطاعي:</strong> المنطقة الوحيدة المخصصة صراحةً لقطاع "معالجة الأغذية".</li>
                <li><strong>خفض التكاليف:</strong> توفر طاقة ومياه بأسعار صناعية مدعومة، مما يرفع هامش الربح.</li>
                <li><strong>بوابة التصدير:</strong> امتلاكها ميناءً صناعياً ضخماً على البحر الأحمر يسهل الوصول للأسواق الأفريقية.</li>
            </ul>
            <a href="https://www.investjcpdi.com" target="_blank" class="btn-contact">
                <i class="fas fa-external-link-alt"></i> زيارة الموقع الرسمي للمنطقة
            </a>
        </section>

        <section class="card">
            <h2 class="section-title">مقارنة المناطق (تحليل فني)</h2>
            <div class="table-responsive">
                <table>
                    <thead>
                        <tr>
                            <th>المنطقة</th>
                            <th>القطاعات المستهدفة</th>
                            <th>المزايا المالية والضريبية</th>
                            <th>البنية التحتية</th>
                            <th>المصدر الرسمي</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>جازان (JCPDI)</strong></td>
                            <td>معالجة الأغذية، تحويل المعادن</td>
                            <td>5% ضريبة دخل (20 عاماً)، 0% ضريبة قيمة مضافة</td>
                            <td>طاقة رخيصة، مياه متعددة الخيارات</td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" class="source-link">عرض المصدر <i class="fas fa-arrow-left"></i></a></td>
                        </tr>
                        <tr>
                            <td><strong>مدينة الملك عبدالله (KAEC)</strong></td>
                            <td>السلع الاستهلاكية، السيارات</td>
                            <td>5% ضريبة دخل، إعفاء جمركي</td>
                            <td>ميناء عالمي، غاز طبيعي</td>
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" class="source-link">عرض المصدر <i class="fas fa-arrow-left"></i></a></td>
                        </tr>
                        <tr>
                            <td><strong>اللوجستية بالرياض (RISLZ)</strong></td>
                            <td>الخدمات اللوجستية، التجميع</td>
                            <td>إعفاء ضريبي 50 عاماً</td>
                            <td>موقع جوي استراتيجي</td>
                            <td><a href="https://www.silz.gaca.gov.sa" target="_blank" class="source-link">عرض المصدر <i class="fas fa-arrow-left"></i></a></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section class="card">
            <h2 class="section-title">حلول التمويل والدعم المالي</h2>
            <div class="finance-grid">
                <div class="finance-item">
                    <h3><i class="fas fa-money-bill-wave" style="color: var(--primary);"></i> تعزيز السيولة النقدية</h3>
                    <p>تأجيل الرسوم الجمركية وإعفاء ضريبة القيمة المضافة يوفر سيولة فورية للمجموعة عند التأسيس.</p>
                    <span class="finance-source">المصدر: حوافز المنطقة الاقتصادية</span>
                </div>
                <div class="finance-item">
                    <h3><i class="fas fa-industry" style="color: var(--primary);"></i> التمويل الصناعي</h3>
                    <p>قروض ميسرة تصل إلى 75% من تكلفة المشروع للمصانع.</p>
                    <span class="finance-source">الجهة: <a href="https://www.sidf.gov.sa" target="_blank">صندوق التنمية الصناعية</a></span>
                </div>
                <div class="finance-item">
                    <h3><i class="fas fa-seedling" style="color: var(--primary);"></i> تمويل الأمن الغذائي</h3>
                    <p>تسهيلات ائتمانية خاصة لمشاريع الإنتاج الغذائي.</p>
                    <span class="finance-source">الجهة: <a href="https://adf.gov.sa" target="_blank">صندوق التنمية الزراعية</a></span>
                </div>
            </div>
        </section>

        <section class="card" style="text-align: center;">
            <h2 class="section-title" style="display:inline-block; border:none; margin-bottom:10px;">ابدأ استثمارك الآن</h2>
            <p style="margin-bottom: 25px;">روابط مباشرة للجهات الحكومية:</p>
            
            <div style="display: flex; gap: 15px; justify-content: center; flex-wrap: wrap;">
                <a href="https://site.ecza.gov.sa/ar" target="_blank" class="btn-contact">
                    هيئة المدن والمناطق الاقتصادية (ECZA)
                </a>
                <a href="https://www.misa.gov.sa" target="_blank" class="btn-contact" style="background-color: #004d25;">
                    وزارة الاستثمار (MISA)
                </a>
                <a href="mailto:info-investors@rcjy.gov.sa" class="btn-contact" style="background-color: var(--secondary);">
                    تواصل معنا (بريد إلكتروني)
                </a>
            </div>
        </section>

    </div>

    <footer>
        <span class="footer-credit">إعداد / نصار منصور الغريب</span>
        <p>المصادر: وثائق هيئة المدن والمناطق الاقتصادية الخاصة (ECZA)</p>
    </footer>

</body>
</html>
