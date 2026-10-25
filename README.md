[index.html](https://github.com/user-attachments/files/33938446/index.html.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إعدادية سيد الأنام | الموقع الرسمي والحسابات المدرسية</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Cairo -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                    },
                    colors: {
                        navy: {
                            800: '#1e3a8a',
                            900: '#0f172a',
                            950: '#080d1a'
                        },
                        gold: {
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706'
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Cairo', sans-serif;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        .hero-pattern {
            background-color: #0f172a;
            background-image: radial-gradient(at 10% 20%, rgba(30, 58, 138, 0.7) 0px, transparent 50%),
                              radial-gradient(at 90% 80%, rgba(5, 150, 105, 0.25) 0px, transparent 50%);
        }
        .login-bg {
            background-color: #080d1a;
            background-image: 
                radial-gradient(at 15% 15%, rgba(30, 58, 138, 0.55) 0px, transparent 45%),
                radial-gradient(at 85% 85%, rgba(217, 119, 6, 0.25) 0px, transparent 45%),
                radial-gradient(at 50% 50%, rgba(5, 150, 105, 0.15) 0px, transparent 60%);
        }
        html:not(.dark) .login-bg {
            background-color: #f1f5f9;
            background-image: 
                radial-gradient(at 15% 15%, rgba(30, 58, 138, 0.15) 0px, transparent 45%),
                radial-gradient(at 85% 85%, rgba(217, 119, 6, 0.15) 0px, transparent 45%),
                radial-gradient(at 50% 50%, rgba(5, 150, 105, 0.1) 0px, transparent 60%);
        }
        /* Robust Dark Mode Variables & Surfaces */
        html.dark body {
            background-color: #080d1a !important;
            color: #f1f5f9 !important;
        }
        html.dark header {
            background-color: rgba(15, 23, 42, 0.95) !important;
            border-color: #1e293b !important;
        }
        html.dark .bg-white {
            background-color: #0f172a !important;
            color: #f8fafc !important;
            border-color: #1e293b !important;
        }
        html.dark .bg-slate-50,
        html.dark .bg-slate-100 {
            background-color: #1e293b !important;
            color: #f1f5f9 !important;
            border-color: #334155 !important;
        }
        html.dark .text-navy-900,
        html.dark .text-slate-800,
        html.dark .text-slate-700,
        html.dark .text-slate-600 {
            color: #f1f5f9 !important;
        }
        html.dark input,
        html.dark select,
        html.dark textarea {
            background-color: #0b1329 !important;
            color: #ffffff !important;
            border-color: #334155 !important;
        }
        html.dark input::placeholder,
        html.dark textarea::placeholder {
            color: #94a3b8 !important;
        }
        html.dark table th {
            background-color: #1e293b !important;
            color: #e2e8f0 !important;
        }
        .card-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .card-hover:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 25px -5px rgba(15, 23, 42, 0.15), 0 8px 10px -6px rgba(15, 23, 42, 0.1);
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased selection:bg-gold-500 selection:text-white overflow-x-hidden">

    <!-- ========================================================== -->
    <!-- MANDATORY FULL-SCREEN ACCOUNT GATE (تسجيل حساب أو دخول) -->
    <!-- ========================================================== -->
    <div id="loginGateOverlay" class="fixed inset-0 z-[100] login-bg flex items-center justify-center p-4 overflow-y-auto transition-colors duration-300">
        
        <!-- Theme & Settings Bar on Login -->
        <div class="fixed top-4 left-4 z-[110] flex items-center gap-2">
            <button type="button" onclick="window.toggleTheme()" class="bg-navy-900/90 dark:bg-slate-800 text-gold-400 hover:scale-105 px-3.5 py-2 rounded-2xl shadow-lg border border-white/15 flex items-center gap-2 text-xs font-extrabold transition">
                <i id="loginThemeIcon" class="fa-solid fa-moon text-sm"></i>
                <span id="loginThemeText">الوضع الليلي</span>
            </button>
            <button type="button" onclick="window.openSettingsModal()" class="bg-white/90 dark:bg-slate-800 text-navy-900 dark:text-white hover:scale-105 px-3.5 py-2 rounded-2xl shadow-lg border border-slate-200 dark:border-slate-700 flex items-center gap-1.5 text-xs font-extrabold transition">
                <i class="fa-solid fa-sliders text-amber-500"></i>
                <span>الإعدادات</span>
            </button>
        </div>

        <div class="max-w-md w-full bg-white backdrop-blur-xl rounded-3xl shadow-2xl border border-slate-200 overflow-hidden my-auto">
            
            <div class="bg-gradient-to-b from-navy-900 to-navy-950 text-white p-6 text-center relative">
                <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-gold-400 to-gold-600 text-navy-950 flex items-center justify-center mx-auto mb-3 shadow-lg shadow-gold-500/30">
                    <i class="fa-solid fa-graduation-cap text-3xl"></i>
                </div>
                <span class="inline-block bg-white/10 text-gold-400 text-[11px] font-bold px-3 py-0.5 rounded-full mb-1 border border-white/10">بوابة الحسابات الرسمية</span>
                <h1 class="text-2xl sm:text-3xl font-black tracking-tight">إعدادية سيد الأنام</h1>
                <p class="text-xs text-slate-300 mt-1">أنشئ حسابك الخاص أو سجل دخولك للمتابعة للموقع</p>
            </div>

            <!-- Auth Mode Switcher -->
            <div class="grid grid-cols-3 bg-slate-100 p-1.5 m-5 mb-0 rounded-2xl border border-slate-200 gap-1">
                <button type="button" onclick="window.switchAuthTab('register')" id="authTabRegister" class="py-2.5 rounded-xl text-xs font-black transition flex items-center justify-center gap-1 bg-navy-900 text-white shadow">
                    <i class="fa-solid fa-user-plus"></i>
                    <span>حساب جديد</span>
                </button>
                <button type="button" onclick="window.switchAuthTab('login')" id="authTabLogin" class="py-2.5 rounded-xl text-xs font-bold text-slate-600 hover:text-navy-900 transition flex items-center justify-center gap-1">
                    <i class="fa-solid fa-right-to-bracket"></i>
                    <span>تسجيل دخول</span>
                </button>
                <button type="button" onclick="window.switchAuthTab('owner')" id="authTabOwner" class="py-2.5 rounded-xl text-xs font-bold text-slate-600 hover:text-navy-900 transition flex items-center justify-center gap-1">
                    <i class="fa-solid fa-crown text-amber-500"></i>
                    <span>الأونر</span>
                </button>
            </div>

            <!-- Form 1: Register New Student Account -->
            <form id="registerAccountForm" onsubmit="window.handleRegisterAccount(event)" class="p-6 pt-4 space-y-3.5">
                <div class="bg-blue-50 dark:bg-slate-800 p-3 rounded-2xl border border-blue-200 dark:border-slate-700 text-xs text-blue-900 dark:text-blue-200">
                    <p class="font-bold mb-0.5"><i class="fa-solid fa-circle-info"></i> كلمة المرور يجب أن تكون باللغة الإنجليزية، الأرقام أو الرموز فقط.</p>
                </div>
                <div>
                    <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1">الاسم الثلاثي أو الرباعي *</label>
                    <input type="text" id="regName" required placeholder="مثال: علي حسين محمد" class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-2.5 text-sm font-semibold focus:outline-none">
                </div>

                <div class="grid grid-cols-2 gap-3">
                    <div>
                        <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1">الصف *</label>
                        <select id="regGrade" required class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3 py-2.5 text-sm font-bold text-navy-900 focus:outline-none">
                            <option value="" disabled selected>اختر الصف...</option>
                            <option value="السادس العلمي">السادس العلمي</option>
                            <option value="السادس الأدبي">السادس الأدبي</option>
                            <option value="الخامس العلمي">الخامس العلمي</option>
                            <option value="الخامس الأدبي">الخامس الأدبي</option>
                            <option value="الرابع العلمي">الرابع العلمي</option>
                            <option value="الرابع الأدبي">الرابع الأدبي</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1">الشعبة *</label>
                        <select id="regSection" required class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3 py-2.5 text-sm font-bold text-navy-900 focus:outline-none">
                            <option value="" disabled selected>اختر الشعبة...</option>
                            <option value="أ">أ</option>
                            <option value="ب">ب</option>
                            <option value="ج">ج</option>
                            <option value="د">د</option>
                            <option value="هـ">هـ</option>
                            <option value="و">و</option>
                        </select>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1">كلمة مرور الحساب (إنجليزي وأرقام ورموز فقط) *</label>
                    <input type="password" id="regPassword" required placeholder="مثال: Ali123@#$" class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-2.5 text-sm font-mono font-bold focus:outline-none">
                </div>

                <button type="submit" class="w-full bg-gradient-to-l from-navy-800 to-navy-950 hover:from-navy-900 hover:to-black text-white font-black py-3 rounded-2xl shadow-lg flex items-center justify-center gap-2 transition">
                    <span>إنشاء الحساب والدخول</span>
                    <i class="fa-solid fa-arrow-left text-gold-400"></i>
                </button>
            </form>

            <!-- Form 2: Login Existing Student Account -->
            <form id="loginAccountForm" onsubmit="window.handleStudentLogin(event)" class="p-6 pt-4 space-y-4 hidden">
                <div>
                    <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1.5">الاسم الثلاثي أو الرباعي المسجل *</label>
                    <input type="text" id="loginStudentName" required placeholder="مثال: علي حسين محمد" class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-3 text-sm font-semibold focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-extrabold text-navy-900 dark:text-white mb-1.5">كلمة مرور حسابك *</label>
                    <input type="password" id="loginStudentPassword" required placeholder="أدخل كلمة المرور الخاصة بحسابك..." class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-3 text-sm font-mono font-bold focus:outline-none">
                </div>
                <p id="studentLoginError" class="text-xs text-red-600 font-bold hidden"><i class="fa-solid fa-circle-exclamation"></i> الاسم أو كلمة المرور غير صحيحة! تأكد من إنشاء حساب أولاً.</p>
                <button type="submit" class="w-full bg-gradient-to-l from-navy-800 to-navy-950 text-white font-black py-3.5 rounded-2xl shadow-lg flex items-center justify-center gap-2 transition">
                    <span>تسجيل الدخول إلى حسابي</span>
                    <i class="fa-solid fa-arrow-left text-gold-400"></i>
                </button>
            </form>

            <!-- Form 3: Owner Login -->
            <form id="ownerLoginForm" onsubmit="window.handleOwnerLogin(event)" class="p-6 pt-4 space-y-4 hidden">
                <div class="bg-amber-50 dark:bg-slate-800 border border-amber-200 dark:border-slate-700 rounded-2xl p-3 text-xs text-amber-900 dark:text-amber-200">
                    <p class="font-bold mb-0.5"><i class="fa-solid fa-shield-halved text-amber-600"></i> بوابة الأونر (مدير الموقع)</p>
                    <p>أدخل كلمة سر الأونر الخاصة بك.</p>
                </div>
                <div>
                    <div class="flex items-center justify-between mb-1">
                        <label class="block text-xs font-extrabold text-navy-900 dark:text-white">كلمة سر الأونر *</label>
                        <button type="button" onclick="window.fillDefaultOwnerPassword()" class="text-[11px] font-bold text-amber-600 hover:text-amber-700">تعبئة سريعة</button>
                    </div>
                    <input type="password" id="loginOwnerPassword" required placeholder="أدخل كلمة سر الأونر..." class="w-full bg-slate-50 border border-slate-300 rounded-xl px-3.5 py-3 text-sm font-mono font-bold focus:outline-none">
                    <p id="ownerLoginError" class="text-xs text-red-600 font-bold mt-1 hidden"><i class="fa-solid fa-circle-exclamation"></i> كلمة السر غير صحيحة!</p>
                </div>
                <button type="submit" class="w-full bg-gradient-to-l from-amber-500 to-gold-600 text-navy-950 font-black py-3.5 rounded-2xl shadow-lg flex items-center justify-center gap-2 transition">
                    <i class="fa-solid fa-key"></i>
                    <span>دخول بصلاحيات الأونر الكاملة</span>
                </button>
            </form>
        </div>
    </div>

    <!-- Top Status Bar -->
    <div class="bg-navy-950 text-slate-200 text-xs sm:text-sm py-2 px-4 border-b border-slate-800">
        <div class="max-w-7xl mx-auto flex flex-wrap justify-between items-center gap-2">
            <div class="flex items-center gap-2">
                <span id="userRoleBadge" class="bg-emerald-500 text-navy-950 font-black px-2.5 py-0.5 rounded-md text-xs">طالب مسجل</span>
                <p id="loggedInUserInfo" class="font-bold text-white text-xs sm:text-sm">مرحباً بك في إعدادية سيد الأنام</p>
            </div>
            <div class="flex items-center gap-2 text-xs">
                <button onclick="window.toggleTheme()" class="bg-slate-800 hover:bg-slate-700 text-gold-400 px-2.5 py-1 rounded-lg font-bold flex items-center gap-1.5 border border-slate-700 transition">
                    <i id="topBarThemeIcon" class="fa-solid fa-moon"></i>
                    <span class="hidden sm:inline">دارك / لايت</span>
                </button>
                <button onclick="window.openSettingsModal()" class="bg-slate-800 hover:bg-slate-700 text-white px-2.5 py-1 rounded-lg font-bold flex items-center gap-1.5 border border-slate-700 transition">
                    <i class="fa-solid fa-gear text-amber-400"></i>
                    <span>الإعدادات</span>
                </button>
                <button onclick="window.handleLogout()" class="bg-red-500/20 hover:bg-red-600 text-red-300 hover:text-white px-3 py-1 rounded-lg font-bold flex items-center gap-1.5 transition">
                    <i class="fa-solid fa-right-from-bracket"></i>
                    <span>خروج</span>
                </button>
            </div>
        </div>
    </div>

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-40 bg-white shadow-sm border-b border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-12 h-12 rounded-2xl bg-gradient-to-br from-navy-800 to-navy-950 flex items-center justify-center text-gold-400 shadow-md">
                        <i class="fa-solid fa-graduation-cap text-2xl"></i>
                    </div>
                    <div>
                        <h1 class="text-xl sm:text-2xl font-black text-navy-900 dark:text-white tracking-tight">إعدادية سيد الأنام</h1>
                        <p class="text-xs text-slate-500 dark:text-slate-400 font-semibold">للدراسة الإعدادية (العلمي والأدبي)</p>
                    </div>
                </a>

                <nav class="hidden lg:flex items-center gap-1">
                    <a href="#home" class="px-3 py-2 rounded-xl text-sm font-bold text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition">الرئيسية</a>
                    <a href="#teachers" class="px-3 py-2 rounded-xl text-sm font-bold text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition">الكادر التدريسي</a>
                    <a href="#malazim" class="px-3 py-2 rounded-xl text-sm font-bold text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition">مكتبة الملازم</a>
                    <a href="#schedule" class="px-3 py-2 rounded-xl text-sm font-bold text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition">الجدول الأسبوعي للدروس</a>
                    <a href="#announcements" class="px-3 py-2 rounded-xl text-sm font-bold text-slate-700 dark:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition">التبليغات</a>
                </nav>

                <div class="flex items-center gap-2">
                    <button onclick="window.openAddModal('studentsLog')" class="owner-only hidden bg-amber-100 dark:bg-amber-900/40 text-amber-900 dark:text-amber-200 px-3 py-2 rounded-xl text-xs font-extrabold flex items-center gap-1">
                        <i class="fa-solid fa-users-viewfinder"></i>
                        <span>الطلاب (<span id="navStudentLogCount">0</span>)</span>
                    </button>
                    <button onclick="window.openAddModal('teacher')" class="owner-only hidden bg-navy-800 text-white px-4 py-2 rounded-xl text-xs font-bold flex items-center gap-2">
                        <i class="fa-solid fa-crown text-gold-400"></i>
                        <span>لوحة الأونر</span>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Owner Mode Active Banner -->
    <div id="adminBanner" class="owner-only hidden bg-amber-50 dark:bg-slate-900 border-b border-amber-200 dark:border-slate-800 px-4 py-3">
        <div class="max-w-7xl mx-auto flex flex-wrap items-center justify-between gap-3 text-xs sm:text-sm font-black text-amber-950 dark:text-amber-200">
            <p><i class="fa-solid fa-crown text-amber-500"></i> أهلاً بك يا أونر الموقع! لديك الصلاحية الكاملة لإدارة المدرسين والملازم والجداول وحسابات الطلاب.</p>
            <div class="flex flex-wrap gap-2">
                <button onclick="window.openAddModal('teacher')" class="bg-navy-800 text-white px-3 py-1.5 rounded-lg text-xs">+ مدرس</button>
                <button onclick="window.openAddModal('malzama')" class="bg-emerald-600 text-white px-3 py-1.5 rounded-lg text-xs">+ ملزمة</button>
                <button onclick="window.openAddModal('schedule')" class="bg-sky-700 text-white px-3 py-1.5 rounded-lg text-xs">+ جدول الدروس</button>
                <button onclick="window.openAddModal('announcement')" class="bg-amber-600 text-white px-3 py-1.5 rounded-lg text-xs">+ تبليغ</button>
                <button onclick="window.openSettingsModal()" class="bg-slate-800 text-gold-400 px-3 py-1.5 rounded-lg text-xs">الإعدادات</button>
            </div>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="home" class="hero-pattern text-white relative py-16 sm:py-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
                <div class="lg:col-span-7 space-y-6 text-center lg:text-right">
                    <span class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/10 text-gold-400 text-xs sm:text-sm font-bold">
                        <i class="fa-solid fa-star"></i> صرح علمي وتربوي نحو التفوق
                    </span>
                    <h2 class="text-3xl sm:text-5xl lg:text-6xl font-black leading-tight">
                        مرحباً بكم في <br>
                        <span class="text-transparent bg-clip-text bg-gradient-to-l from-gold-400 to-yellow-200">إعدادية سيد الأنام</span>
                    </h2>
                    <p class="text-slate-300 text-base sm:text-lg leading-relaxed max-w-2xl mx-auto lg:mx-0">
                        المنصة الإلكترونية الرسمية لطلبتنا الأعزاء. استعرض الملازم والملخصات وجداول الدروس الأسبوعية وتعرف على الكادر التدريسي.
                    </p>
                    <div class="flex flex-wrap justify-center lg:justify-start gap-3">
                        <a href="#teachers" class="bg-gold-500 hover:bg-gold-600 text-navy-950 font-black px-6 py-3 rounded-2xl shadow-lg flex items-center gap-2">
                            <i class="fa-solid fa-chalkboard-user"></i> الكادر التدريسي
                        </a>
                        <a href="#schedule" class="bg-white/10 hover:bg-white/20 text-white border border-white/20 font-bold px-6 py-3 rounded-2xl flex items-center gap-2">
                            <i class="fa-solid fa-calendar-days text-gold-400"></i> الجدول الأسبوعي للدروس
                        </a>
                    </div>
                </div>

                <div class="lg:col-span-5">
                    <div class="bg-white/10 backdrop-blur-md border border-white/15 rounded-3xl p-6 sm:p-8 shadow-2xl space-y-6">
                        <h3 class="font-bold text-lg text-white border-b border-white/10 pb-3">إحصائيات المنصة المدرسية</h3>
                        <div class="grid grid-cols-2 gap-4 text-center">
                            <div class="bg-navy-950/60 p-4 rounded-2xl border border-white/10">
                                <span id="statTeachers" class="block text-3xl font-black text-gold-400">0</span>
                                <span class="text-xs text-slate-300 font-semibold mt-1 block">مدرس</span>
                            </div>
                            <div class="bg-navy-950/60 p-4 rounded-2xl border border-white/10">
                                <span id="statMalazim" class="block text-3xl font-black text-emerald-400">0</span>
                                <span class="text-xs text-slate-300 font-semibold mt-1 block">ملزمة</span>
                            </div>
                            <div class="bg-navy-950/60 p-4 rounded-2xl border border-white/10">
                                <span id="statSchedules" class="block text-3xl font-black text-sky-400">0</span>
                                <span class="text-xs text-slate-300 font-semibold mt-1 block">جدول دراسي</span>
                            </div>
                            <div class="bg-navy-950/60 p-4 rounded-2xl border border-white/10">
                                <span id="statAnnouncements" class="block text-3xl font-black text-amber-400">0</span>
                                <span class="text-xs text-slate-300 font-semibold mt-1 block">تبليغ</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Teachers Section -->
    <section id="teachers" class="py-16 sm:py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-4">
            <div>
                <span class="text-navy-800 dark:text-gold-400 font-bold text-sm mb-2 block"><span class="w-2.5 h-2.5 rounded-full bg-gold-500 inline-block ml-1.5"></span> نخبة الأساتذة</span>
                <h2 class="text-3xl sm:text-4xl font-black text-navy-900 dark:text-white">الكادر التدريسي في إعدادية سيد الأنام</h2>
            </div>
            <button onclick="window.openAddModal('teacher')" class="owner-only hidden bg-navy-800 text-white font-bold px-5 py-3 rounded-2xl text-sm flex items-center gap-2">
                <i class="fa-solid fa-user-plus text-gold-400"></i> إضافة مدرس وصورته
            </button>
        </div>

        <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200 dark:border-slate-800 mb-8 flex flex-col lg:flex-row gap-4 justify-between items-center">
            <div class="flex items-center gap-2 overflow-x-auto w-full lg:w-auto pb-2" id="subjectFilters">
                <button onclick="window.filterTeachersBySubject('الكل')" data-subject="الكل" class="subject-btn bg-navy-800 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">الكل</button>
                <button onclick="window.filterTeachersBySubject('التربية الإسلامية')" data-subject="التربية الإسلامية" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">التربية الإسلامية</button>
                <button onclick="window.filterTeachersBySubject('اللغة العربية')" data-subject="اللغة العربية" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">اللغة العربية</button>
                <button onclick="window.filterTeachersBySubject('اللغة الإنكليزية')" data-subject="اللغة الإنكليزية" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">اللغة الإنكليزية</button>
                <button onclick="window.filterTeachersBySubject('الرياضيات')" data-subject="الرياضيات" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">الرياضيات</button>
                <button onclick="window.filterTeachersBySubject('الفيزياء')" data-subject="الفيزياء" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">الفيزياء</button>
                <button onclick="window.filterTeachersBySubject('الكيمياء')" data-subject="الكيمياء" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">الكيمياء</button>
                <button onclick="window.filterTeachersBySubject('الأحياء')" data-subject="الأحياء" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">الأحياء</button>
                <button onclick="window.filterTeachersBySubject('اللغة الكردية')" data-subject="اللغة الكردية" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">اللغة الكردية</button>
                <button onclick="window.filterTeachersBySubject('جرائم حزب البعث')" data-subject="جرائم حزب البعث" class="subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0">جرائم حزب البعث</button>
            </div>
            <div class="relative w-full lg:w-72 shrink-0">
                <input type="text" id="teacherSearchInput" oninput="window.renderTeachers()" placeholder="ابحث عن اسم الأستاذ أو المادة..." class="w-full bg-slate-50 border border-slate-300 dark:border-slate-700 rounded-xl pr-10 pl-4 py-2.5 text-sm focus:outline-none">
                <i class="fa-solid fa-magnifying-glass absolute right-3.5 top-3 text-slate-400"></i>
            </div>
        </div>

        <div id="teachersGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6"></div>
    </section>

    <!-- Malazim Section -->
    <section id="malazim" class="py-16 sm:py-20 bg-slate-100/80 dark:bg-slate-900 border-y border-slate-200 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-4">
                <div>
                    <span class="text-emerald-700 dark:text-emerald-400 font-bold text-sm mb-2 block"><i class="fa-solid fa-book-bookmark ml-1"></i> المكتبة الإلكترونية</span>
                    <h2 class="text-3xl sm:text-4xl font-black text-navy-900 dark:text-white">مكتبة الملازم والملخصات الدراسية</h2>
                </div>
                <button onclick="window.openAddModal('malzama')" class="owner-only hidden bg-emerald-600 text-white font-bold px-5 py-3 rounded-2xl text-sm flex items-center gap-2">
                    <i class="fa-solid fa-file-arrow-up"></i> إضافة ملزمة جديدة
                </button>
            </div>

            <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200 dark:border-slate-800 mb-8 flex flex-col md:flex-row gap-4 justify-between items-center">
                <div class="flex flex-wrap items-center gap-2 w-full md:w-auto" id="stageFilters">
                    <button onclick="window.filterMalazimByStage('الكل')" data-stage="الكل" class="stage-btn bg-emerald-600 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">جميع المراحل</button>
                    <button onclick="window.filterMalazimByStage('السادس الإعدادي')" data-stage="السادس الإعدادي" class="stage-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">السادس الإعدادي</button>
                    <button onclick="window.filterMalazimByStage('الخامس الإعدادي')" data-stage="الخامس الإعدادي" class="stage-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">الخامس الإعدادي</button>
                    <button onclick="window.filterMalazimByStage('الرابع الإعدادي')" data-stage="الرابع الإعدادي" class="stage-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">الرابع الإعدادي</button>
                </div>
                <div class="flex items-center gap-2 w-full md:w-80">
                    <input type="text" id="malzamaSearchInput" oninput="window.renderMalazim()" placeholder="ابحث عن ملزمة أو أستاذ..." class="w-full bg-slate-50 border border-slate-300 dark:border-slate-700 rounded-xl pr-10 pl-4 py-2.5 text-sm focus:outline-none">
                </div>
            </div>

            <div id="malazimGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"></div>
        </div>
    </section>

    <!-- SCHEDULE SECTION: الجدول الأسبوعي للدروس -->
    <section id="schedule" class="py-16 sm:py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-4">
            <div>
                <span class="text-sky-600 dark:text-sky-400 font-bold text-sm mb-2 block"><i class="fa-solid fa-calendar-week ml-1"></i> الحصص والدوام</span>
                <h2 class="text-3xl sm:text-4xl font-black text-navy-900 dark:text-white">الجدول الأسبوعي للدروس</h2>
            </div>
            <button onclick="window.openAddModal('schedule')" class="owner-only hidden bg-sky-600 text-white font-bold px-5 py-3 rounded-2xl text-sm flex items-center gap-2">
                <i class="fa-solid fa-calendar-plus"></i> إضافة جدول جديد
            </button>
        </div>

        <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200 dark:border-slate-800 mb-8 flex flex-wrap items-center gap-2" id="scheduleFilters">
            <button onclick="window.filterScheduleByClass('الكل')" data-class="الكل" class="schedule-btn bg-sky-600 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">جميع الجداول</button>
            <button onclick="window.filterScheduleByClass('السادس العلمي')" data-class="السادس العلمي" class="schedule-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">السادس العلمي</button>
            <button onclick="window.filterScheduleByClass('السادس الأدبي')" data-class="السادس الأدبي" class="schedule-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">السادس الأدبي</button>
            <button onclick="window.filterScheduleByClass('الخامس الإعدادي')" data-class="الخامس الإعدادي" class="schedule-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">الخامس الإعدادي</button>
            <button onclick="window.filterScheduleByClass('الرابع الإعدادي')" data-class="الرابع الإعدادي" class="schedule-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold">الرابع الإعدادي</button>
        </div>

        <div id="scheduleGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"></div>
    </section>

    <!-- Announcements Section -->
    <section id="announcements" class="py-16 sm:py-20 bg-slate-100/80 dark:bg-slate-900 border-t border-slate-200 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-4">
                <div>
                    <span class="text-amber-600 dark:text-amber-400 font-bold text-sm mb-2 block"><i class="fa-solid fa-bullhorn ml-1"></i> إدارة المدرسة</span>
                    <h2 class="text-3xl sm:text-4xl font-black text-navy-900 dark:text-white">لوحة التبليغات الرسمية والقرارات</h2>
                </div>
                <button onclick="window.openAddModal('announcement')" class="owner-only hidden bg-amber-500 text-navy-950 font-black px-5 py-3 rounded-2xl text-sm flex items-center gap-2">
                    <i class="fa-solid fa-bell"></i> نشر تبليغ جديد
                </button>
            </div>
            <div id="announcementsGrid" class="grid grid-cols-1 md:grid-cols-2 gap-6"></div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-navy-950 text-slate-400 py-12 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center sm:text-right flex flex-col sm:flex-row justify-between items-center gap-4">
            <p>جميع الحقوق محفوظة &copy; <span id="currentYear"></span> لـ <strong>إعدادية سيد الأنام</strong></p>
            <p class="text-xs">تصميم المنصة الإلكترونية المدرسية</p>
        </div>
    </footer>

    <!-- SETTINGS MODAL -->
    <div id="settingsModal" class="fixed inset-0 z-[120] hidden bg-navy-950/75 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-3xl max-w-xl w-full shadow-2xl border border-slate-200 dark:border-slate-800 overflow-hidden my-8">
            <div class="bg-gradient-to-l from-navy-900 to-slate-900 text-white px-6 py-5 flex items-center justify-between">
                <h3 class="font-black text-lg"><i class="fa-solid fa-sliders text-amber-500 ml-1"></i> إعدادات الموقع والمظهر</h3>
                <button onclick="window.closeSettingsModal()" class="w-9 h-9 rounded-xl bg-white/10 text-white"><i class="fa-solid fa-xmark"></i></button>
            </div>
            <div class="p-6 space-y-6 max-h-[80vh] overflow-y-auto">
                <div class="bg-slate-50 dark:bg-slate-900 rounded-2xl p-4 border border-slate-200 dark:border-slate-800 space-y-3">
                    <h4 class="font-black text-navy-900 dark:text-white text-sm"><i class="fa-solid fa-palette text-amber-500 ml-1"></i> مظهر وخلفية الموقع (Dark / Light)</h4>
                    <div class="grid grid-cols-2 gap-3">
                        <button type="button" onclick="window.setThemeMode('light')" id="themeBtnLight" class="p-3 rounded-xl border border-slate-300 bg-white text-navy-900 font-bold text-xs flex items-center justify-center gap-2 transition">
                            <i class="fa-solid fa-sun text-amber-500"></i> الوضع النهاري
                        </button>
                        <button type="button" onclick="window.setThemeMode('dark')" id="themeBtnDark" class="p-3 rounded-xl border border-slate-700 bg-slate-900 text-white font-bold text-xs flex items-center justify-center gap-2 transition">
                            <i class="fa-solid fa-moon text-gold-400"></i> الوضع الليلي
                        </button>
                    </div>
                </div>

                <!-- Owner Only Password Change Section -->
                <div id="ownerPasswordSettingsSection" class="bg-slate-50 dark:bg-slate-900 rounded-2xl p-5 border border-slate-200 dark:border-slate-800 space-y-4 hidden">
                    <div class="flex items-center justify-between border-b border-slate-200 dark:border-slate-800 pb-3">
                        <h4 class="font-black text-navy-900 dark:text-white text-sm"><i class="fa-solid fa-user-lock text-emerald-600 ml-1"></i> تغيير كلمة سر الأونر</h4>
                    </div>
                    <form id="dedicatedPasswordForm" onsubmit="window.handleDedicatedPasswordChange(event)" class="space-y-3">
                        <div>
                            <label class="block text-xs font-bold text-navy-900 dark:text-slate-200 mb-1">كلمة السر الحالية للأونر *</label>
                            <input type="password" id="settingsCurrentPass" required placeholder="أدخل كلمة السر الحالية..." class="w-full bg-white border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm font-mono font-bold focus:outline-none">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-navy-900 dark:text-slate-200 mb-1">كلمة السر الجديدة (إنجليزي وأرقام ورموز) *</label>
                            <input type="password" id="settingsNewPass" required placeholder="أدخل كلمة السر الجديدة..." class="w-full bg-white border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm font-mono font-bold focus:outline-none">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-navy-900 dark:text-slate-200 mb-1">تأكيد كلمة السر الجديدة *</label>
                            <input type="password" id="settingsConfirmPass" required placeholder="أعد كتابة كلمة السر..." class="w-full bg-white border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm font-mono font-bold focus:outline-none">
                        </div>
                        <p id="settingsPassFeedback" class="text-xs font-bold hidden"></p>
                        <button type="submit" class="w-full bg-navy-900 text-white font-black py-3 rounded-xl text-sm shadow">حفظ كلمة سر الأونر الجديدة</button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- MANAGEMENT MODAL (Owner Panel) -->
    <div id="managementModal" class="fixed inset-0 z-50 hidden bg-navy-950/75 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-3xl max-w-4xl w-full shadow-2xl border border-slate-200 dark:border-slate-800 overflow-hidden my-8">
            <div class="bg-navy-900 text-white px-6 py-5 flex items-center justify-between">
                <h3 class="font-black text-lg"><i class="fa-solid fa-crown text-gold-400 ml-1"></i> لوحة تحكم الأونر - إعدادية سيد الأنام</h3>
                <button onclick="window.closeManagementModal()" class="w-9 h-9 rounded-xl bg-white/10 text-white"><i class="fa-solid fa-xmark"></i></button>
            </div>
            <div class="flex flex-wrap border-b border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 px-4 pt-3 gap-1">
                <button onclick="window.switchModalTab('teacher')" id="tabBtn-teacher" class="px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm border-b-2 border-navy-800 text-navy-900 dark:text-white bg-white dark:bg-slate-800">مدرس</button>
                <button onclick="window.switchModalTab('malzama')" id="tabBtn-malzama" class="px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm text-slate-600 dark:text-slate-400">ملزمة</button>
                <button onclick="window.switchModalTab('schedule')" id="tabBtn-schedule" class="px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm text-slate-600 dark:text-slate-400">الجدول الأسبوعي</button>
                <button onclick="window.switchModalTab('announcement')" id="tabBtn-announcement" class="px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm text-slate-600 dark:text-slate-400">تبليغ</button>
                <button onclick="window.switchModalTab('studentsLog')" id="tabBtn-studentsLog" class="px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm text-slate-600 dark:text-slate-400">سجل الطلاب</button>
            </div>
            <div class="p-6 max-h-[75vh] overflow-y-auto">
                <form id="form-teacher" onsubmit="window.handleSaveTeacher(event)" class="space-y-4">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">اسم الأستاذ الكامل *</label>
                            <input type="text" id="tName" required placeholder="مثال: أ. حيدر الموسوي" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">المادة الدراسية *</label>
                            <select id="tSubject" required class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                                <option value="التربية الإسلامية">التربية الإسلامية</option>
                                <option value="اللغة العربية">اللغة العربية</option>
                                <option value="اللغة الإنكليزية">اللغة الإنكليزية</option>
                                <option value="الرياضيات">الرياضيات</option>
                                <option value="الفيزياء">الفيزياء</option>
                                <option value="الكيمياء">الكيمياء</option>
                                <option value="الأحياء">الأحياء</option>
                                <option value="اللغة الكردية">اللغة الكردية</option>
                                <option value="جرائم حزب البعث">جرائم حزب البعث</option>
                                <option value="إدارة المدرسة">إدارة المدرسة</option>
                            </select>
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">المراحل الدراسية *</label>
                        <input type="text" id="tStages" required placeholder="مثال: السادس العلمي • الخامس العلمي" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">صورة الأستاذ (رفع ملف أو رابط)</label>
                        <input type="file" accept="image/*" onchange="window.handlePhotoUpload(event)" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl p-2 text-xs">
                        <input type="url" id="tPhotoUrl" placeholder="أو ضع رابط صورة مباشر..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2 text-xs mt-2">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">نبذة عن الأستاذ</label>
                        <textarea id="tBio" rows="2" placeholder="نبذة مختصرة..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl p-3 text-sm"></textarea>
                    </div>
                    <button type="submit" class="w-full bg-navy-900 text-white font-bold py-3 rounded-xl text-sm shadow">حفظ بيانات الأستاذ</button>
                </form>

                <form id="form-malzama" onsubmit="window.handleSaveMalzama(event)" class="space-y-4 hidden">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">عنوان الملزمة أو الملخص *</label>
                        <input type="text" id="mTitle" required placeholder="مثال: الملزمة الشاملة في الفيزياء الفصل الأول" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">اسم الأستاذ *</label>
                            <input type="text" id="mTeacher" required placeholder="مثال: أ. حيدر الموسوي" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">المادة الدراسية *</label>
                            <select id="mSubject" required class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                                <option value="الفيزياء">الفيزياء</option>
                                <option value="اللغة العربية">اللغة العربية</option>
                                <option value="اللغة الإنكليزية">اللغة الإنكليزية</option>
                                <option value="الرياضيات">الرياضيات</option>
                                <option value="الكيمياء">الكيمياء</option>
                                <option value="الأحياء">الأحياء</option>
                                <option value="اللغة الكردية">اللغة الكردية</option>
                                <option value="جرائم حزب البعث">جرائم حزب البعث</option>
                                <option value="التربية الإسلامية">التربية الإسلامية</option>
                            </select>
                        </div>
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">المرحلة الدراسية *</label>
                            <select id="mStage" required class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                                <option value="السادس الإعدادي">السادس الإعدادي</option>
                                <option value="الخامس الإعدادي">الخامس الإعدادي</option>
                                <option value="الرابع الإعدادي">الرابع الإعدادي</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">رابط التحميل (درايف / تليكرام) *</label>
                            <input type="url" id="mLink" required placeholder="https://t.me/..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                        </div>
                    </div>
                    <button type="submit" class="w-full bg-emerald-600 text-white font-bold py-3 rounded-xl text-sm shadow">رفع الملزمة ونشرها</button>
                </form>

                <form id="form-schedule" onsubmit="window.handleSaveSchedule(event)" class="space-y-4 hidden">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">عنوان الجدول (الصف والشعبة) *</label>
                        <input type="text" id="schTitle" required placeholder="مثال: جدول السادس العلمي - شعبة أ" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">الصف الدراسي *</label>
                            <select id="schClass" required class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                                <option value="السادس العلمي">السادس العلمي</option>
                                <option value="السادس الأدبي">السادس الأدبي</option>
                                <option value="الخامس الإعدادي">الخامس الإعدادي</option>
                                <option value="الرابع الإعدادي">الرابع الإعدادي</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">رابط صورة الجدول (أو درايف)</label>
                            <input type="url" id="schLink" placeholder="https://..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">تفاصيل الحصص والايام (أو ملاحظات الجدول) *</label>
                        <textarea id="schContent" required rows="3" placeholder="مثال: الأحد: رياضيات، فيزياء، إسلامية... الاثنين: كيمياء، عربي..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl p-3 text-sm"></textarea>
                    </div>
                    <button type="submit" class="w-full bg-sky-600 text-white font-bold py-3 rounded-xl text-sm shadow">نشر الجدول الأسبوعي</button>
                </form>

                <form id="form-announcement" onsubmit="window.handleSaveAnnouncement(event)" class="space-y-4 hidden">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">عنوان التبليغ *</label>
                        <input type="text" id="aTitle" required placeholder="مثال: جدول الامتحانات الشهرية" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">نوع التبليغ</label>
                        <select id="aBadge" class="w-full border border-slate-300 dark:border-slate-700 rounded-xl px-3.5 py-2.5 text-sm">
                            <option value="تبليغ هام">تبليغ هام</option>
                            <option value="جدول الامتحانات">جدول الامتحانات</option>
                            <option value="مكتبة الملازم">مكتبة الملازم</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-slate-700 dark:text-slate-300 mb-1">نص التبليغ *</label>
                        <textarea id="aContent" required rows="3" placeholder="تفاصيل التبليغ..." class="w-full border border-slate-300 dark:border-slate-700 rounded-xl p-3 text-sm"></textarea>
                    </div>
                    <button type="submit" class="w-full bg-amber-500 text-navy-950 font-bold py-3 rounded-xl text-sm shadow">نشر التبليغ رسمياً</button>
                </form>

                <div id="form-studentsLog" class="space-y-4 hidden">
                    <div class="flex flex-col sm:flex-row items-center justify-between gap-3">
                        <h4 class="font-bold text-navy-900 dark:text-white text-sm">سجل الطلاب المسجلين (<span id="totalStudentsCount">0</span>)</h4>
                        <div class="relative w-full sm:w-72">
                            <input type="text" id="studentLogSearchInput" oninput="window.renderStudentLogs()" placeholder="ابحث باسم الطالب أو الصف..." class="w-full bg-slate-50 border border-slate-300 dark:border-slate-700 rounded-xl pr-10 pl-4 py-2 text-xs focus:outline-none">
                            <i class="fa-solid fa-magnifying-glass absolute right-3.5 top-3 text-slate-400"></i>
                        </div>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-right text-xs">
                            <thead class="bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-200">
                                <tr>
                                    <th class="p-3">اسم الطالب الثلاثي</th>
                                    <th class="p-3">الصف</th>
                                    <th class="p-3">الشعبة</th>
                                    <th class="p-3">كلمة السر</th>
                                    <th class="p-3">وقت الإنشاء</th>
                                    <th class="p-3">إدارة</th>
                                </tr>
                            </thead>
                            <tbody id="studentLogsTableBody" class="divide-y divide-slate-200 dark:divide-slate-800"></tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast -->
    <div id="toast" class="fixed bottom-5 left-5 z-50 hidden bg-navy-900 text-white px-5 py-3.5 rounded-2xl shadow-2xl border border-slate-700 flex items-center gap-3">
        <i class="fa-solid fa-circle-check text-emerald-400 text-lg"></i>
        <span id="toastMessage" class="text-xs sm:text-sm font-bold">تم الحفظ بنجاح</span>
    </div>

    <!-- Main JavaScript Module -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, doc, setDoc, onSnapshot } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        let schoolData = {
            ownerPassword: "Nn6Tg0Bx2Iw76t",
            themeMode: "light",
            registeredStudents: [],
            teachers: [
                { id: "t1", name: "أ. حيدر الموسوي", subject: "الفيزياء", stages: "السادس العلمي • الخامس العلمي", bio: "مدرس مادة الفيزياء في إعدادية سيد الأنام.", photo: "" },
                { id: "t2", name: "أ. أحمد الخفاجي", subject: "اللغة العربية", stages: "السادس الإعدادي", bio: "مدرس قواعد اللغة العربية والأدب والنصوص.", photo: "" }
            ],
            malazim: [
                { id: "m1", title: "الملزمة الكاملة في الفيزياء - الجزء الأول", teacher: "أ. حيدر الموسوي", subject: "الفيزياء", stage: "السادس الإعدادي", link: "#malazim", notes: "شاملة للوزاريات" }
            ],
            schedules: [
                { id: "sch1", title: "جدول حصص السادس العلمي - شعبة أ", classGroup: "السادس العلمي", content: "الأحد: رياضيات، فيزياء، عربي • الاثنين: كيمياء، إنجليزي، أحياء • الثلاثاء: رياضيات، فيزياء، إسلامية • الأربعاء: عربي، كيمياء، إنجليزي • الخميس: أحياء، رياضيات، اجتماعيات", link: "#" }
            ],
            announcements: [
                { id: "a1", title: "ترحيب بطلبة إعدادية سيد الأنام للعام الدراسي الجديد", badge: "تبليغ هام", date: "إدارة المدرسة", content: "تُرحب إدارة وكادر إعدادية سيد الأنام بجميع طلبتنا الأعزاء." }
            ]
        };

        try {
            const savedPass = localStorage.getItem('sayyid_owner_password');
            if (savedPass) schoolData.ownerPassword = savedPass;
            const savedTheme = localStorage.getItem('sayyid_theme_mode');
            if (savedTheme) schoolData.themeMode = savedTheme;
            const savedStudents = localStorage.getItem('sayyid_registered_students');
            if (savedStudents) schoolData.registeredStudents = JSON.parse(savedStudents);
        } catch (e) {}

        let activeSession = null;
        try {
            const savedSession = localStorage.getItem('sayyid_active_session');
            if (savedSession) activeSession = JSON.parse(savedSession);
        } catch(e) {}

        let isAdminMode = false;
        if (activeSession && activeSession.role === 'owner') isAdminMode = true;

        let currentSubjectFilter = 'الكل';
        let currentStageFilter = 'الكل';
        let currentScheduleFilter = 'الكل';
        let currentUploadedPhotoBase64 = '';
        let db = null;
        let currentUser = null;
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'sayyid-al-anam-school';

        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // Theme UI
        window.applyThemeUI = function(mode) {
            const htmlEl = document.documentElement;
            const isDark = mode === 'dark';
            if (isDark) {
                htmlEl.classList.add('dark');
            } else {
                htmlEl.classList.remove('dark');
            }

            const loginIcon = document.getElementById('loginThemeIcon');
            const loginText = document.getElementById('loginThemeText');
            const topIcon = document.getElementById('topBarThemeIcon');
            const btnLight = document.getElementById('themeBtnLight');
            const btnDark = document.getElementById('themeBtnDark');

            if (loginIcon) loginIcon.className = isDark ? 'fa-solid fa-sun text-amber-400 text-sm' : 'fa-solid fa-moon text-gold-400 text-sm';
            if (loginText) loginText.textContent = isDark ? 'الوضع النهاري' : 'الوضع الليلي';
            if (topIcon) topIcon.className = isDark ? 'fa-solid fa-sun text-amber-400' : 'fa-solid fa-moon text-gold-400';

            if (btnLight && btnDark) {
                if (isDark) {
                    btnDark.className = 'p-3 rounded-xl border-2 border-gold-400 bg-slate-900 text-white font-bold text-xs flex items-center justify-center gap-2 transition';
                    btnLight.className = 'p-3 rounded-xl border border-slate-700 bg-slate-800 text-slate-300 font-bold text-xs flex items-center justify-center gap-2 transition';
                } else {
                    btnLight.className = 'p-3 rounded-xl border-2 border-navy-800 bg-white text-navy-900 font-bold text-xs flex items-center justify-center gap-2 transition';
                    btnDark.className = 'p-3 rounded-xl border border-slate-300 bg-slate-900 text-slate-700 font-bold text-xs flex items-center justify-center gap-2 transition';
                }
            }
        };

        window.setThemeMode = function(mode) {
            schoolData.themeMode = mode;
            try { localStorage.setItem('sayyid_theme_mode', mode); } catch (e) {}
            window.applyThemeUI(mode);
            window.showToast(mode === 'dark' ? 'تم تفعيل الوضع الليلي' : 'تم تفعيل الوضع النهاري');
            saveToCloud();
        };

        window.toggleTheme = function() {
            const newMode = schoolData.themeMode === 'dark' ? 'light' : 'dark';
            window.setThemeMode(newMode);
        };

        window.applyThemeUI(schoolData.themeMode);

        // Auth Tabs
        window.switchAuthTab = function(tab) {
            const regForm = document.getElementById('registerAccountForm');
            const loginForm = document.getElementById('loginAccountForm');
            const ownerForm = document.getElementById('ownerLoginForm');
            const tabReg = document.getElementById('authTabRegister');
            const tabLogin = document.getElementById('authTabLogin');
            const tabOwner = document.getElementById('authTabOwner');

            regForm.classList.add('hidden');
            loginForm.classList.add('hidden');
            ownerForm.classList.add('hidden');
            tabReg.className = 'py-2.5 rounded-xl text-xs font-bold text-slate-600 dark:text-slate-400 hover:text-navy-900 transition flex items-center justify-center gap-1';
            tabLogin.className = 'py-2.5 rounded-xl text-xs font-bold text-slate-600 dark:text-slate-400 hover:text-navy-900 transition flex items-center justify-center gap-1';
            tabOwner.className = 'py-2.5 rounded-xl text-xs font-bold text-slate-600 dark:text-slate-400 hover:text-navy-900 transition flex items-center justify-center gap-1';

            if (tab === 'register') {
                regForm.classList.remove('hidden');
                tabReg.className = 'py-2.5 rounded-xl text-xs font-black transition flex items-center justify-center gap-1 bg-navy-900 text-white shadow';
            } else if (tab === 'login') {
                loginForm.classList.remove('hidden');
                tabLogin.className = 'py-2.5 rounded-xl text-xs font-black transition flex items-center justify-center gap-1 bg-navy-900 text-white shadow';
            } else {
                ownerForm.classList.remove('hidden');
                tabOwner.className = 'py-2.5 rounded-xl text-xs font-black transition flex items-center justify-center gap-1 bg-amber-500 text-navy-950 shadow';
            }
        };

        window.fillDefaultOwnerPassword = function() {
            const input = document.getElementById('loginOwnerPassword');
            input.value = schoolData.ownerPassword || 'Nn6Tg0Bx2Iw76t';
            input.type = 'text';
            window.showToast('تم إدراج كلمة سر الأونر');
        };

        // Register Account with English/Symbols/Numbers validation only
        window.handleRegisterAccount = async function(e) {
            e.preventDefault();
            const name = document.getElementById('regName').value.trim();
            const grade = document.getElementById('regGrade').value;
            const section = document.getElementById('regSection').value;
            const password = document.getElementById('regPassword').value.trim();

            if (!name || !grade || !section || !password) return;

            // Check if password contains Arabic characters
            const arabicRegex = /[\u0600-\u06FF]/;
            if (arabicRegex.test(password)) {
                window.showToast('خطأ: يجب أن تكون كلمة المرور باللغة الإنجليزية، الأرقام أو الرموز فقط بدون أحرف عربية!');
                return;
            }

            const existing = schoolData.registeredStudents.find(s => s.name.toLowerCase() === name.toLowerCase());
            if (existing) {
                window.showToast('هذا الاسم مسجل مسبقاً! يرجى تسجيل الدخول مباشرة.');
                window.switchAuthTab('login');
                document.getElementById('loginStudentName').value = name;
                return;
            }

            const nowStr = new Date().toLocaleString('ar-IQ', { month: 'short', day: 'numeric', hour: '2-digit', minute: '2-digit' });
            const newStudent = { id: 'st_' + Date.now(), name, grade, section, password, time: nowStr };

            schoolData.registeredStudents.unshift(newStudent);
            try { localStorage.setItem('sayyid_registered_students', JSON.stringify(schoolData.registeredStudents)); } catch(e){}

            activeSession = { role: 'student', name, grade, section };
            isAdminMode = false;
            try { localStorage.setItem('sayyid_active_session', JSON.stringify(activeSession)); } catch(e){}

            applySessionPermissions();
            document.getElementById('loginGateOverlay').classList.add('hidden');
            window.showToast(`تم إنشاء حسابك بنجاح وأهلاً بك يا (${name})!`);
            await saveToCloud();
        };

        // Student Login
        window.handleStudentLogin = function(e) {
            e.preventDefault();
            const name = document.getElementById('loginStudentName').value.trim();
            const password = document.getElementById('loginStudentPassword').value.trim();
            const errEl = document.getElementById('studentLoginError');

            const student = schoolData.registeredStudents.find(s => s.name.toLowerCase() === name.toLowerCase() && s.password === password);
            if (student) {
                errEl.classList.add('hidden');
                activeSession = { role: 'student', name: student.name, grade: student.grade, section: student.section };
                isAdminMode = false;
                try { localStorage.setItem('sayyid_active_session', JSON.stringify(activeSession)); } catch(e){}
                applySessionPermissions();
                document.getElementById('loginGateOverlay').classList.add('hidden');
                window.showToast(`مرحباً عودتك يا (${student.name})`);
            } else {
                errEl.classList.remove('hidden');
            }
        };

        // Owner Login
        window.handleOwnerLogin = function(e) {
            e.preventDefault();
            const enteredPass = document.getElementById('loginOwnerPassword').value.trim();
            const validPass = schoolData.ownerPassword || 'Nn6Tg0Bx2Iw76t';
            const errEl = document.getElementById('ownerLoginError');

            if (enteredPass === validPass) {
                errEl.classList.add('hidden');
                activeSession = { role: 'owner', name: 'الأونر (مدير الموقع)', grade: 'الإدارة', section: '' };
                isAdminMode = true;
                try { localStorage.setItem('sayyid_active_session', JSON.stringify(activeSession)); } catch(e){}
                applySessionPermissions();
                document.getElementById('loginGateOverlay').classList.add('hidden');
                window.showToast('مرحباً بك يا أونر الموقع بصلاحيات كاملة!');
                renderAll();
            } else {
                errEl.classList.remove('hidden');
            }
        };

        window.handleLogout = function() {
            activeSession = null;
            isAdminMode = false;
            try { localStorage.removeItem('sayyid_active_session'); } catch(e){}
            document.getElementById('loginGateOverlay').classList.remove('hidden');
            window.switchAuthTab('register');
        };

        function applySessionPermissions() {
            const badge = document.getElementById('userRoleBadge');
            const info = document.getElementById('loggedInUserInfo');
            const ownerEls = document.querySelectorAll('.owner-only');
            const gate = document.getElementById('loginGateOverlay');

            if (activeSession) {
                gate.classList.add('hidden');
            } else {
                gate.classList.remove('hidden');
                return;
            }

            if (isAdminMode) {
                badge.className = 'bg-amber-500 text-navy-950 font-black px-2.5 py-0.5 rounded-md text-xs';
                badge.innerHTML = '<i class="fa-solid fa-crown"></i> أونر الموقع';
                info.textContent = `مرحباً بك يا مدير الموقع`;
                ownerEls.forEach(el => el.classList.remove('hidden'));
            } else if (activeSession && activeSession.role === 'student') {
                badge.className = 'bg-emerald-500 text-navy-950 font-black px-2.5 py-0.5 rounded-md text-xs';
                badge.innerHTML = '<i class="fa-solid fa-user-graduate"></i> طالب مسجل';
                info.textContent = `${activeSession.name} • ${activeSession.grade} (${activeSession.section})`;
                ownerEls.forEach(el => el.classList.add('hidden'));
            }
            renderAll();
        }

        // Render Functions
        window.renderTeachers = function() {
            const grid = document.getElementById('teachersGrid');
            if (!grid) return;
            const q = (document.getElementById('teacherSearchInput')?.value || '').toLowerCase();

            const filtered = schoolData.teachers.filter(t => {
                const matchSub = currentSubjectFilter === 'الكل' || t.subject === currentSubjectFilter;
                const matchQ = t.name.toLowerCase().includes(q) || t.subject.toLowerCase().includes(q);
                return matchSub && matchQ;
            });

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="col-span-full py-12 text-center text-slate-500">لا توجد نتائج مطابقة لبحثك</div>`;
                return;
            }

            grid.innerHTML = filtered.map(t => `
                <div class="bg-white rounded-3xl p-6 shadow-sm border border-slate-200 dark:border-slate-800 card-hover flex flex-col justify-between">
                    <div>
                        <div class="flex items-center gap-4 mb-4">
                            <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-navy-800 to-navy-950 text-gold-400 font-black text-2xl flex items-center justify-center overflow-hidden shrink-0 shadow">
                                ${t.photo ? `<img src="${t.photo}" class="w-full h-full object-cover">` : `<i class="fa-solid fa-chalkboard-user"></i>`}
                            </div>
                            <div>
                                <h3 class="font-black text-navy-900 dark:text-white text-lg">${t.name}</h3>
                                <span class="inline-block bg-navy-50 dark:bg-slate-800 text-navy-800 dark:text-gold-400 text-xs font-bold px-2.5 py-0.5 rounded-full mt-1">${t.subject}</span>
                            </div>
                        </div>
                        <p class="text-xs text-slate-600 dark:text-slate-300 font-medium mb-3"><i class="fa-solid fa-graduation-cap text-gold-500 ml-1"></i> المراحل: ${t.stages || 'جميع المراحل'}</p>
                        <p class="text-xs text-slate-500 dark:text-slate-400 line-clamp-2 leading-relaxed mb-4">${t.bio || 'مدرس المادة في إعدادية سيد الأنام'}</p>
                    </div>
                    <div class="pt-4 border-t border-slate-100 dark:border-slate-800 flex items-center justify-between gap-2">
                        <button onclick="window.showTeacherMalazim('${t.name}')" class="flex-1 bg-navy-50 dark:bg-slate-800 hover:bg-navy-100 dark:hover:bg-slate-700 text-navy-900 dark:text-white text-xs font-bold py-2 rounded-xl transition">ملازم الأستاذ</button>
                        ${isAdminMode ? `<button onclick="window.deleteTeacher('${t.id}')" class="text-red-500 hover:text-red-700 p-2 text-xs"><i class="fa-solid fa-trash"></i></button>` : ''}
                    </div>
                </div>
            `).join('');
        };

        window.renderMalazim = function() {
            const grid = document.getElementById('malazimGrid');
            if (!grid) return;
            const q = (document.getElementById('malzamaSearchInput')?.value || '').toLowerCase();

            const filtered = schoolData.malazim.filter(m => {
                const matchStage = currentStageFilter === 'الكل' || m.stage === currentStageFilter;
                const matchQ = m.title.toLowerCase().includes(q) || m.teacher.toLowerCase().includes(q) || m.subject.toLowerCase().includes(q);
                return matchStage && matchQ;
            });

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="col-span-full py-12 text-center text-slate-500">لا توجد ملازم مطابقة لبحثك</div>`;
                return;
            }

            grid.innerHTML = filtered.map(m => `
                <div class="bg-white rounded-3xl p-6 shadow-sm border border-slate-200 dark:border-slate-800 card-hover flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <span class="bg-emerald-100 dark:bg-emerald-950/60 text-emerald-800 dark:text-emerald-300 text-[11px] font-bold px-3 py-1 rounded-full">${m.stage}</span>
                            <span class="text-xs font-bold text-slate-500 dark:text-slate-400">${m.subject}</span>
                        </div>
                        <h3 class="font-black text-navy-900 dark:text-white text-base mb-2 leading-snug">${m.title}</h3>
                        <p class="text-xs text-slate-600 dark:text-slate-300 font-semibold mb-3"><i class="fa-solid fa-chalkboard-user text-navy-800 dark:text-gold-400 ml-1"></i> الأستاذ: ${m.teacher}</p>
                        <p class="text-xs text-slate-500 dark:text-slate-400 bg-slate-50 dark:bg-slate-800 p-2.5 rounded-xl mb-4">${m.notes || 'ملزمة منهجية معتمدة'}</p>
                    </div>
                    <div class="pt-4 border-t border-slate-100 dark:border-slate-800 flex items-center justify-between gap-2">
                        <a href="${m.link}" target="_blank" class="flex-1 bg-emerald-600 hover:bg-emerald-700 text-white text-xs font-black py-2.5 px-4 rounded-xl text-center shadow transition flex items-center justify-center gap-1.5">
                            <i class="fa-solid fa-cloud-arrow-down"></i> تحميل أو عرض
                        </a>
                        ${isAdminMode ? `<button onclick="window.deleteMalzama('${m.id}')" class="text-red-500 hover:text-red-700 p-2"><i class="fa-solid fa-trash"></i></button>` : ''}
                    </div>
                </div>
            `).join('');
        };

        window.renderSchedule = function() {
            const grid = document.getElementById('scheduleGrid');
            if (!grid) return;

            const filtered = (schoolData.schedules || []).filter(sch => {
                return currentScheduleFilter === 'الكل' || sch.classGroup === currentScheduleFilter;
            });

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="col-span-full py-12 text-center text-slate-500 text-base font-bold">لا توجد جداول دراسية منشورة حالياً</div>`;
                return;
            }

            grid.innerHTML = filtered.map(sch => {
                let dayEntries = [];
                if (sch.content) {
                    dayEntries = sch.content.split('•').map(item => item.trim()).filter(Boolean);
                }

                return `
                <div class="bg-white dark:bg-slate-900 rounded-3xl p-6 sm:p-7 shadow-xl border border-slate-200 dark:border-slate-800 card-hover flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-5 pb-3 border-b border-slate-100 dark:border-slate-800">
                            <span class="bg-sky-100 dark:bg-sky-950/80 text-sky-800 dark:text-sky-300 text-sm font-black px-4 py-1.5 rounded-xl flex items-center gap-1.5">
                                <i class="fa-solid fa-graduation-cap"></i> ${sch.classGroup}
                            </span>
                            <span class="text-sm text-emerald-600 dark:text-emerald-400 font-bold bg-emerald-50 dark:bg-emerald-950/50 px-3.5 py-1.5 rounded-xl">
                                <i class="fa-solid fa-circle-check ml-1.5"></i> جدول معتمد رسمياً
                            </span>
                        </div>
                        
                        <h3 class="font-black text-navy-900 dark:text-white text-xl mb-5 flex items-center gap-2">
                            <i class="fa-solid fa-calendar-days text-sky-500 text-2xl"></i>
                            <span>${sch.title}</span>
                        </h3>

                        <!-- Styled Days Grid with larger readable fonts -->
                        <div class="space-y-3.5 mb-6">
                            ${dayEntries.length > 0 ? dayEntries.map(entry => {
                                const parts = entry.split(':');
                                const dayName = parts[0] || '';
                                const dayLessons = parts[1] || entry;
                                return `
                                <div class="bg-slate-50 dark:bg-slate-800/80 p-4 rounded-2xl border border-slate-100 dark:border-slate-700/60 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                                    <span class="font-black text-sky-700 dark:text-sky-400 text-base bg-sky-50 dark:bg-sky-950/60 px-4 py-2 rounded-xl w-fit shrink-0 flex items-center gap-2">
                                        <i class="fa-solid fa-sun text-amber-400"></i> ${dayName}
                                    </span>
                                    <span class="text-sm sm:text-base font-bold text-slate-800 dark:text-slate-100 leading-relaxed">${dayLessons}</span>
                                </div>`;
                            }).join('') : `<p class="text-base text-slate-700 dark:text-slate-200 bg-slate-50 dark:bg-slate-800 p-4 rounded-2xl leading-relaxed">${sch.content}</p>`}
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-100 dark:border-slate-800 flex items-center justify-between gap-3">
                        ${sch.link && sch.link !== '#' ? `
                            <a href="${sch.link}" target="_blank" class="flex-1 bg-gradient-to-l from-sky-600 to-sky-700 hover:from-sky-700 hover:to-sky-800 text-white text-sm font-black py-3.5 px-4 rounded-2xl text-center shadow-lg transition flex items-center justify-center gap-2">
                                <i class="fa-solid fa-image text-lg"></i>
                                <span>عرض صورة الجدول كاملة</span>
                            </a>` : ''}
                        ${isAdminMode ? `
                            <button onclick="window.deleteSchedule('${sch.id}')" class="bg-red-50 dark:bg-red-950/40 hover:bg-red-100 text-red-600 dark:text-red-400 px-4 py-3.5 rounded-2xl text-sm font-bold transition flex items-center gap-1.5 shrink-0">
                                <i class="fa-solid fa-trash"></i>
                                <span>حذف الجدول</span>
                            </button>` : ''}
                    </div>
                </div>
            `;
            }).join('');
        };

        window.renderAnnouncements = function() {
            const grid = document.getElementById('announcementsGrid');
            if (!grid) return;

            grid.innerHTML = schoolData.announcements.map(a => `
                <div class="bg-white rounded-3xl p-6 shadow-sm border border-slate-200 dark:border-slate-800 space-y-3">
                    <div class="flex items-center justify-between">
                        <span class="bg-amber-100 dark:bg-amber-950/60 text-amber-900 dark:text-amber-300 text-xs font-bold px-3 py-1 rounded-full">${a.badge}</span>
                        <span class="text-xs text-slate-400 font-medium">${a.date}</span>
                    </div>
                    <h3 class="font-black text-navy-900 dark:text-white text-lg">${a.title}</h3>
                    <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-300 leading-relaxed">${a.content}</p>
                    ${isAdminMode ? `<div class="pt-2 text-left"><button onclick="window.deleteAnnouncement('${a.id}')" class="text-red-500 text-xs font-bold"><i class="fa-solid fa-trash"></i> حذف التبليغ</button></div>` : ''}
                </div>
            `).join('');
        };

        window.renderStudentLogs = function() {
            const tbody = document.getElementById('studentLogsTableBody');
            const countEl = document.getElementById('totalStudentsCount');
            const navCount = document.getElementById('navStudentLogCount');
            const searchInput = document.getElementById('studentLogSearchInput');
            if (!tbody) return;

            const query = (searchInput?.value || '').toLowerCase();
            const list = (schoolData.registeredStudents || []).filter(s => {
                return s.name.toLowerCase().includes(query) || s.grade.toLowerCase().includes(query) || s.section.toLowerCase().includes(query);
            });

            if (countEl) countEl.textContent = (schoolData.registeredStudents || []).length;
            if (navCount) navCount.textContent = (schoolData.registeredStudents || []).length;

            if (list.length === 0) {
                tbody.innerHTML = `<tr><td colspan="6" class="p-6 text-center text-slate-400">لا توجد نتائج مطابقة لبحثك في سجل الطلاب</td></tr>`;
                return;
            }

            tbody.innerHTML = list.map(s => `
                <tr>
                    <td class="p-3 font-bold text-navy-900 dark:text-white">${s.name}</td>
                    <td class="p-3 dark:text-slate-300">${s.grade}</td>
                    <td class="p-3 dark:text-slate-300">شعبة (${s.section})</td>
                    <td class="p-3 font-mono font-bold text-amber-600 dark:text-amber-400">${s.password}</td>
                    <td class="p-3 text-slate-500">${s.time}</td>
                    <td class="p-3"><button onclick="window.deleteStudent('${s.id}')" class="text-red-500 hover:text-red-700"><i class="fa-solid fa-trash"></i></button></td>
                </tr>
            `).join('');
        };

        window.renderAll = function() {
            window.renderTeachers();
            window.renderMalazim();
            window.renderSchedule();
            window.renderAnnouncements();
            window.renderStudentLogs();
            document.getElementById('statTeachers').textContent = schoolData.teachers.length;
            document.getElementById('statMalazim').textContent = schoolData.malazim.length;
            document.getElementById('statSchedules').textContent = (schoolData.schedules || []).length;
            document.getElementById('statAnnouncements').textContent = schoolData.announcements.length;
        };

        // Filter triggers
        window.filterTeachersBySubject = function(sub) {
            currentSubjectFilter = sub;
            document.querySelectorAll('.subject-btn').forEach(btn => {
                btn.className = btn.dataset.subject === sub ? 'subject-btn bg-navy-800 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0' : 'subject-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shrink-0';
            });
            window.renderTeachers();
        };

        window.filterMalazimByStage = function(stage) {
            currentStageFilter = stage;
            document.querySelectorAll('.stage-btn').forEach(btn => {
                btn.className = btn.dataset.stage === stage ? 'stage-btn bg-emerald-600 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold' : 'stage-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold';
            });
            window.renderMalazim();
        };

        window.filterScheduleByClass = function(cls) {
            currentScheduleFilter = cls;
            document.querySelectorAll('.schedule-btn').forEach(btn => {
                btn.className = btn.dataset.class === cls ? 'schedule-btn bg-sky-600 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold' : 'schedule-btn bg-slate-100 dark:bg-slate-800 text-slate-700 dark:text-slate-300 px-4 py-2 rounded-xl text-xs sm:text-sm font-bold';
            });
            window.renderSchedule();
        };

        window.showTeacherMalazim = function(teacherName) {
            document.getElementById('malzamaSearchInput').value = teacherName;
            window.filterMalazimByStage('الكل');
            document.getElementById('malazim').scrollIntoView({ behavior: 'smooth' });
            window.renderMalazim();
        };

        // Modal Controls
        window.openAddModal = function(tab = 'teacher') {
            if (!isAdminMode) return;
            document.getElementById('managementModal').classList.remove('hidden');
            window.switchModalTab(tab);
        };
        window.closeManagementModal = function() {
            document.getElementById('managementModal').classList.add('hidden');
        };

        window.openSettingsModal = function() {
            const ownerPasswordSection = document.getElementById('ownerPasswordSettingsSection');
            if (isAdminMode) {
                ownerPasswordSection.classList.remove('hidden');
            } else {
                ownerPasswordSection.classList.add('hidden');
            }
            document.getElementById('settingsModal').classList.remove('hidden');
        };

        window.closeSettingsModal = function() {
            document.getElementById('settingsModal').classList.add('hidden');
        };

        window.switchModalTab = function(tab) {
            ['teacher', 'malzama', 'schedule', 'announcement', 'studentsLog'].forEach(t => {
                const form = document.getElementById(`form-${t}`);
                const btn = document.getElementById(`tabBtn-${t}`);
                if (!form || !btn) return;
                if (t === tab) {
                    form.classList.remove('hidden');
                    btn.className = 'px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm border-b-2 border-navy-800 text-navy-900 dark:text-white bg-white dark:bg-slate-800';
                } else {
                    form.classList.add('hidden');
                    btn.className = 'px-3.5 py-2.5 rounded-t-xl font-bold text-xs sm:text-sm text-slate-600 dark:text-slate-400';
                }
            });
            if (tab === 'studentsLog') window.renderStudentLogs();
        };

        // Photo Upload
        window.handlePhotoUpload = function(e) {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = function(evt) {
                currentUploadedPhotoBase64 = evt.target.result;
            };
            reader.readAsDataURL(file);
        };

        window.handleSaveTeacher = async function(e) {
            e.preventDefault();
            const name = document.getElementById('tName').value.trim();
            const subject = document.getElementById('tSubject').value;
            const stages = document.getElementById('tStages').value.trim();
            const bio = document.getElementById('tBio').value.trim();
            const urlPhoto = document.getElementById('tPhotoUrl').value.trim();
            const photo = currentUploadedPhotoBase64 || urlPhoto;

            schoolData.teachers.unshift({ id: 't_' + Date.now(), name, subject, stages, bio, photo });
            document.getElementById('form-teacher').reset();
            currentUploadedPhotoBase64 = '';
            window.closeManagementModal();
            window.showToast('تمت إضافة الأستاذ بنجاح');
            await saveToCloud();
        };

        window.deleteTeacher = async function(id) {
            schoolData.teachers = schoolData.teachers.filter(t => t.id !== id);
            window.showToast('تم حذف الأستاذ');
            await saveToCloud();
        };

        window.handleSaveMalzama = async function(e) {
            e.preventDefault();
            const title = document.getElementById('mTitle').value.trim();
            const teacher = document.getElementById('mTeacher').value.trim();
            const subject = document.getElementById('mSubject').value;
            const stage = document.getElementById('mStage').value;
            const link = document.getElementById('mLink').value.trim();

            schoolData.malazim.unshift({ id: 'm_' + Date.now(), title, teacher, subject, stage, link });
            document.getElementById('form-malzama').reset();
            window.closeManagementModal();
            window.showToast('تمت إضافة الملزمة بنجاح');
            await saveToCloud();
        };

        window.deleteMalzama = async function(id) {
            schoolData.malazim = schoolData.malazim.filter(m => m.id !== id);
            window.showToast('تم حذف الملزمة');
            await saveToCloud();
        };

        window.handleSaveSchedule = async function(e) {
            e.preventDefault();
            const title = document.getElementById('schTitle').value.trim();
            const classGroup = document.getElementById('schClass').value;
            const link = document.getElementById('schLink').value.trim();
            const content = document.getElementById('schContent').value.trim();

            if (!schoolData.schedules) schoolData.schedules = [];
            schoolData.schedules.unshift({ id: 'sch_' + Date.now(), title, classGroup, link, content });
            document.getElementById('form-schedule').reset();
            window.closeManagementModal();
            window.showToast('تم نشر الجدول الأسبوعي بنجاح');
            await saveToCloud();
        };

        window.deleteSchedule = async function(id) {
            schoolData.schedules = (schoolData.schedules || []).filter(sch => sch.id !== id);
            window.showToast('تم حذف الجدول');
            await saveToCloud();
        };

        window.handleSaveAnnouncement = async function(e) {
            e.preventDefault();
            const title = document.getElementById('aTitle').value.trim();
            const badge = document.getElementById('aBadge').value;
            const content = document.getElementById('aContent').value.trim();

            schoolData.announcements.unshift({ id: 'a_' + Date.now(), title, badge, content, date: 'اليوم' });
            document.getElementById('form-announcement').reset();
            window.closeManagementModal();
            window.showToast('تم نشر التبليغ بنجاح');
            await saveToCloud();
        };

        window.deleteAnnouncement = async function(id) {
            schoolData.announcements = schoolData.announcements.filter(a => a.id !== id);
            window.showToast('تم حذف التبليغ');
            await saveToCloud();
        };

        window.deleteStudent = async function(id) {
            schoolData.registeredStudents = schoolData.registeredStudents.filter(s => s.id !== id);
            try { localStorage.setItem('sayyid_registered_students', JSON.stringify(schoolData.registeredStudents)); } catch(e){}
            window.renderStudentLogs();
            window.showToast('تم حذف الحساب');
            await saveToCloud();
        };

        // Owner Password Change
        window.handleDedicatedPasswordChange = async function(e) {
            e.preventDefault();
            if (!isAdminMode) return;
            const currentEntered = document.getElementById('settingsCurrentPass').value.trim();
            const newPass = document.getElementById('settingsNewPass').value.trim();
            const confirmPass = document.getElementById('settingsConfirmPass').value.trim();
            const feedback = document.getElementById('settingsPassFeedback');
            feedback.classList.remove('hidden');

            const arabicRegex = /[\u0600-\u06FF]/;
            if (arabicRegex.test(newPass)) {
                feedback.className = 'text-xs font-bold text-red-600 block';
                feedback.textContent = 'كلمة السر الجديدة يجب أن تكون باللغة الإنجليزية والأرقام والرموز فقط!';
                return;
            }

            const validCurrent = schoolData.ownerPassword || 'Nn6Tg0Bx2Iw76t';
            if (currentEntered !== validCurrent) {
                feedback.className = 'text-xs font-bold text-red-600 block';
                feedback.textContent = 'كلمة السر الحالية للأونر غير صحيحة!';
                return;
            }
            if (newPass.length < 4) {
                feedback.className = 'text-xs font-bold text-red-600 block';
                feedback.textContent = 'يجب ألا تقل كلمة السر الجديدة عن 4 أحرف أو أرقام.';
                return;
            }
            if (newPass !== confirmPass) {
                feedback.className = 'text-xs font-bold text-red-600 block';
                feedback.textContent = 'كلمة السر الجديدة وتأكيدها غير متطابقين!';
                return;
            }

            schoolData.ownerPassword = newPass;
            try { localStorage.setItem('sayyid_owner_password', newPass); } catch(e){}
            feedback.className = 'text-xs font-bold text-emerald-600 block';
            feedback.textContent = `تم حفظ كلمة سر الأونر الجديدة بنجاح!`;
            window.showToast('تم تحديث كلمة سر الأونر بنجاح');
            document.getElementById('dedicatedPasswordForm').reset();
            await saveToCloud();
        };

        window.showToast = function(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMessage').textContent = msg;
            toast.classList.remove('hidden');
            setTimeout(() => { toast.classList.add('hidden'); }, 4000);
        };

        async function initCloudSync() {
            try {
                if (typeof __firebase_config !== 'undefined' && __firebase_config) {
                    const firebaseConfig = JSON.parse(__firebase_config);
                    const app = initializeApp(firebaseConfig);
                    const auth = getAuth(app);
                    db = getFirestore(app);

                    if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
                        await signInWithCustomToken(auth, __initial_auth_token);
                    } else {
                        await signInAnonymously(auth);
                    }
                    currentUser = auth.currentUser;

                    if (currentUser) {
                        const ref = doc(db, 'artifacts', appId, 'public', 'data', 'school_portal', 'main_data');
                        onSnapshot(ref, (snap) => {
                            if (snap.exists()) {
                                const d = snap.data();
                                if (d.teachers) schoolData.teachers = JSON.parse(d.teachers);
                                if (d.malazim) schoolData.malazim = JSON.parse(d.malazim);
                                if (d.schedules) schoolData.schedules = JSON.parse(d.schedules);
                                if (d.announcements) schoolData.announcements = JSON.parse(d.announcements);
                                if (d.registeredStudents) {
                                    schoolData.registeredStudents = JSON.parse(d.registeredStudents);
                                    try { localStorage.setItem('sayyid_registered_students', d.registeredStudents); } catch(e){}
                                }
                                if (d.ownerPassword) schoolData.ownerPassword = d.ownerPassword;
                                if (d.themeMode) window.applyThemeUI(d.themeMode);
                                window.renderAll();
                            }
                        }, (error) => {});
                    }
                }
            } catch (e) {}
        }

        async function saveToCloud() {
            window.renderAll();
            try { localStorage.setItem('sayyid_registered_students', JSON.stringify(schoolData.registeredStudents)); } catch(e){}
            if (!db || !currentUser) return;
            try {
                const ref = doc(db, 'artifacts', appId, 'public', 'data', 'school_portal', 'main_data');
                await setDoc(ref, {
                    teachers: JSON.stringify(schoolData.teachers),
                    malazim: JSON.stringify(schoolData.malazim),
                    schedules: JSON.stringify(schoolData.schedules || []),
                    announcements: JSON.stringify(schoolData.announcements),
                    registeredStudents: JSON.stringify(schoolData.registeredStudents),
                    ownerPassword: schoolData.ownerPassword,
                    themeMode: schoolData.themeMode,
                    updatedAt: Date.now()
                });
            } catch(e) {}
        }

        applySessionPermissions();
        window.renderAll();
        initCloudSync();
    </script>
</body>
</html>
