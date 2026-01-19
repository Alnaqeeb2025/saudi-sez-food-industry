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

        table { width: 100%; border-collapse: collapse; min-width: 1000px; /* زيادة العرض لاستيعاب المحتوى الجديد */ }
        th { background: var(--primary); color: white; padding: 15px; text-align: right; font-size: 1rem; white-space: nowrap; vertical-align: top; }
        td { padding: 12px; border-bottom: 1px solid #eee; color: var(--text-dark); vertical-align: top; font-size: 0.9rem; }
        tr:nth-child(even) { background-color: #f8fafc; }
        
        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-bottom: 3px;
            background: #e0f2fe; color: #0369a1;
        }
        
        ul.table-list {
            list-style-type: disc;
            padding-right: 20px;
            margin: 0;
        }
        ul.table-list li { margin-bottom: 5px; }

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
                            <th width="15%">المنطقة</th>
                            <th width="25%">القطاعات المستهدفة</th>
                            <th width="25%">الحوافز</th>
                            <th width="25%">المزايا / التسهيلات</th>
                            <th width="10%">الموقع الرسمي</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td style="font-weight:bold;">المنطقة الاقتصادية الخاصة بمدينة الملك عبد الله الاقتصادية (KAEC) – مكة</td>
                            <td>
                                <ul class="table-list">
                                    <li>سلسلة إمداد السيارات وتجميعها</li>
                                    <li>السلع الاستهلاكية</li>
                                    <li>الصناعات الإلكترونية الخفيفة</li>
                                    <li>الأدوية</li>
                                    <li>التقنيات الطبية</li>
                                    <li>الخدمات اللوجستية</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>5% ضريبة دخل الشركات لمدة 20 عامًا</li>
                                    <li>0% ضريبة الاقتطاع (دائمًا) على إعادة الأرباح إلى دول أجنبية</li>
                                    <li>0% الرسوم الجمركية المؤجلة على البضائع المدخلة</li>
                                    <li>لوائح مرنة للمواهب الأجنبية خلال أول 5 سنوات</li>
                                    <li>0% ضريبة القيمة المضافة على السلع داخل المنطقة والمتبادلة داخلها وبين المناطق</li>
                                    <li>إعفاء من الرسوم التشغيلية للموظفين الأجانب وعائلاتهم داخل المنطقة</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>موقع جيوستراتيجي على البحر الأحمر يسهّل الوصول لسلاسل الإمداد العالمية، مع ربط سككي عالي السرعة (450 كم) ووصول للكفاءات الماهرة وقرب من مطار الملك عبدالعزيز وجدة</li>
                                    <li>بنية مرافق عالية الجودة: كهرباء (أكثر من 29 جيجاوات/ساعة سنويًا من طاقة نظيفة – خطط قيد التنفيذ)، ألياف ضوئية، صرف صحي مترابط (مفاعل حيوي غشائي)، مياه بضغط 1.5 بار (حد أدنى)، وتزويد بغاز طبيعي “بتكلفة مناسبة”</li>
                                </ul>
                            </td>
                            <td><a href="https://www.kaec.net/kaecsez" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>

                        <tr>
                            <td style="font-weight:bold;">المنطقة الاقتصادية الخاصة برأس الخير – المنطقة الشرقية</td>
                            <td>
                                <ul class="table-list">
                                    <li>بناء السفن (الصيانة/الإصلاح/التشغيل)</li>
                                    <li>منصات الحفر العائمة (الصيانة/الإصلاح/التشغيل)</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>5% ضريبة دخل الشركات لمدة 20 عامًا</li>
                                    <li>0% ضريبة الاقتطاع (دائمًا) على إعادة الأرباح إلى دول أجنبية</li>
                                    <li>0% الرسوم الجمركية المؤجلة على البضائع المدخلة</li>
                                    <li>لوائح مرنة للمواهب الأجنبية خلال أول 5 سنوات</li>
                                    <li>0% ضريبة القيمة المضافة على السلع داخل المنطقة والمتبادلة داخلها وبين المناطق</li>
                                    <li>إعفاء من الرسوم التشغيلية للموظفين الأجانب وعائلاتهم داخل المنطقة</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>قربها من ميناء رأس الخير (أحدث ميناء صناعي) يخدم الشحنات السائبة وأكثر من 100 مشروع تصنيع، ويستقبل السفن بمختلف أحجامها</li>
                                    <li>ربط سككي شمال–جنوب للوصول إلى مواد المدخلات، وقرب من مطار الملك فهد الدولي (43 وجهة)، وحوض بناء سفن “الأكبر في الشرق الأوسط وشمال أفريقيا” مع خدمات بناء/صيانة/إصلاح/ترميم</li>
                                </ul>
                            </td>
                            <td><a href="https://www.rcjy.gov.sa" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>

                        <tr style="background-color: #f0fdf4; border: 2px solid var(--primary);">
                            <td style="font-weight:bold; color:var(--primary);">المنطقة الاقتصادية الخاصة بجازان – جازان <i class="fas fa-star" style="color:var(--gold);"></i></td>
                            <td>
                                <ul class="table-list">
                                    <li>معالجة الأغذية</li>
                                    <li>تحويل المعادن</li>
                                    <li>الخدمات اللوجستية</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>5% ضريبة دخل الشركات لمدة 20 عامًا</li>
                                    <li>0% ضريبة الاقتطاع (دائمًا) على إعادة الأرباح إلى دول أجنبية</li>
                                    <li>0% الرسوم الجمركية المؤجلة على البضائع المدخلة</li>
                                    <li>لوائح مرنة للمواهب الأجنبية خلال أول 5 سنوات</li>
                                    <li>0% ضريبة القيمة المضافة على السلع داخل المنطقة والمتبادلة داخلها وبين المناطق</li>
                                    <li>إعفاء من الرسوم التشغيلية للموظفين الأجانب وعائلاتهم داخل المنطقة</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    [cite_start]<li>الوصول إلى أحد أكبر الموانئ في المنطقة لتصدير السلع واستيراد مواد التصنيع [cite: 887]</li>
                                    [cite_start]<li>توفر “كل ما تحتاجه” من الخدمات (الكهرباء/المياه/الأراضي/المواهب) لضمان مشروع فعال وتنافسي [cite: 887]</li>
                                    [cite_start]<li>وصول مباشر لمواد خام (مثل الحجر الجيري/الجبس/الرمل/التراب الكلسي/الغاز الطبيعي) وقرب من مجمع مصفاة جازان في أرامكو [cite: 887]</li>
                                    [cite_start]<li>طاقة منخفضة التكلفة (تشمل 2.4 جيجاوات)، قوى عاملة ماهرة، عقد إيجار صناعي تنافسي، وخيارات مياه منخفضة التكلفة [cite: 887]</li>
                                </ul>
                            </td>
                            <td><a href="https://www.investjcpdi.com" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>

                        <tr>
                            <td style="font-weight:bold;">المنطقة الاقتصادية الخاصة للحوسبة السحابية والمعلوماتية – مقرها الرياض (غير مرتبطة بموقع محدد)</td>
                            <td>
                                <ul class="table-list">
                                    <li>خدمات الحوسبة السحابية</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>معاملة ضريبية خاصة تتماشى مع مبدأ تجنب الازدواج الضريبي لمنظمة التعاون والتنمية الاقتصادية وبما يتوافق مع نموذج تشغيل مزودي الخدمات السحابية</li>
                                    <li>تكلفة كهرباء للشركات 0.05 دولار/كيلوواط-ساعة</li>
                                    <li>إعفاء من الرسوم التشغيلية للموظفين الأجانب وعائلاتهم داخل المنطقة</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>غير مرتبطة بموقع جغرافي محدد: مقرها في الرياض (برج الابتكار بمدينة الملك عبدالعزيز للعلوم والتقنية) مع إمكانية إنشاء وتشغيل مراكز البيانات في جميع أنحاء المملكة</li>
                                    <li>مرونة تقديم خدمات الحوسبة السحابية وإمكانية إنشاء/تشغيل مراكز البيانات من أنحاء المملكة</li>
                                </ul>
                            </td>
                            <td><a href="https://www.cst.gov.sa" target="_blank" class="btn-link">زيارة</a></td>
                        </tr>

                        <tr>
                            <td style="font-weight:bold;">المنطقة الخاصة اللوجستية المتكاملة في الرياض (SILZ) – الرياض</td>
                            <td>
                                <ul class="table-list">
                                    <li>المنتجات الاستهلاكية</li>
                                    <li>أجزاء الحاسوب</li>
                                    <li>الأدوية</li>
                                    <li>المستلزمات الغذائية والطبية</li>
                                    <li>صناعة الفضاء وقطاع الغيار</li>
                                    <li>السلع الكمالية والمجوهرات والمعادن النفيسة</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>إعفاء من الرسوم الجمركية على السلع المستوردة أو المنقولة داخل المنطقة</li>
                                    <li>إعفاء من ضريبة القيمة المضافة على البضائع الداخلة لأنشطة الخدمة أو التصنيع</li>
                                    <li>معدل ضريبة دخل 0% على أنشطة محددة</li>
                                    <li>مزايا ضريبية تنافسية إضافية: 0% ضريبة دخل الشركات، إعفاءات ضريبة الاستقطاع، إعفاءات رسوم تحويل الأموال، إعفاءات على ضريبة القيمة المضافة، وإعفاءات ضريبية لمدة 50 عامًا</li>
                                </ul>
                            </td>
                            <td>
                                <ul class="table-list">
                                    <li>مزايا تسهيل ممارسة الأعمال: منصة موحدة للخدمات، ممر يربط مطار الملك خالد بالمناطق الأخرى، الإعفاء من قيود إعادة رأس المال، التصديق السريع للتصدير، إعفاء البضائع من الرسوم الجمركية، متطلبات مرنة للتوطين، و ملكية أجنبية 100%</li>
                                </ul>
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
