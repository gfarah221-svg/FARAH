# FARAH
.....
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة التاريخ الرقمية - الصف الأول الثانوي</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts (Amiri & Cairo) -->
    <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@700&family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        pharaoh: {
                            navy: '#0B132B',
                            gold: '#D4AF37',
                            lightGold: '#F3E5AB',
                            darkGold: '#AA7C11',
                            cardBg: '#1C2541'
                        }
                    },
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                        amiri: ['Amiri', 'serif']
                    }
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Cairo', sans-serif; }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col selection:bg-pharaoh-gold selection:text-pharaoh-navy">

    <!-- Top Announcement Bar -->
    <div class="bg-gradient-to-r from-pharaoh-navy via-slate-900 to-pharaoh-navy border-b border-pharaoh-gold/20 py-2.5 px-4 text-xs sm:text-sm font-medium flex justify-between items-center max-w-7xl mx-auto w-full">
        <div class="flex items-center gap-2 text-pharaoh-lightGold">
            <span class="px-2 py-0.5 rounded bg-pharaoh-gold/20 border border-pharaoh-gold/40 font-bold text-xs">إصدار 2027</span>
            <span class="font-semibold">تحديثات وزارة التربية والتعليم ونواتج التعلم الحديثة</span>
        </div>
        <div class="hidden md:flex items-center gap-4 text-slate-300">
            <span><i class="fa-solid fa-graduation-cap text-pharaoh-gold ml-1"></i> العام الدراسي 2026 / 2027</span>
            <span><i class="fa-solid fa-book-open-reader text-pharaoh-gold ml-1"></i> تاريخ الصف الأول الثانوي</span>
        </div>
    </div>

    <!-- Main Navigation Bar -->
    <header class="sticky top-0 z-40 bg-pharaoh-navy/95 backdrop-blur-md border-b border-pharaoh-gold/30 shadow-xl">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Brand Logo -->
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-pharaoh-darkGold via-pharaoh-gold to-yellow-200 flex items-center justify-center shadow-lg shadow-pharaoh-gold/20 text-pharaoh-navy text-2xl font-black">
                    <i class="fa-solid fa-ankh"></i>
                </div>
                <div>
                    <h1 class="text-xl md:text-2xl font-black tracking-wide text-transparent bg-clip-text bg-gradient-to-r from-pharaoh-lightGold via-yellow-200 to-amber-300 font-amiri">
                        مَنَصَّة التَّاريخ الرَّقْمِيَّة
                    </h1>
                    <p class="text-xs text-slate-400 flex items-center gap-1 font-semibold">
                        <span>الصف الأول الثانوي</span>
                        <span class="text-pharaoh-gold">•</span>
                        <span>فهم • استنتاج • ربط</span>
                    </p>
                </div>
            </div>

            <!-- Gamification & Progress Stats -->
            <div class="hidden lg:flex items-center gap-4 bg-slate-900/80 px-4 py-2 rounded-2xl border border-pharaoh-gold/20">
                <div class="flex items-center gap-2">
                    <div class="w-8 h-8 rounded-full bg-amber-500/10 text-pharaoh-gold flex items-center justify-center font-bold">
                        <i class="fa-solid fa-trophy text-sm"></i>
                    </div>
                    <div>
                        <div class="text-[10px] text-slate-400">نقاط المعرفة</div>
                        <div id="statPoints" class="text-sm font-black text-amber-300">0 نقطة</div>
                    </div>
                </div>
                <div class="h-6 w-px bg-slate-700"></div>
                <div class="flex items-center gap-2">
                    <div class="w-8 h-8 rounded-full bg-purple-500/10 text-purple-400 flex items-center justify-center font-bold">
                        <i class="fa-solid fa-medal text-sm"></i>
                    </div>
                    <div>
                        <div class="text-[10px] text-slate-400">المستوى</div>
                        <div id="statLevel" class="text-sm font-black text-purple-300">مؤرخ مبتدئ</div>
                    </div>
                </div>
            </div>

            <!-- Navigation Tabs -->
            <nav class="flex items-center gap-1 sm:gap-2">
                <button onclick="switchTab('curriculum')" id="tabBtn-curriculum" class="tab-btn px-
