<!DOCTYPE html>
<html lang="zh-TW" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>護理系一年級甲班 - 官方班網</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome 圖示庫 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Canvas Confetti Library for Winner Effects -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        nursing: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            400: '#38bdf8',
                            500: '#0284c7',
                            600: '#0369a1',
                            700: '#0f766e',
                            800: '#115e59',
                        }
                    },
                    animation: {
                        'bounce-short': 'bounce 0.5s ease-in-out 2',
                        'pulse-fast': 'pulse 0.5s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    }
                }
            }
        }
    </script>
    <style>
        .gradient-border {
            background: linear-gradient(135deg, #0284c7, #0f766e);
        }
        /* Custom scrollbar for student roster textarea */
        textarea::-webkit-scrollbar {
            width: 8px;
        }
        textarea::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 4px;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 flex flex-col min-h-screen font-sans">

    <!-- 1. 頂部導覽列 (Navbar) -->
    <nav class="bg-white/95 backdrop-blur shadow-md sticky top-0 z-40 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <!-- 左上方 Logo：點擊可返回首頁 (href="#top") -->
                <a href="#top" class="flex items-center space-x-3 group cursor-pointer" title="返回首頁">
                    <div class="w-10 h-10 rounded-full bg-nursing-500 text-white flex items-center justify-center shadow-md group-hover:bg-nursing-600 transition">
                        <i class="fa-solid fa-user-nurse text-xl"></i>
                    </div>
                    <div class="flex flex-col">
                        <span class="font-bold text-xl text-slate-800 group-hover:text-nursing-600 transition tracking-wide">護一甲 官方班網</span>
                        <span class="text-xs text-teal-600 font-medium">Department of Nursing</span>
                    </div>
                </a>

                <!-- 導覽選單 (桌面版) -->
                <div class="hidden lg:flex items-center space-x-5 font-medium text-sm">
                    <a href="#about" class="text-slate-600 hover:text-nursing-500 transition py-2 border-b-2 border-transparent hover:border-nursing-500">班級簡介</a>
                    <a href="#schedule" class="text-slate-600 hover:text-nursing-500 transition py-2 border-b-2 border-transparent hover:border-nursing-500">班級課表</a>
                    <a href="#students" class="text-slate-600 hover:text-nursing-500 transition py-2 border-b-2 border-transparent hover:border-nursing-500">同學介紹</a>
                    <a href="#random-picker" class="text-teal-700 font-bold hover:text-teal-900 transition py-1.5 px-3 bg-teal-50 hover:bg-teal-100 rounded-lg border border-teal-200">
                        <i class="fa-solid fa-dice text-teal-600 mr-1"></i>隨機抽籤
                    </a>
                    <a href="#poll" class="text-slate-600 hover:text-nursing-500 transition py-2 border-b-2 border-transparent hover:border-nursing-500">班級投票</a>
                    <a href="#events" class="text-slate-600 hover:text-nursing-500 transition py-2 border-b-2 border-transparent hover:border-nursing-500">活動花絮</a>
                </div>

                <!-- 手機版選單按鈕 -->
                <div class="lg:hidden flex items-center">
                    <button id="mobileMenuBtn" type="button" class="text-slate-600 hover:text-nursing-500 p-2 focus:outline-none" aria-label="開啟選單">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- 手機版下拉選單 -->
        <div id="mobileMenu" class="hidden lg:hidden bg-white border-b border-slate-200 px-4 pt-2 pb-4 space-y-2">
            <a href="#top" class="block py-2 text-nursing-600 font-bold border-b border-slate-100"><i class="fa-solid fa-house mr-2"></i>返回首頁頂部</a>
            <a href="#about" class="block py-2 text-slate-700 hover:text-nursing-500 font-medium">班級簡介</a>
            <a href="#schedule" class="block py-2 text-slate-700 hover:text-nursing-500 font-medium">班級課表</a>
            <a href="#students" class="block py-2 text-slate-700 hover:text-nursing-500 font-medium">同學介紹</a>
            <a href="#random-picker" class="block py-2 text-teal-700 font-bold bg-teal-50 px-2 rounded"><i class="fa-solid fa-dice mr-2"></i>隨機抽籤功能</a>
            <a href="#poll" class="block py-2 text-slate-700 hover:text-nursing-500 font-medium">班級投票</a>
            <a href="#events" class="block py-2 text-slate-700 hover:text-nursing-500 font-medium">活動花絮</a>
        </div>
    </nav>

    <!-- 2. Hero 橫幅區域 (#top) -->
    <header id="top" class="relative bg-gradient-to-r from-teal-700 via-teal-600 to-nursing-600 text-white py-20 px-4 overflow-hidden">
        <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:16px_16px]"></div>
        <div class="max-w-4xl mx-auto text-center relative z-10">
            <span class="bg-white/20 text-white text-sm font-semibold px-4 py-1.5 rounded-full inline-block mb-4 backdrop-blur-sm border border-white/30">
                <i class="fa-solid fa-heart-pulse mr-1"></i> 護理系一年級甲班
            </span>
            <h1 class="text-4xl md:text-5xl font-extrabold mb-4 tracking-tight leading-tight">用心守護生命，用愛關懷世界</h1>
            <p class="text-lg md:text-xl text-teal-50 mb-8 max-w-2xl mx-auto font-light leading-relaxed">
                歡迎來到護一甲的溫馨園地！這裡是我們學習白衣天使專業知識、記錄青春歡笑與共同成長的專屬天地。
            </p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#schedule" class="bg-white text-nursing-600 font-bold px-6 py-3 rounded-xl shadow-lg hover:bg-slate-100 transform hover:-translate-y-0.5 transition duration-200">
                    <i class="fa-solid fa-calendar-week mr-2"></i>查看班級課表
                </a>
                <a href="#random-picker" class="bg-amber-400 hover:bg-amber-300 text-slate-900 font-bold px-6 py-3 rounded-xl shadow-lg transform hover:-translate-y-0.5 transition duration-200">
                    <i class="fa-solid fa-dice mr-2"></i>課堂隨機抽籤
                </a>
                <a href="#poll" class="bg-teal-800/80 hover:bg-teal-900 text-white font-bold px-6 py-3 rounded-xl shadow-lg border border-white/20 transform hover:-translate-y-0.5 transition duration-200 backdrop-blur-sm">
                    <i class="fa-solid fa-vote-yea mr-2"></i>參與最新投票
                </a>
            </div>
        </div>
    </header>

    <!-- 主體內容容器 -->
    <main id="about" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 space-y-24 flex-grow">

        <!-- 3. 班級課表區塊 (#schedule) -->
        <section id="schedule" class="scroll-mt-24">
            <div class="flex items-center justify-between mb-6">
                <div class="flex items-center space-x-3">
                    <div class="p-3 bg-nursing-100 text-nursing-600 rounded-xl">
                        <i class="fa-solid fa-calendar-days text-2xl"></i>
                    </div>
                    <div>
                        <h2 class="text-2xl font-bold text-slate-800">114學年度 第一學期課表</h2>
                        <p class="text-sm text-slate-500">請注意解剖學實驗與護理學導論之教室更換通知</p>
                    </div>
                </div>
            </div>

            <div class="bg-white shadow-lg rounded-2xl overflow-hidden border border-slate-200/80">
                <div class="overflow-x-auto">
                    <table class="w-full text-center border-collapse min-w-[700px]">
                        <thead>
                            <tr class="bg-nursing-600 text-white font-semibold">
                                <th class="p-4 border-r border-nursing-500 w-32">節次 / 時間</th>
                                <th class="p-4 border-r border-nursing-500">星期一</th>
                                <th class="p-4 border-r border-nursing-500">星期二</th>
                                <th class="p-4 border-r border-nursing-500">星期三</th>
                                <th class="p-4 border-r border-nursing-500">星期四</th>
                                <th class="p-4">星期五</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-slate-200 text-sm md:text-base">
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 1 節<br><span class="text-xs text-slate-500 font-normal">08:10 - 09:00</span></td>
                                <td rowspan="2" class="p-3 bg-sky-50/80 text-sky-800 font-medium rounded-lg border border-sky-100">
                                    <span class="block font-bold">解剖學</span>
                                    <span class="text-xs text-sky-600"><i class="fa-solid fa-location-dot"></i> 醫學大樓 301</span>
                                </td>
                                <td class="p-3 text-slate-700">普通心理學</td>
                                <td rowspan="2" class="p-3 bg-teal-50/80 text-teal-800 font-medium rounded-lg border border-teal-100">
                                    <span class="block font-bold">護理學導論</span>
                                    <span class="text-xs text-teal-600"><i class="fa-solid fa-location-dot"></i> 護理館 202</span>
                                </td>
                                <td class="p-3 text-slate-700">全民國防教育</td>
                                <td class="p-3 text-slate-700">英文閱讀與寫作</td>
                            </tr>
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 2 節<br><span class="text-xs text-slate-500 font-normal">09:10 - 10:00</span></td>
                                <td class="p-3 text-slate-700">普通心理學</td>
                                <td class="p-3 bg-amber-50 text-amber-800 font-medium rounded-lg border border-amber-100">
                                    <span class="block font-bold">班會 / 導師時間</span>
                                    <span class="text-xs text-amber-600">護理館 101</span>
                                </td>
                                <td class="p-3 text-slate-700">英文閱讀與寫作</td>
                            </tr>
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 3 節<br><span class="text-xs text-slate-500 font-normal">10:10 - 11:00</span></td>
                                <td class="p-3 text-slate-700">體育 (一)</td>
                                <td rowspan="2" class="p-3 bg-emerald-50/80 text-emerald-800 font-medium rounded-lg border border-emerald-100">
                                    <span class="block font-bold">解剖學實驗</span>
                                    <span class="text-xs text-emerald-600"><i class="fa-solid fa-flask"></i> 實驗大樓 105</span>
                                </td>
                                <td class="p-3 text-slate-700">大學中文</td>
                                <td class="p-3 text-slate-700">通識：藝術欣賞</td>
                                <td class="p-3 text-slate-400 italic">自主學習 / 空堂</td>
                            </tr>
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 4 節<br><span class="text-xs text-slate-500 font-normal">11:10 - 12:00</span></td>
                                <td class="p-3 text-slate-700">體育 (一)</td>
                                <td class="p-3 text-slate-700">大學中文</td>
                                <td class="p-3 text-slate-700">通識：藝術欣賞</td>
                                <td class="p-3 text-slate-400 italic">自主學習 / 空堂</td>
                            </tr>
                            <tr class="bg-slate-100 text-slate-600 font-medium">
                                <td colspan="6" class="py-2.5 text-xs tracking-wider uppercase"><i class="fa-solid fa-utensils mr-1"></i> 午休時間 (12:00 - 13:30)</td>
                            </tr>
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 5 節<br><span class="text-xs text-slate-500 font-normal">13:30 - 14:20</span></td>
                                <td class="p-3 text-slate-700">生理學入門</td>
                                <td class="p-3 text-slate-700">資訊素養</td>
                                <td class="p-3 bg-indigo-50/80 text-indigo-800 font-medium rounded-lg border border-indigo-100">
                                    <span class="block font-bold">基本護理學概論</span>
                                    <span class="text-xs text-indigo-600">護理館 301</span>
                                </td>
                                <td rowspan="2" class="p-3 bg-purple-50/80 text-purple-800 font-medium rounded-lg border border-purple-100">
                                    <span class="block font-bold">化學與生物化學</span>
                                    <span class="text-xs text-purple-600">理學館 402</span>
                                </td>
                                <td class="p-3 text-teal-700 font-medium">社團時間</td>
                            </tr>
                            <tr>
                                <td class="p-3 font-semibold bg-slate-50 text-slate-700">第 6 節<br><span class="text-xs text-slate-500 font-normal">14:30 - 15:20</span></td>
                                <td class="p-3 text-slate-700">生理學入門</td>
                                <td class="p-3 text-slate-700">資訊素養</td>
                                <td class="p-3 text-slate-700">基本護理學概論</td>
                                <td class="p-3 text-teal-700 font-medium">社團時間</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

        <!-- 4. 同學介紹區塊 (#students) -->
        <section id="students" class="scroll-mt-24">
            <div class="flex items-center space-x-3 mb-6">
                <div class="p-3 bg-teal-100 text-teal-700 rounded-xl">
                    <i class="fa-solid fa-users text-2xl"></i>
                </div>
                <div>
                    <h2 class="text-2xl font-bold text-slate-800">護一甲 幹部與同學</h2>
                    <p class="text-sm text-slate-500">互相扶持、共同進步的最佳夥伴們</p>
                </div>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- 同學卡片 1 -->
                <div class="bg-white rounded-2xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden border border-slate-100 group">
                    <div class="relative h-48 overflow-hidden bg-slate-200">
                        <img class="w-full h-full object-cover group-hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&q=80&w=400" alt="班長照片" aria-hidden="true">
                        <span class="absolute top-3 right-3 bg-nursing-500 text-white text-xs font-bold px-3 py-1 rounded-full shadow">班長</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-lg font-bold text-slate-800">01. 林小美</h3>
                        <p class="text-xs text-teal-600 font-medium mb-3"><i class="fa-solid fa-heart mr-1"></i>志願：急診專科護理師</p>
                        <p class="text-sm text-slate-600 mb-3"><strong class="text-slate-700">興趣：</strong>彈吉他、手作甜點</p>
                        <blockquote class="text-xs text-slate-500 italic bg-slate-50 p-2.5 rounded-lg border-l-2 border-nursing-400">
                            「希望大家這四年都能平平安安，一起順利Pass過關！」
                        </blockquote>
                    </div>
                </div>

                <!-- 同學卡片 2 -->
                <div class="bg-white rounded-2xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden border border-slate-100 group">
                    <div class="relative h-48 overflow-hidden bg-slate-200">
                        <img class="w-full h-full object-cover group-hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?auto=format&fit=crop&q=80&w=400" alt="副班長照片" aria-hidden="true">
                        <span class="absolute top-3 right-3 bg-teal-600 text-white text-xs font-bold px-3 py-1 rounded-full shadow">副班長</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-lg font-bold text-slate-800">02. 陳大明</h3>
                        <p class="text-xs text-teal-600 font-medium mb-3"><i class="fa-solid fa-heart mr-1"></i>志願：手術室護理師</p>
                        <p class="text-sm text-slate-600 mb-3"><strong class="text-slate-700">興趣：</strong>打籃球、慢跑</p>
                        <blockquote class="text-xs text-slate-500 italic bg-slate-50 p-2.5 rounded-lg border-l-2 border-teal-400">
                            「課業有問題歡迎隨時討論，班務我也會全力協助！」
                        </blockquote>
                    </div>
                </div>

                <!-- 同學卡片 3 -->
                <div class="bg-white rounded-2xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden border border-slate-100 group">
                    <div class="relative h-48 overflow-hidden bg-slate-200">
                        <img class="w-full h-full object-cover group-hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&q=80&w=400" alt="康樂股長照片" aria-hidden="true">
                        <span class="absolute top-3 right-3 bg-slate-600 text-white text-xs font-bold px-3 py-1 rounded-full shadow">康樂股長</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-lg font-bold text-slate-800">03. 張婷婷</h3>
                        <p class="text-xs text-teal-600 font-medium mb-3"><i class="fa-solid fa-heart mr-1"></i>志願：小兒科護理師</p>
                        <p class="text-sm text-slate-600 mb-3"><strong class="text-slate-700">興趣：</strong>聽流行樂、看韓劇</p>
                        <blockquote class="text-xs text-slate-500 italic bg-slate-50 p-2.5 rounded-lg border-l-2 border-slate-400">
                            「解剖學雖然頭痛，但大家一起讀書一定能搞定！」
                        </blockquote>
                    </div>
                </div>

                <!-- 同學卡片 4 -->
                <div class="bg-white rounded-2xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden border border-slate-100 group">
                    <div class="relative h-48 overflow-hidden bg-slate-200">
                        <img class="w-full h-full object-cover group-hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&q=80&w=400" alt="總務股長照片" aria-hidden="true">
                        <span class="absolute top-3 right-3 bg-slate-600 text-white text-xs font-bold px-3 py-1 rounded-full shadow">總務股長</span>
                    </div>
                    <div class="p-5">
                        <h3 class="text-lg font-bold text-slate-800">04. 黃俊傑</h3>
                        <p class="text-xs text-teal-600 font-medium mb-3"><i class="fa-solid fa-heart mr-1"></i>志願：社區護理師</p>
                        <p class="text-sm text-slate-600 mb-3"><strong class="text-slate-700">興趣：</strong>攝影、羽毛球</p>
                        <blockquote class="text-xs text-slate-500 italic bg-slate-50 p-2.5 rounded-lg border-l-2 border-slate-400">
                            「大家記得準時繳交班費與共筆費用喔～感謝配合！」
                        </blockquote>
                    </div>
                </div>
            </div>
        </section>

        <!-- 5. 隨機抽籤/點名功能區塊 (#random-picker) -->
        <section id="random-picker" class="scroll-mt-24">
            <div class="bg-gradient-to-br from-teal-900 via-teal-800 to-nursing-800 text-white p-6 md:p-10 rounded-3xl shadow-xl relative overflow-hidden">
                <!-- 背景護理十字圖案 -->
                <div class="absolute -right-10 -bottom-10 opacity-10 text-white pointer-events-none">
                    <i class="fa-solid fa-hospital-user text-[240px]"></i>
                </div>

                <div class="relative z-10">
                    <!-- 標題列 -->
                    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8 pb-6 border-b border-teal-700/60">
                        <div class="flex items-center space-x-3">
                            <div class="p-3.5 bg-amber-400 text-slate-900 rounded-2xl shadow-lg">
                                <i class="fa-solid fa-dice text-3xl"></i>
                            </div>
                            <div>
                                <h2 class="text-2xl md:text-3xl font-extrabold tracking-wide">課堂隨機抽籤與點名系統</h2>
                                <p class="text-teal-200 text-sm mt-0.5">課堂提問、值日生安排、實驗分組幸運兒抽籤小幫手</p>
                            </div>
                        </div>
                        <button id="toggleRosterBtn" class="self-start md:self-auto px-4 py-2 bg-teal-700/80 hover:bg-teal-600 text-teal-100 rounded-xl text-sm font-semibold border border-teal-500/40 transition flex items-center space-x-2">
                            <i class="fa-solid fa-user-pen"></i>
                            <span>編輯同學名單 (<span id="rosterCount">12</span>人)</span>
                        </button>
                    </div>

                    <!-- 抽籤設定控制項與主要介面 -->
                    <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
                        
                        <!-- 左側：設定控制面板 (5欄) -->
                        <div class="lg:col-span-5 bg-teal-950/60 backdrop-blur-md p-6 rounded-2xl border border-teal-600/30 space-y-6">
                            <h3 class="text-lg font-bold text-amber-300 flex items-center">
                                <i class="fa-solid fa-sliders mr-2"></i> 抽籤控制項
                            </h3>

                            <!-- 控制項 1: 選取人數 -->
                            <div>
                                <label for="selectCount" class="block text-sm font-semibold mb-2 text-teal-100 flex justify-between">
                                    <span><i class="fa-solid fa-users-line text-teal-400 mr-1.5"></i>抽取人數：</span>
                                    <span id="countDisplay" class="text-amber-300 font-bold">1 人</span>
                                </label>
                                <div class="flex items-center space-x-3">
                                    <input type="range" id="selectCount" min="1" max="6" value="1" class="w-full h-2.5 bg-teal-800 rounded-lg appearance-none cursor-pointer accent-amber-400">
                                </div>
                                <p class="text-xs text-teal-300/70 mt-1">可拖曳選擇一次抽出 1 到 6 位同學</p>
                            </div>

                            <!-- 控制項 2: 是否允許重複抽取 -->
                            <div class="pt-2 border-t border-teal-800">
                                <label class="flex items-center space-x-3 cursor-pointer group">
                                    <div class="relative">
                                        <input type="checkbox" id="allowDuplicate" class="sr-only">
                                        <div id="toggleBg" class="w-11 h-6 bg-teal-800 rounded-full transition group-hover:bg-teal-700"></div>
                                        <div id="toggleDot" class="absolute left-1 top-1 bg-white w-4 h-4 rounded-full transition transform"></div>
                                    </div>
                                    <span class="text-sm font-medium text-teal-100 select-none">允許重複選取相同同學</span>
                                </label>
                                <p class="text-xs text-teal-300/70 mt-1 pl-14">未勾選時，單次抽籤結果不會出現重複名單</p>
                            </div>

                            <!-- 按鈕操作區 -->
                            <div class="pt-4 space-y-3">
                                <button id="startRollBtn" class="w-full py-4 bg-gradient-to-r from-amber-400 to-amber-500 hover:from-amber-300 hover:to-amber-400 text-slate-950 font-black text-xl rounded-2xl shadow-xl transition transform active:scale-95 flex items-center justify-center space-x-3">
                                    <i class="fa-solid fa-bolt text-2xl"></i>
                                    <span>開始隨機抽取！</span>
                                </button>
                                
                                <button id="resetHistoryBtn" class="w-full py-2 bg-teal-800/50 hover:bg-teal-700/60 text-teal-200 text-xs rounded-xl transition border border-teal-700/50">
                                    <i class="fa-solid fa-rotate-left mr-1"></i>清空歷史抽中紀錄
                                </button>
                            </div>
                        </div>

                        <!-- 右側：滾動動畫展示區與歷史紀錄 (7欄) -->
                        <div class="lg:col-span-7 space-y-6">
                            
                            <!-- 閃爍滾動顯示大螢幕 -->
                            <div class="bg-slate-950/80 border-2 border-teal-400/40 rounded-2xl p-8 text-center relative overflow-hidden shadow-inner min-h-[200px] flex flex-col justify-center items-center">
                                <span class="text-xs font-bold text-teal-400 tracking-widest uppercase mb-2 block">
                                    <i class="fa-solid fa-display mr-1"></i> Lucky Student Selector
                                </span>
                                
                                <!-- 滾動名字展示區域 -->
                                <div id="displaySlot" class="text-4xl md:text-5xl font-extrabold text-amber-300 tracking-wider my-2 h-16 flex items-center justify-center transition-all">
                                    準備好了嗎？
                                </div>
                                <p id="statusMsg" class="text-sm text-teal-300/80">點擊左側「開始隨機抽取」按鈕即刻抽籤</p>
                            </div>

                            <!-- 抽籤歷史紀錄清單 -->
                            <div class="bg-teal-950/40 rounded-2xl p-4 border border-teal-700/30">
                                <h4 class="text-xs font-bold uppercase tracking-wider text-teal-300 mb-3 flex items-center">
                                    <i class="fa-solid fa-clock-rotate-left mr-1.5 text-amber-400"></i> 本次抽中歷史紀錄
                                </h4>
                                <div id="historyTags" class="flex flex-wrap gap-2 max-h-28 overflow-y-auto pr-1">
                                    <span class="text-xs text-teal-400/60 italic">尚未進行抽籤...</span>
                                </div>
                            </div>

                        </div>
                    </div>

                    <!-- 隱藏式可編輯同學名單面板 -->
                    <div id="rosterModal" class="hidden mt-8 pt-6 border-t border-teal-700/60 bg-teal-950/80 p-6 rounded-2xl border border-teal-500/30">
                        <div class="flex justify-between items-center mb-3">
                            <h3 class="font-bold text-amber-300 text-lg flex items-center">
                                <i class="fa-solid fa-list-check mr-2"></i> 自訂班級抽籤同學名單
                            </h3>
                            <button id="saveRosterBtn" class="px-4 py-1.5 bg-emerald-500 hover:bg-emerald-600 text-white rounded-lg text-xs font-bold transition">
                                儲存更新名單
                            </button>
                        </div>
                        <p class="text-xs text-teal-200/80 mb-3">請以逗號或換行分隔同學姓名。編輯後點擊儲存即可使用新名單抽取：</p>
                        <textarea id="rosterInput" rows="4" class="w-full bg-slate-900 border border-teal-700 rounded-xl p-3 text-sm text-teal-100 focus:outline-none focus:border-amber-400"></textarea>
                    </div>

                </div>
            </div>
        </section>

        <!-- 6. 班級主題投票區塊 (#poll) -->
        <section id="poll" class="scroll-mt-24">
            <div class="bg-gradient-to-br from-white to-sky-50/50 p-6 md:p-8 rounded-3xl shadow-lg border border-sky-100 max-w-3xl mx-auto">
                <div class="flex items-center space-x-3 mb-6">
                    <div class="p-3 bg-nursing-500 text-white rounded-2xl shadow-md">
                        <i class="fa-solid fa-square-poll-vertical text-2xl"></i>
                    </div>
                    <div>
                        <h2 class="text-2xl font-bold text-slate-800">班級即時投票</h2>
                        <p class="text-sm text-slate-500">每人限投一票，即時呈現最新統計結果</p>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200/80 mb-6">
                    <div class="flex items-center justify-between mb-3">
                        <span class="text-xs font-bold bg-teal-100 text-teal-700 px-3 py-1 rounded-full">進行中</span>
                        <span class="text-xs text-slate-400"><i class="fa-regular fa-clock mr-1"></i>截止日期：10/25 23:59</span>
                    </div>
                    <h3 class="text-xl font-bold text-slate-800 mb-2">【護理週班服顏色選擇】</h3>
                    <p class="text-sm text-slate-600 mb-6">請大家選出最希望能代表我們護一甲的班服顏色：</p>

                    <form id="pollForm" class="space-y-3">
                        <label class="flex items-center p-3.5 rounded-xl border border-slate-200 hover:border-nursing-400 hover:bg-sky-50/50 cursor-pointer transition group">
                            <input type="radio" name="option" value="A" class="w-5 h-5 text-nursing-500 focus:ring-nursing-400" required>
                            <span class="ml-3 font-medium text-slate-700 group-hover:text-slate-900">A. 霧藍色 (代表沉穩與專業)</span>
                        </label>
                        <label class="flex items-center p-3.5 rounded-xl border border-slate-200 hover:border-nursing-400 hover:bg-sky-50/50 cursor-pointer transition group">
                            <input type="radio" name="option" value="B" class="w-5 h-5 text-nursing-500 focus:ring-nursing-400">
                            <span class="ml-3 font-medium text-slate-700 group-hover:text-slate-900">B. 莫蘭迪綠 (代表清新與療癒)</span>
                        </label>
                        <label class="flex items-center p-3.5 rounded-xl border border-slate-200 hover:border-nursing-400 hover:bg-sky-50/50 cursor-pointer transition group">
                            <input type="radio" name="option" value="C" class="w-5 h-5 text-nursing-500 focus:ring-nursing-400">
                            <span class="ml-3 font-medium text-slate-700 group-hover:text-slate-900">C. 燕麥奶茶色 (代表溫暖與包容)</span>
                        </label>
                        <button type="submit" id="submitBtn" class="w-full mt-4 bg-nursing-500 hover:bg-nursing-600 text-white font-bold py-3 rounded-xl shadow-md transition transform active:scale-95 flex items-center justify-center space-x-2">
                            <span>送出我的投票</span>
                            <i class="fa-solid fa-paper-plane"></i>
                        </button>
                    </form>
                </div>

                <!-- 投票結果展示 -->
                <div id="pollResult" class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200/80">
                    <h4 class="font-bold text-slate-800 mb-4 flex items-center justify-between">
                        <span><i class="fa-solid fa-chart-simple text-nursing-500 mr-2"></i>當前投票統計</span>
                        <span id="totalVotesText" class="text-xs text-slate-500 font-normal">總投票數：25 票</span>
                    </h4>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between text-sm font-medium mb-1.5">
                                <span class="text-slate-700">A. 霧藍色</span>
                                <span id="countA" class="text-nursing-600 font-bold">12 票 (48%)</span>
                            </div>
                            <div class="w-full bg-slate-100 rounded-full h-3 overflow-hidden">
                                <div id="barA" class="bg-nursing-500 h-3 rounded-full transition-all duration-700" style="width: 48%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between text-sm font-medium mb-1.5">
                                <span class="text-slate-700">B. 莫蘭迪綠</span>
                                <span id="countB" class="text-teal-600 font-bold">8 票 (32%)</span>
                            </div>
                            <div class="w-full bg-slate-100 rounded-full h-3 overflow-hidden">
                                <div id="barB" class="bg-teal-500 h-3 rounded-full transition-all duration-700" style="width: 32%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between text-sm font-medium mb-1.5">
                                <span class="text-slate-700">C. 燕麥奶茶色</span>
                                <span id="countC" class="text-amber-600 font-bold">5 票 (20%)</span>
                            </div>
                            <div class="w-full bg-slate-100 rounded-full h-3 overflow-hidden">
                                <div id="barC" class="bg-amber-400 h-3 rounded-full transition-all duration-700" style="width: 20%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 7. 系上活動花絮區塊 (#events) -->
        <section id="events" class="scroll-mt-24">
            <div class="flex items-center space-x-3 mb-6">
                <div class="p-3 bg-amber-100 text-amber-700 rounded-xl">
                    <i class="fa-solid fa-camera-retro text-2xl"></i>
                </div>
                <div>
                    <h2 class="text-2xl font-bold text-slate-800">系上活動花絮</h2>
                    <p class="text-sm text-slate-500">紀錄屬於護一甲的每一個精彩瞬間</p>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- 花絮 1 -->
                <div class="bg-white rounded-2xl shadow-md overflow-hidden border border-slate-100 hover:shadow-lg transition">
                    <div class="h-48 overflow-hidden relative">
                        <img class="w-full h-full object-cover hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?auto=format&fit=crop&q=80&w=600" alt="迎新茶會" aria-hidden="true">
                        <span class="absolute bottom-3 left-3 bg-black/60 text-white text-xs px-2.5 py-1 rounded-md backdrop-blur-sm">
                            <i class="fa-regular fa-calendar mr-1"></i>2026/09/15
                        </span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-bold text-lg text-slate-800 mb-2">護理系新生迎新茶會</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            第一次與學長姐們相聚，傳授了超級實用的解剖學共筆整理技巧與實習經驗談！
                        </p>
                    </div>
                </div>

                <!-- 花絮 2 -->
                <div class="bg-white rounded-2xl shadow-md overflow-hidden border border-slate-100 hover:shadow-lg transition">
                    <div class="h-48 overflow-hidden relative">
                        <img class="w-full h-full object-cover hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?auto=format&fit=crop&q=80&w=600" alt="解剖實驗" aria-hidden="true">
                        <span class="absolute bottom-3 left-3 bg-black/60 text-white text-xs px-2.5 py-1 rounded-md backdrop-blur-sm">
                            <i class="fa-regular fa-calendar mr-1"></i>2026/09/28
                        </span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-bold text-lg text-slate-800 mb-2">第一次穿白袍解剖實驗課</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            穿上潔白的實驗袍，操作顯微鏡觀察細胞結構，深刻感受身為護理生該有的嚴謹態度。
                        </p>
                    </div>
                </div>

                <!-- 花絮 3 -->
                <div class="bg-white rounded-2xl shadow-md overflow-hidden border border-slate-100 hover:shadow-lg transition">
                    <div class="h-48 overflow-hidden relative">
                        <img class="w-full h-full object-cover hover:scale-105 transition duration-500" src="https://images.unsplash.com/photo-1511632765486-a01980e01a18?auto=format&fit=crop&q=80&w=600" alt="新生班聚" aria-hidden="true">
                        <span class="absolute bottom-3 left-3 bg-black/60 text-white text-xs px-2.5 py-1 rounded-md backdrop-blur-sm">
                            <i class="fa-regular fa-calendar mr-1"></i>2026/10/02
                        </span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-bold text-lg text-slate-800 mb-2">期中加油班聚火鍋晚會</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            期中考將至，全班圍坐在一起吃熱騰騰的火鍋，交流讀書心得，為彼此加油打氣！
                        </p>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- 8. 頁尾區塊 -->
    <footer class="bg-slate-900 text-slate-400 py-10 mt-20 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-4">
            <div class="flex justify-center items-center space-x-2 text-white font-bold text-lg">
                <i class="fa-solid fa-heart-pulse text-nursing-400"></i>
                <span>護理系一年級甲班 (護一甲)</span>
            </div>
            <p class="text-sm text-slate-500 max-w-md mx-auto">
                本網頁為護一甲班級內部交流平台。用愛與專業，紀錄我們在護理這條路上的點點滴滴。
            </p>
            <div class="pt-4 border-t border-slate-800 text-xs text-slate-600">
                <p>© 114 學年度 護一甲班務團隊 版權所有 | 網頁維護：資訊股長</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript 互動與隨機抽籤邏輯 -->
    <script>
        // --- 1. 基本選單與 UI 互動 ---
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('#mobileMenu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // --- 2. 隨機抽籤與點名系統邏輯 ---
        // 預設同學名單
        let studentRoster = [
            "01. 林小美 (班長)",
            "02. 陳大明 (副班長)",
            "03. 張婷婷 (康樂)",
            "04. 黃俊傑 (總務)",
            "05. 李哲宇",
            "06. 吳沛蓁",
            "07. 蔡宜臻",
            "08. 許家豪",
            "09. 鄭心妤",
            "10. 郭子翔",
            "11. 謝雅婷",
            "12. 楊宗翰"
        ];

        let historyList = [];
        let isRolling = false;

        // DOM 元素引用
        const selectCountInput = document.getElementById('selectCount');
        const countDisplay = document.getElementById('countDisplay');
        const allowDuplicateCheckbox = document.getElementById('allowDuplicate');
        const toggleBg = document.getElementById('toggleBg');
        const toggleDot = document.getElementById('toggleDot');
        const startRollBtn = document.getElementById('startRollBtn');
        const displaySlot = document.getElementById('displaySlot');
        const statusMsg = document.getElementById('statusMsg');
        const historyTags = document.getElementById('historyTags');
        const resetHistoryBtn = document.getElementById('resetHistoryBtn');
        const toggleRosterBtn = document.getElementById('toggleRosterBtn');
        const rosterModal = document.getElementById('rosterModal');
        const rosterInput = document.getElementById('rosterInput');
        const saveRosterBtn = document.getElementById('saveRosterBtn');
        const rosterCountSpan = document.getElementById('rosterCount');

        // 更新人數顯示
        selectCountInput.addEventListener('input', (e) => {
            countDisplay.textContent = `${e.target.value} 人`;
        });

        // 自訂 Checkbox 開關切換視覺
        allowDuplicateCheckbox.addEventListener('change', (e) => {
            if (e.target.checked) {
                toggleBg.classList.replace('bg-teal-800', 'bg-amber-400');
                toggleDot.classList.add('translate-x-5');
            } else {
                toggleBg.classList.replace('bg-amber-400', 'bg-teal-800');
                toggleDot.classList.remove('translate-x-5');
            }
        });

        // 編輯名單切換
        toggleRosterBtn.addEventListener('click', () => {
            rosterModal.classList.toggle('hidden');
            if (!rosterModal.classList.contains('hidden')) {
                rosterInput.value = studentRoster.join('\n');
            }
        });

        // 儲存更新名單
        saveRosterBtn.addEventListener('click', () => {
            const text = rosterInput.value.trim();
            if (!text) {
                alert('同學名單不能為空！');
                return;
            }
            // 支援以換行或逗號分割
            studentRoster = text.split(/[\n,]+/).map(item => item.trim()).filter(item => item.length > 0);
            rosterCountSpan.textContent = studentRoster.length;
            rosterModal.classList.add('hidden');
            
            // 更新 slider 最大值
            selectCountInput.max = Math.min(studentRoster.length, 10);
            if (parseInt(selectCountInput.value) > studentRoster.length) {
                selectCountInput.value = studentRoster.length;
                countDisplay.textContent = `${studentRoster.length} 人`;
            }

            alert(`名單更新成功！目前共有 ${studentRoster.length} 位同學。`);
        });

        // 隨機抽籤核心算法與滾動動畫
        startRollBtn.addEventListener('click', () => {
            if (isRolling) return;
            if (studentRoster.length === 0) {
                alert('同學名單為空，請先編輯新增同學！');
                return;
            }

            const count = parseInt(selectCountInput.value);
            const allowDuplicate = allowDuplicateCheckbox.checked;

            if (!allowDuplicate && count > studentRoster.length) {
                alert(`目前名單只有 ${studentRoster.length} 人，無法不重複抽出 ${count} 人！`);
                return;
            }

            isRolling = true;
            startRollBtn.disabled = true;
            startRollBtn.classList.add('opacity-50', 'cursor-not-allowed');
            statusMsg.textContent = '🎲 隨機滾動中，請稍候...';

            let duration = 2000; // 滾動動畫時長 (毫秒)
            let intervalTime = 60; // 滾動切換間隔
            let elapsedTime = 0;

            // 音效/特效視覺滾動計數器
            const timer = setInterval(() => {
                elapsedTime += intervalTime;
                
                // 動態展示隨機同學名字
                const randomSample = studentRoster[Math.floor(Math.random() * studentRoster.length)];
                displaySlot.textContent = randomSample;
                displaySlot.classList.add('text-teal-200');

                if (elapsedTime >= duration) {
                    clearInterval(timer);
                    finishRoll(count, allowDuplicate);
                }
            }, intervalTime);
        });

        // 完成抽籤並計算獲勝者
        function finishRoll(count, allowDuplicate) {
            let winners = [];

            if (allowDuplicate) {
                for (let i = 0; i < count; i++) {
                    const idx = Math.floor(Math.random() * studentRoster.length);
                    winners.push(studentRoster[idx]);
                }
            } else {
                // 不重複洗牌抽取
                let shuffled = [...studentRoster].sort(() => 0.5 - Math.random());
                winners = shuffled.slice(0, count);
            }

            // 顯示最終中籤同學
            displaySlot.classList.remove('text-teal-200');
            displaySlot.classList.add('text-amber-300', 'scale-105');
            displaySlot.innerHTML = winners.map(w => `<span class="px-2 inline-block animate-bounce-short">🎉 ${w}</span>`).join(' ');

            statusMsg.textContent = `✨ 恭喜以上 ${winners.length} 位幸運同學！`;

            // 紀錄至歷史紀錄區
            winners.forEach(w => {
                historyList.unshift({ name: w, time: new Date().toLocaleTimeString([], {hour: '2-digit', minute:'2-digit', second:'2-digit'}) });
            });
            updateHistoryUI();

            // 觸發彩色禮花彩帶特效 (Confetti)
            if (typeof confetti === 'function') {
                confetti({
                    particleCount: 80,
                    spread: 70,
                    origin: { y: 0.6 }
                });
            }

            // 解鎖按鈕
            setTimeout(() => {
                isRolling = false;
                startRollBtn.disabled = false;
                startRollBtn.classList.remove('opacity-50', 'cursor-not-allowed');
                displaySlot.classList.remove('scale-105');
            }, 800);
        }

        // 更新歷史紀錄 UI
        function updateHistoryUI() {
            if (historyList.length === 0) {
                historyTags.innerHTML = '<span class="text-xs text-teal-400/60 italic">尚未進行抽籤...</span>';
                return;
            }
            historyTags.innerHTML = historyList.map(item => `
                <span class="inline-flex items-center bg-teal-900/90 text-amber-200 border border-teal-600/50 text-xs px-2.5 py-1 rounded-full font-medium">
                    <i class="fa-solid fa-check text-emerald-400 mr-1 text-[10px]"></i> ${item.name}
                    <span class="ml-1.5 text-[10px] text-teal-400">${item.time}</span>
                </span>
            `).join('');
        }

        // 清空歷史紀錄
        resetHistoryBtn.addEventListener('click', () => {
            historyList = [];
            updateHistoryUI();
            displaySlot.textContent = '準備好了嗎？';
            statusMsg.textContent = '歷史紀錄已清空';
        });


        // --- 3. 即時投票統計邏輯 ---
        const votes = { A: 12, B: 8, C: 5 };
        let hasVoted = false;

        document.getElementById('pollForm').addEventListener('submit', function(e) {
            e.preventDefault();

            if (hasVoted) {
                alert('您已經參與過本次投票囉！感謝您的支持。');
                return;
            }

            const selected = document.querySelector('input[name="option"]:checked');
            if (!selected) {
                alert('請先選擇一個選項再提交！');
                return;
            }

            const val = selected.value;
            votes[val]++;
            hasVoted = true;

            const total = votes.A + votes.B + votes.C;

            const pA = Math.round((votes.A / total) * 100);
            const pB = Math.round((votes.B / total) * 100);
            const pC = Math.round((votes.C / total) * 100);

            document.getElementById('countA').textContent = `${votes.A} 票 (${pA}%)`;
            document.getElementById('barA').style.width = `${pA}%`;

            document.getElementById('countB').textContent = `${votes.B} 票 (${pB}%)`;
            document.getElementById('barB').style.width = `${pB}%`;

            document.getElementById('countC').textContent = `${votes.C} 票 (${pC}%)`;
            document.getElementById('barC').style.width = `${pC}%`;

            document.getElementById('totalVotesText').textContent = `總投票數：${total} 票`;

            const submitBtn = document.getElementById('submitBtn');
            submitBtn.classList.remove('bg-nursing-500', 'hover:bg-nursing-600');
            submitBtn.classList.add('bg-emerald-600', 'cursor-not-allowed');
            submitBtn.innerHTML = '<span>已完成投票 <i class="fa-solid fa-circle-check"></i></span>';

            alert('投票成功！感謝您的參與。');
        });
    </script>
</body>
</html>
