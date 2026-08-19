<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pinkjulieland - Mobile Shop</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&family=Prompt:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Prompt', 'sans-serif'],
                        outfit: ['Outfit', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            dark: '#D9779B',     
                            main: '#FF9EBB',     
                            light: '#FFF0F5',    
                            text: '#4A332A',     
                            subtext: '#8A6F65'   
                        }
                    },
                    boxShadow: {
                        'app': '0 -10px 40px -15px rgba(255, 158, 187, 0.15), 0 10px 40px -15px rgba(255, 158, 187, 0.15)',
                        'nav': '0 -5px 20px -5px rgba(255, 158, 187, 0.2)'
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #FAFAFA;
            -webkit-tap-highlight-color: transparent;
        }
        .app-container {
            max-width: 430px;
            margin: 0 auto;
            min-height: 100vh;
            background-color: #FFF0F5;
            position: relative;
            box-shadow: 0 0 20px rgba(0,0,0,0.05);
            overflow-x: hidden;
        }
        .gradient-bg {
            background: linear-gradient(180deg, #FF8DAF 0%, #FFB6C1 100%);
        }
        .stars-bg {
            background-image: 
                radial-gradient(circle at 15% 30%, white 1px, transparent 1.5px),
                radial-gradient(circle at 85% 20%, white 1px, transparent 1.5px),
                radial-gradient(circle at 30% 60%, white 2px, transparent 2.5px),
                radial-gradient(circle at 75% 70%, white 1.5px, transparent 2px);
            background-size: 100% 100%;
        }
        .hero-image-placeholder {
            width: 190px;
            height: 190px;
            background-color: white;
            border-radius: 50%;
            border: 4px solid white;
            box-shadow: 0 10px 20px rgba(255, 158, 187, 0.4);
            margin: 0 auto;
            position: relative;
            z-index: 20;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        .page {
            display: none;
            animation: fadeIn 0.3s ease-out forwards;
            padding-bottom: 90px;
        }
        .page.active {
            display: block;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        /* Custom Scrollbar for template list */
        #template-list::-webkit-scrollbar {
            width: 4px;
        }
        #template-list::-webkit-scrollbar-track {
            background: transparent;
        }
        #template-list::-webkit-scrollbar-thumb {
            background: #FF9EBB;
            border-radius: 10px;
        }
    </style>
</head>
<body class="text-brand-text font-sans antialiased">

    <div class="app-container flex flex-col">
        
        <!-- ==================== PAGE 1: HOME ==================== -->
        <div id="page-home" class="page active">
            <!-- Header Section -->
            <div class="gradient-bg pt-10 px-6 pb-24 relative rounded-b-[40px]">
                <div class="stars-bg absolute inset-0 opacity-40"></div>
                <div class="flex justify-between items-center mb-6 relative z-10">
                    <div class="text-brand-text font-outfit text-2xl font-bold tracking-wide flex flex-col brand-title">
                        PINKJULIELAND
                        <span class="text-xs font-medium tracking-widest text-brand-subtext mt-1">Mobile Shop</span>
                    </div>
                    <div class="relative">
                        <i class="fa-regular fa-bell text-brand-text text-xl"></i>
                        <span class="absolute -top-1 -right-1 w-2.5 h-2.5 bg-brand-main rounded-full border-2 border-white"></span>
                    </div>
                </div>
                
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="text-lg font-semibold text-brand-text flex justify-center items-center">
                        Welcome to my shop 
                        <svg viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5 inline-block text-white ml-1 drop-shadow-sm"><path d="M12 10.5C11.5 8 9 6 6 6 3 6 2 8 2 10.5 2 13 5 14 8 13.5L10 14.5C9.5 17 8 20 6 21 8.5 21 11 19 12 16 13 19 15.5 21 18 21 16 20 14.5 17 14 14.5L16 13.5C19 14 22 13 22 10.5 22 8 21 6 18 6 15 6 12.5 8 12 10.5Z" /></svg>
                    </h1>
                    <p class="text-sm font-medium text-brand-subtext mt-1">ร้านจูรับทำเว็บไซต์ครบวงจร และจำหน่ายแอป</p>
                </div>
                
                <!-- อัปเดตลิงก์รูปภาพโดยตรงจากเว็บฝากรูปแล้วค่ะ ปังชัวร์! -->
                <div class="hero-image-placeholder mt-4 mb-[-80px]">
                    <img src="https://i.postimg.cc/Ssm1y82k/att-wk7qrx-RHAp1Ej-HFxr8ZWJOqko-Id-NEvk-Y6mf5-n2Id-W4.jpg" alt="Pinkjulieland Logo" class="w-full h-full object-cover" onerror="this.onerror=null; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' viewBox=\'0 0 24 24\' fill=\'%23FF9EBB\'><path d=\'M16 6V4C16 1.79 14.21 0 12 0C9.79 0 8 1.79 8 4V6H2V22C2 23.1 2.9 24 4 24H20C21.1 24 22 23.1 22 22V6H16ZM10 4C10 2.9 10.9 2 12 2C13.1 2 14 2.9 14 4V6H10V4ZM20 22H4V8H20V22Z\'/></svg>'">
                </div>
            </div>

            <!-- Content Area -->
            <div class="bg-white rounded-t-[35px] -mt-16 relative z-10 pt-10 px-5 shadow-app pb-6">
                <!-- Fast Menu -->
                <div class="text-center mb-4 mt-12">
                    <span class="text-brand-main font-semibold text-sm tracking-wide bg-brand-light px-4 py-1.5 rounded-full inline-block border border-brand-main/20">
                        Fast Menu
                        <svg class="w-3.5 h-3.5 inline-block text-brand-main ml-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777 2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657 5.656l-2.12 2.122"/></svg>
                    </span>
                </div>
                
                <div class="grid grid-cols-4 gap-3 mb-8">
                    <!-- Menu Items -->
                    <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-services', 1)">
                        <div class="w-14 h-14 rounded-2xl bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-main text-xl shadow-sm border border-brand-main/10 transition-colors">
                            <i class="fa-solid fa-laptop-code"></i>
                        </div>
                        <span class="text-[10px] text-center text-brand-text font-medium leading-tight">รับทำ<br>เว็บไซต์</span>
                    </div>
                    <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-goodnotes', 2)">
                        <div class="w-14 h-14 rounded-2xl bg-[#F5ECE9] group-hover:bg-[#EFE5E2] flex items-center justify-center text-[#8A6F65] text-xl shadow-sm border border-[#EFE5E2] transition-colors">
                            <i class="fa-solid fa-book-open"></i>
                        </div>
                        <span class="text-[10px] text-center text-brand-text font-medium leading-tight">แอป<br>Goodnotes</span>
                    </div>
                    <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-course', -1)">
                        <div class="w-14 h-14 rounded-2xl bg-[#EFE5E2] group-hover:bg-[#E0D4CF] flex items-center justify-center text-brand-text text-xl shadow-sm border border-[#E0D4CF] transition-colors">
                            <i class="fa-solid fa-graduation-cap"></i>
                        </div>
                        <span class="text-[10px] text-center text-brand-text font-medium leading-tight">คอร์ส<br>สอนเว็บ</span>
                    </div>
                    <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-contact', 3)">
                        <div class="w-14 h-14 rounded-2xl bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-main text-xl shadow-sm border border-brand-main/10 transition-colors">
                            <i class="fa-regular fa-comment-dots"></i>
                        </div>
                        <span class="text-[10px] text-center text-brand-text font-medium leading-tight">ช่องทาง<br>ติดต่อ</span>
                    </div>
                </div>

                <!-- Steps & Rules (Global) -->
                <div class="space-y-3 mb-8">
                    <div class="border border-brand-light rounded-2xl bg-white shadow-sm overflow-hidden">
                        <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text">
                            <span class="flex items-center gap-2"><i class="fa-solid fa-list-ol text-brand-main"></i> ขั้นตอนการสั่ง & เงื่อนไข</span>
                        </div>
                        <div class="px-4 py-3 text-sm text-brand-subtext bg-brand-light/40 border-t border-brand-light">
                            <ul class="space-y-2 list-disc pl-4 pb-2">
                                <li>ตามปกติรองาน 4-8 ชั่วโมง แล้วแต่คิว</li>
                                <li>งานเร่ง *2 ของราคา</li>
                                <li>สามารถแคปหน้าเว็บที่อยากได้ของร้านเรามาเป็นเรฟได้ หากไม่แคปและแก้เยอะ จะกระทบคิวถัดไป</li>
                                <li><span class="text-brand-main font-medium">เน้นย้ำ:</span> หลังจากส่งงานให้รีเช็ค ตอบกลับภายในไม่เกิน 30 นาที</li>
                                <li>เขียนรายละเอียดร้านค้า หรือพิมพ์ข้อมูลร้านส่งมาได้เลย</li>
                                <li>หากมีโลโก้ให้แนบลิงก์ Google Drive เท่านั้น ระบุให้ชัดเจน</li>
                                <li>ชำระเงินราคาเริ่มต้น 129.- ส่งงานให้เช็ค หากเกินจากนี้จะแจ้งยอดคงค้าง</li>
                                <li class="text-xs text-brand-subtext/70 mt-2 list-none -ml-4">ในอนาคตอาจมีการเปลี่ยนลิงก์ หากนำไปเปลี่ยนโดเมนแล้วมีค่าใช้จ่าย ทางร้านไม่รับผิดชอบทุกกรณี</li>
                            </ul>
                        </div>
                    </div>
                    <div class="border border-[#EFE5E2] rounded-2xl bg-white shadow-sm overflow-hidden">
                        <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text">
                            <span class="flex items-center gap-2"><i class="fa-solid fa-shield-halved text-brand-text"></i> กฎของร้าน</span>
                        </div>
                        <div class="px-4 py-3 text-sm text-brand-text bg-[#F5ECE9]/50 border-t border-[#EFE5E2]">
                            <ul class="space-y-2 pb-2">
                                <li><i class="fa-solid fa-xmark mr-1"></i> โอนเงินแล้วไม่คืนเงินทุกกรณี</li>
                                <li><i class="fa-solid fa-xmark mr-1"></i> ยกเลิกหลังตรวจงานแล้ว ไม่คืนเงิน</li>
                                <li><i class="fa-solid fa-xmark mr-1"></i> งดจิกงดเร่งทุกกรณีนะคะ</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ==================== PAGE 2: ALL SERVICES (GRID) ==================== -->
        <div id="page-services" class="page">
            <div class="gradient-bg pt-10 px-6 pb-20 relative rounded-b-[40px]">
                <div class="flex justify-between items-center mb-6">
                    <div class="w-8 h-8 bg-brand-light/80 rounded-full flex items-center justify-center text-brand-main backdrop-blur-md shadow-sm cursor-pointer border border-brand-main/20" onclick="switchTab('page-home', 0)">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </div>
                    <div class="text-brand-text font-outfit text-xl font-bold tracking-wide brand-title">PINKJULIELAND</div>
                    <div class="w-8"></div>
                </div>
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="font-outfit text-sm font-medium text-brand-subtext">All Services</h1>
                    <div class="text-2xl font-bold mt-1 text-brand-text flex justify-center items-center">
                        บริการทั้งหมด 
                        <svg class="w-5 h-5 inline-block text-white ml-1 drop-shadow-sm" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 002-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"/></svg>
                    </div>
                </div>
            </div>

            <div class="px-5 -mt-10 relative z-10 pb-8">
                <!-- Grid Menu -->
                <div class="bg-white rounded-[24px] shadow-app p-5 border border-brand-light">
                    <div class="grid grid-cols-4 gap-y-6 gap-x-2">
                        <!-- Templates -->
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="toggleCategory('bright')">
                            <div class="w-12 h-12 rounded-xl bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-main text-xl shadow-sm border border-brand-light transition-colors">
                                <i class="fa-solid fa-sun"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">โทนสดใส</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="toggleCategory('dark')">
                            <div class="w-12 h-12 rounded-xl bg-[#F5ECE9] group-hover:bg-[#EFE5E2] flex items-center justify-center text-[#8A6F65] text-xl shadow-sm border border-[#F5ECE9] transition-colors">
                                <i class="fa-solid fa-moon"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">โทนมืด</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="toggleCategory('pastel')">
                            <div class="w-12 h-12 rounded-xl bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-text text-xl shadow-sm border border-brand-light transition-colors">
                                <i class="fa-solid fa-candy-cane"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">พาสเทล</span>
                        </div>
                        <!-- Links to other pages -->
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-course', -1)">
                            <div class="w-12 h-12 rounded-xl bg-[#EFE5E2] group-hover:bg-[#E0D4CF] flex items-center justify-center text-brand-text text-xl shadow-sm border border-[#EFE5E2] transition-colors">
                                <i class="fa-solid fa-chalkboard-user"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">คอร์สสอน</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-goodnotes', 2)">
                            <div class="w-12 h-12 rounded-xl bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-main text-xl shadow-sm border border-brand-light transition-colors">
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">GN ถาวร</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-goodnotes', 2)">
                            <div class="w-12 h-12 rounded-xl bg-[#F5ECE9] group-hover:bg-[#EFE5E2] flex items-center justify-center text-[#8A6F65] text-xl shadow-sm border border-[#F5ECE9] transition-colors">
                                <i class="fa-solid fa-check-circle"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">GN รายปี</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-goodnotes', 2)">
                            <div class="w-12 h-12 rounded-xl bg-[#EFE5E2] group-hover:bg-[#E0D4CF] flex items-center justify-center text-brand-text text-xl shadow-sm border border-[#EFE5E2] transition-colors">
                                <i class="fa-solid fa-crown"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">GN Pro</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 cursor-pointer group" onclick="switchTab('page-contact', 3)">
                            <div class="w-12 h-12 rounded-full bg-brand-light group-hover:bg-[#FFD1E0] flex items-center justify-center text-brand-main text-xl shadow-sm border border-brand-main/20 transition-colors">
                                <i class="fa-solid fa-ellipsis"></i>
                            </div>
                            <span class="text-[10px] text-center text-brand-text font-medium">ติดต่อ</span>
                        </div>
                    </div>
                </div>

                <!-- Template Content Container -->
                <div id="template-links-container" class="hidden bg-white rounded-[24px] shadow-app border border-brand-light p-5 mt-4">
                    <h3 id="template-title" class="font-bold text-brand-text text-sm mb-3 flex items-center"></h3>
                    <div id="template-list" class="space-y-2 max-h-[300px] overflow-y-auto pr-1"></div>
                </div>

                <div class="border border-[#EFE5E2] rounded-2xl bg-white shadow-sm overflow-hidden mb-3 mt-4">
                    <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text bg-[#F5ECE9]/60">
                        <span class="flex items-center gap-2"><i class="fa-solid fa-triangle-exclamation text-brand-text w-4"></i> กฎกลุ่ม (อ่านก่อนตัดสินใจ)</span>
                    </div>
                    <div class="px-4 py-3 text-[11px] text-brand-text bg-[#F5ECE9]/30 border-t border-[#EFE5E2]">
                        <div class="space-y-3 pb-2 leading-relaxed">
                            <p class="font-bold text-brand-text text-xs"><i class="fa-solid fa-thumbtack mr-1 text-brand-main"></i> กฎสำคัญของกลุ่มคอร์ส</p>
                            <ul class="space-y-2 text-brand-subtext">
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-lock text-brand-main mt-0.5"></i> <span><strong class="text-brand-text">เนื้อหาทั้งหมดเป็นลิขสิทธิ์ของคอร์ส:</strong> ห้ามนำออกนอกกลุ่มโดยเด็ดขาด</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-ban text-brand-text mt-0.5"></i> <span>ห้ามส่งต่อคลิปบทเรียน / ห้ามแจกไฟล์ทุกชนิด</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-ban text-brand-text mt-0.5"></i> <span>ห้ามนำเนื้อหาไปขายต่อ / ห้ามอัปโหลดลงที่อื่นทุกกรณี</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-bullhorn text-brand-main mt-0.5"></i> <span>ห้ามฝากร้าน โฆษณา แชร์สิ่งที่ไม่เกี่ยวข้อง (ลบทันที)</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-book text-brand-text mt-0.5"></i> <span><strong>ดูบทเรียนให้ครบก่อนสอบถาม:</strong> คำถามที่มีในบทเรียนแล้ว ทีมงานจะไม่ตอบซ้ำ</span></li>
                            </ul>
                            <div class="bg-[#F5ECE9] p-3 rounded-xl border border-[#EFE5E2] text-brand-text font-bold text-center mt-2">
                                <i class="fa-solid fa-triangle-exclamation mr-1 text-brand-main"></i> หากตรวจพบการละเมิดกฎ<br>
                                ปรับ 5,000.- ต่อ 1 กรณี<br>
                                <span class="text-[10px] font-medium">(หากมีการเผยแพร่เนื้อหา ข้อความละ 500.- ดำเนินการทันที)</span>
                            </div>
                            <div class="border-t border-[#EFE5E2] pt-3 text-center">
                                <strong class="text-brand-text flex items-center justify-center mb-2 text-xs"><i class="fa-solid fa-location-dot mr-1 text-brand-main"></i> เงื่อนไขเพิ่มเติม <i class="fa-solid fa-location-dot ml-1 text-brand-main"></i></strong>
                                ขอความกรุณาไม่นำสิ่งที่สอนไปประยุกต์ใช้กับ <span class="text-brand-main font-bold">“ผลงานผู้อื่นโดยตรง”</span> นะคะ ให้ยึดตามเนื้อหา หรือออกแบบสไตล์ตัวเอง ไม่อ้างอิงผลงานท่านอื่นค่ะ
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <!-- ==================== PAGE 3: WEBSITE DESIGN ==================== -->
        <div id="page-website" class="page">
            <div class="gradient-bg pt-10 px-6 pb-20 relative rounded-b-[40px]">
                <div class="flex justify-between items-center mb-6">
                    <div class="w-8 h-8 bg-brand-light/80 rounded-full flex items-center justify-center text-brand-main backdrop-blur-md shadow-sm cursor-pointer border border-brand-main/20" onclick="switchTab('page-home', 0)">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </div>
                    <div class="text-brand-text font-outfit text-xl font-bold tracking-wide brand-title">PINKJULIELAND</div>
                    <div class="w-8"></div>
                </div>
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="font-outfit text-sm font-medium text-brand-subtext">Website Services</h1>
                    <div class="text-2xl font-bold mt-1 text-brand-text flex justify-center items-center">
                        รับทำเว็บไซต์ <i class="fa-solid fa-laptop-code ml-2 text-white drop-shadow-sm"></i>
                    </div>
                </div>
            </div>

            <div class="px-5 -mt-10 relative z-10 pb-8 space-y-4">
                <div class="bg-white rounded-[24px] shadow-app border border-brand-light p-6">
                    <div class="text-center mb-4">
                        <span class="bg-brand-light text-brand-main text-[10px] font-bold px-3 py-1 rounded-full border border-brand-main/20">HOT DEAL <i class="fa-solid fa-fire text-brand-text ml-1"></i></span>
                        <h3 class="text-lg font-bold text-brand-text mt-3 mb-1">ออกแบบเว็บไซต์ร้านค้า</h3>
                        <p class="text-xs text-brand-subtext">สวยปัง คุมโทน เพิ่มยอดขายให้ร้านคุณ</p>
                    </div>
                    
                    <div class="bg-brand-light/20 rounded-xl p-4 border border-brand-light space-y-2 mb-4">
                        <div class="flex justify-between items-center border-b border-brand-light pb-2">
                            <span class="text-sm font-medium text-brand-text"><i class="fa-solid fa-star text-brand-main text-[10px] mr-1"></i> เริ่มต้น</span>
                            <span class="text-lg font-bold text-brand-main">129.-</span>
                        </div>
                        <ul class="text-xs text-brand-subtext space-y-2 pt-2">
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-brand-text mt-0.5"></i> ออกแบบให้ตามเรฟ/บรีฟ</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-brand-text mt-0.5"></i> แถมฟรีโดเมนพร้อมใช้ (ลิงก์สั้น)</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-brand-text mt-0.5"></i> จ่ายครั้งเดียว ไม่มีรายเดือน</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-brand-text mt-0.5"></i> งานเร่งด่วน x2 ของราคาปกติ</li>
                        </ul>
                    </div>
                    
                    <button onclick="switchTab('page-contact', 3)" class="w-full bg-brand-main hover:bg-brand-dark text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-pink-300 transition-all text-sm flex items-center justify-center gap-2">
                        ทักแชทสั่งทำเลย <i class="fa-regular fa-paper-plane"></i>
                    </button>
                </div>

                <!-- CARD: คอร์สสอนทำเว็บ -->
                <div class="bg-white rounded-[24px] shadow-app border border-brand-light p-6">
                    <div class="text-center mb-4">
                        <span class="bg-[#F5ECE9] text-brand-text text-[10px] font-bold px-3 py-1 rounded-full border border-[#EFE5E2]">BEST SELLER <i class="fa-solid fa-fire text-brand-main ml-1"></i></span>
                        <h3 class="text-lg font-bold text-brand-text mt-3 mb-1">คอร์สสอนทำ “เว็บร้าน” สไตล์พิ้งจู</h3>
                        <p class="text-[11px] text-brand-subtext">ไม่ต้องมีพื้นฐาน ไม่ต้องงมเอง <i class="fa-solid fa-heart text-brand-main ml-1"></i></p>
                    </div>
                    
                    <div class="bg-[#F5ECE9]/30 rounded-xl p-4 border border-[#EFE5E2] space-y-2 mb-4">
                        <div class="flex justify-between items-center border-b border-[#EFE5E2] pb-2">
                            <span class="text-sm font-medium text-brand-text"><i class="fa-solid fa-sparkles text-brand-text text-[10px] mr-1"></i> เข้าตลอดชีพเพียง</span>
                            <span class="text-lg font-bold text-brand-text">459.-</span>
                        </div>
                        <ul class="text-[10px] text-brand-subtext space-y-2 pt-2">
                            <li class="flex items-start gap-2"><i class="fa-solid fa-play text-brand-text mt-0.5"></i> คลิปสอนทำจริงแบบละเอียด</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-note-sticky text-brand-text mt-0.5"></i> โน้ตสรุป + ทริคสำคัญ อ่านง่าย</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-palette text-brand-text mt-0.5"></i> เทมเพลต 50+ แบบ ใช้ต่อทันที!</li>
                        </ul>
                    </div>
                    
                    <button onclick="switchTab('page-course', -1)" class="w-full bg-brand-text hover:bg-[#3A2821] text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-[#EFE5E2] transition-all text-sm flex items-center justify-center gap-2">
                        ดูรายละเอียดคอร์สเต็มๆ <i class="fa-solid fa-arrow-right ml-1"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- ==================== PAGE 4: GOODNOTES ==================== -->
        <div id="page-goodnotes" class="page">
            <div class="gradient-bg pt-10 px-6 pb-20 relative rounded-b-[40px]">
                <div class="flex justify-between items-center mb-6">
                    <div class="w-8 h-8 bg-brand-light/80 rounded-full flex items-center justify-center text-brand-main backdrop-blur-md shadow-sm cursor-pointer border border-brand-main/20" onclick="switchTab('page-home', 0)">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </div>
                    <div class="text-brand-text font-outfit text-xl font-bold tracking-wide brand-title">PINKJULIELAND</div>
                    <div class="w-8"></div>
                </div>
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="font-outfit text-sm font-medium text-brand-subtext">Premium Apps</h1>
                    <div class="text-2xl font-bold mt-1 text-brand-text flex justify-center items-center">
                        แอป Goodnotes <i class="fa-solid fa-pen-nib ml-2 text-white drop-shadow-sm"></i>
                    </div>
                </div>
            </div>

            <div class="px-5 -mt-10 relative z-10 pb-8 space-y-4">
                <div class="bg-white rounded-[24px] shadow-app border border-brand-light p-5">
                    <p class="text-xs text-brand-subtext text-center mb-4">สายจดสรุป สายเรียนห้ามพลาด! อัปเดตฟรีตลอดชีพ โหลดไว้ใช้ยังไงก็คุ้ม <i class="fa-solid fa-heart text-brand-main ml-1"></i></p>
                    
                    <div class="space-y-3">
                        <!-- รายการ 1 -->
                        <div class="border border-brand-light rounded-xl p-3 flex items-center justify-between bg-white hover:bg-brand-light/30 transition-colors">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-lg bg-brand-light flex items-center justify-center text-brand-main text-lg"><i class="fa-solid fa-infinity"></i></div>
                                <div>
                                    <div class="text-sm font-bold text-brand-text">GN ถาวร (IOS)</div>
                                    <div class="text-[10px] text-brand-subtext">โหลดผ่าน Apple ID ร้าน</div>
                                </div>
                            </div>
                            <div class="text-right">
                                <div class="text-brand-main font-bold text-sm">69.-</div>
                                <button onclick="switchTab('page-contact', 3)" class="text-[9px] bg-brand-light text-brand-main px-2 py-1 rounded-md mt-1 font-bold">สั่งซื้อ</button>
                            </div>
                        </div>

                        <!-- รายการ 2 -->
                        <div class="border border-[#EFE5E2] rounded-xl p-3 flex items-center justify-between bg-white hover:bg-[#F5ECE9]/30 transition-colors">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-lg bg-[#F5ECE9] flex items-center justify-center text-[#8A6F65] text-lg"><i class="fa-solid fa-calendar-check"></i></div>
                                <div>
                                    <div class="text-sm font-bold text-brand-text">GN รายปี (IOS)</div>
                                    <div class="text-[10px] text-brand-subtext">ใช้งาน 1 ปีเต็มสุดคุ้ม</div>
                                </div>
                            </div>
                            <div class="text-right">
                                <div class="text-[#8A6F65] font-bold text-sm">49.-</div>
                                <button onclick="switchTab('page-contact', 3)" class="text-[9px] bg-[#F5ECE9] text-[#8A6F65] px-2 py-1 rounded-md mt-1 font-bold">สั่งซื้อ</button>
                            </div>
                        </div>

                        <!-- รายการ 3 -->
                        <div class="border border-[#EFE5E2] rounded-xl p-3 flex items-center justify-between bg-white hover:bg-[#F5ECE9]/30 transition-colors relative overflow-hidden">
                            <div class="absolute top-0 right-0 bg-brand-text text-white text-[8px] font-bold px-2 py-0.5 rounded-bl-lg">BEST SELLER</div>
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-lg bg-[#EFE5E2] flex items-center justify-center text-brand-text text-lg"><i class="fa-solid fa-crown"></i></div>
                                <div>
                                    <div class="text-sm font-bold text-brand-text">GN Pro (Full)</div>
                                    <div class="text-[10px] text-brand-subtext">ปลดล็อกครบทุกฟังก์ชัน</div>
                                </div>
                            </div>
                            <div class="text-right">
                                <div class="text-brand-text font-bold text-sm">99.-</div>
                                <button onclick="switchTab('page-contact', 3)" class="text-[9px] bg-[#EFE5E2] text-brand-text px-2 py-1 rounded-md mt-1 font-bold">สั่งซื้อ</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ==================== PAGE 5: COURSE DETAILS ==================== -->
        <div id="page-course" class="page">
            <div class="gradient-bg pt-10 px-6 pb-20 relative rounded-b-[40px]">
                <div class="flex justify-between items-center mb-6">
                    <div class="w-8 h-8 bg-brand-light/80 rounded-full flex items-center justify-center text-brand-main backdrop-blur-md shadow-sm cursor-pointer border border-brand-main/20" onclick="switchTab('page-home', 0)">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </div>
                    <div class="text-brand-text font-outfit text-xl font-bold tracking-wide brand-title">PINKJULIELAND</div>
                    <div class="w-8"></div>
                </div>
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="font-outfit text-sm font-medium text-brand-subtext">Learning Class</h1>
                    <div class="text-2xl font-bold mt-1 text-brand-text flex justify-center items-center">
                        คอร์สสอนทำเว็บ <i class="fa-solid fa-graduation-cap ml-2 text-white drop-shadow-sm"></i>
                    </div>
                </div>
            </div>

            <div class="px-5 -mt-10 relative z-10 pb-8 space-y-4">
                <!-- Main Course Card -->
                <div class="bg-white rounded-[24px] shadow-app border border-brand-light p-6">
                    <div class="text-center mb-4">
                        <span class="bg-[#F5ECE9] text-brand-text text-[10px] font-bold px-3 py-1 rounded-full border border-[#EFE5E2]">BEST SELLER <i class="fa-solid fa-fire text-brand-main ml-1"></i></span>
                        <h3 class="text-lg font-bold text-brand-text mt-3 mb-1">คอร์สสอนทำ “เว็บร้าน” สไตล์พิ้งจู</h3>
                        <p class="text-[11px] text-brand-subtext leading-relaxed">
                            จาก 0 <i class="fa-solid fa-arrow-right mx-1 text-[9px]"></i> ทำเว็บใช้งานได้จริง!<br>
                            ไม่ต้องมีพื้นฐาน ไม่ต้องงมเอง <i class="fa-solid fa-sparkles text-brand-main ml-1"></i><br>
                            สอนครบทุกขั้นตอน ดูรอบเดียวทำตามได้เลย
                        </p>
                    </div>
                    
                    <div class="bg-[#F5ECE9]/30 rounded-xl p-4 border border-[#EFE5E2] space-y-3 mb-4">
                        <ul class="text-[11px] text-brand-text space-y-2">
                            <li class="flex items-start gap-2"><div class="w-4 flex justify-center mt-0.5"><i class="fa-solid fa-play text-brand-main"></i></div> <span><strong>คลิปสอนทำจริงแบบละเอียด</strong></span></li>
                            <li class="flex items-start gap-2"><div class="w-4 flex justify-center mt-0.5"><i class="fa-solid fa-note-sticky text-brand-main"></i></div> <span><strong>โน้ตสรุป + ทริคสำคัญ</strong> อ่านง่าย</span></li>
                            <li class="flex items-start gap-2"><div class="w-4 flex justify-center mt-0.5"><i class="fa-solid fa-palette text-brand-main"></i></div> <span><strong>เทมเพลตเว็บ 50+ แบบ</strong> เอาไปใช้ต่อได้ทันที!</span></li>
                        </ul>
                    </div>
                    
                    <div class="bg-brand-light/30 border border-brand-light rounded-xl p-3 mb-4 text-center">
                        <span class="text-brand-subtext text-[11px]">เข้าได้ตลอดชีพในราคาเพียง</span><br>
                        <span class="text-brand-main font-bold text-2xl">459.-</span>
                        <p class="text-[9px] text-brand-subtext mt-1">คุ้มมากสำหรับสายทำเว็บ/หารายได้เสริม! <i class="fa-solid fa-heart text-brand-main ml-0.5"></i></p>
                    </div>

                    <a href="https://drive.google.com/drive/folders/1fj024BhkgC1ctJeiwyZUG3USteSdzWzr" target="_blank" class="w-full bg-white hover:bg-brand-light/50 text-brand-text font-semibold py-3 rounded-xl shadow-sm transition-all text-[11px] flex items-center justify-center gap-2 mb-3 border border-brand-light">
                        <i class="fa-regular fa-folder-open text-brand-main text-sm"></i> ดูตัวอย่างภายในกลุ่ม
                    </a>
                    
                    <button onclick="switchTab('page-contact', 3)" class="w-full bg-brand-text hover:bg-[#3A2821] text-white font-semibold py-3.5 rounded-xl shadow-lg shadow-[#EFE5E2] transition-all text-sm flex items-center justify-center gap-2">
                        ทักแชทสมัครเรียนเลย <i class="fa-solid fa-hand-sparkles ml-1"></i>
                    </button>
                </div>

                <!-- Who is this for -->
                <div class="border border-[#EFE5E2] rounded-2xl bg-white shadow-sm overflow-hidden">
                    <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text bg-[#F5ECE9]/60">
                        <span class="flex items-center gap-2"><i class="fa-solid fa-users text-brand-main w-4"></i> คอร์สนี้เหมาะกับใคร?</span>
                    </div>
                    <div class="px-4 py-3 text-[11px] text-brand-text bg-[#F5ECE9]/30 border-t border-[#EFE5E2]">
                        <p class="text-brand-subtext mb-3 leading-relaxed text-center">เหมาะกับพ่อค้าแม่ค้าหลายสายงาน มีหน้าเว็บรวบรวมรายละเอียดครบ จบในที่เดียว ช่วยลดการตอบซ้ำ และเพิ่มความน่าเชื่อถือ</p>
                        <div class="space-y-3">
                            <div class="bg-white p-3 rounded-xl border border-brand-light shadow-sm">
                                <p class="font-bold text-brand-text mb-1"><i class="fa-solid fa-star text-brand-main text-[10px] mr-1"></i> ขายป้าย / ขายสติกเกอร์</p>
                                <p class="text-brand-subtext">แสดงผลงาน เรตราคา โทนสี ขั้นตอนสั่งงาน และกฎกติกาครบจบ</p>
                            </div>
                            <div class="bg-white p-3 rounded-xl border border-brand-light shadow-sm">
                                <p class="font-bold text-brand-text mb-1"><i class="fa-solid fa-star text-brand-main text-[10px] mr-1"></i> ปล่อยเช่ารหัส / รับเติมเกม</p>
                                <p class="text-brand-subtext">แสดงแพ็กเกจ เรตราคา มีฟอร์มให้ลูกค้าคัดลอกไปจอง ลดการตอบซ้ำ</p>
                            </div>
                            <div class="bg-white p-3 rounded-xl border border-brand-light shadow-sm">
                                <p class="font-bold text-brand-text mb-1"><i class="fa-solid fa-star text-brand-main text-[10px] mr-1"></i> สายคอมมิชชั่น / ทั่วไป</p>
                                <p class="text-brand-subtext">แจ้งรายละเอียด เงื่อนไข พร้อมปุ่มกดเช็คคิวผ่าน Sheet ปรับใช้ได้หมด!</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Scope -->
                <div class="border border-[#EFE5E2] rounded-2xl bg-white shadow-sm overflow-hidden">
                    <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text bg-[#F5ECE9]/60">
                        <span class="flex items-center gap-2"><i class="fa-solid fa-circle-info text-brand-main w-4"></i> ขอบเขตการสอน (ควรอ่าน)</span>
                    </div>
                    <div class="px-4 py-3 text-[11px] text-brand-subtext bg-[#F5ECE9]/30 border-t border-[#EFE5E2] leading-relaxed">
                        <ul class="space-y-2">
                            <li class="flex items-start gap-1.5"><i class="fa-solid fa-check text-brand-main mt-0.5"></i> <span>ภายในคอร์สมีเทมเพลตให้ใช้งานจำนวนมาก พร้อมสอนวิธีใช้งานครบทุกขั้นตอน <strong class="text-brand-text">ไม่ต้องเขียนโค้ดเอง</strong></span></li>
                            <li class="flex items-start gap-1.5"><i class="fa-solid fa-check text-brand-main mt-0.5"></i> <span>เหมาะสำหรับผู้ไม่มีพื้นฐาน นำไปต่อยอดใช้งานได้จริง เน้นการใช้งานเทมเพลตและเทคนิคต่างๆ</span></li>
                            <li class="flex items-start gap-1.5"><i class="fa-solid fa-triangle-exclamation text-brand-text mt-0.5"></i> <span><strong class="text-brand-text">ไม่ได้สอนสร้างเทมเพลตหรือเขียนโค้ดขึ้นมาใหม่</strong> (ไม่ลงลึกระดับผู้พัฒนา) ไม่ได้สอนจับมือเขียนโค้ด</span></li>
                            <li class="flex items-start gap-1.5"><i class="fa-solid fa-check text-brand-main mt-0.5"></i> <span>เหมาะกับคนที่ต้องการความสะดวกสบาย มีตัวเลือกเยอะ อนาคตจะยังคงรูปแบบการสอนเน้นประยุกต์ใช้เป็นหลักค่ะ</span></li>
                        </ul>
                    </div>
                </div>

                <!-- Rules -->
                <div class="border border-[#EFE5E2] rounded-2xl bg-white shadow-sm overflow-hidden">
                    <div class="w-full flex justify-between items-center p-4 text-left font-medium text-sm text-brand-text bg-[#F5ECE9]/60">
                        <span class="flex items-center gap-2"><i class="fa-solid fa-triangle-exclamation text-brand-text w-4"></i> กฎกลุ่ม (อ่านก่อนตัดสินใจ)</span>
                    </div>
                    <div class="px-4 py-3 text-[11px] text-brand-text bg-[#F5ECE9]/30 border-t border-[#EFE5E2]">
                        <div class="space-y-3 pb-2 leading-relaxed">
                            <p class="font-bold text-brand-text text-xs"><i class="fa-solid fa-thumbtack mr-1 text-brand-main"></i> กฎสำคัญของกลุ่มคอร์ส</p>
                            <ul class="space-y-2 text-brand-subtext">
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-lock text-brand-main mt-0.5"></i> <span><strong class="text-brand-text">เนื้อหาทั้งหมดเป็นลิขสิทธิ์ของคอร์ส:</strong> ห้ามนำออกนอกกลุ่มโดยเด็ดขาด</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-ban text-brand-text mt-0.5"></i> <span>ห้ามส่งต่อคลิปบทเรียน / ห้ามแจกไฟล์ทุกชนิด</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-ban text-brand-text mt-0.5"></i> <span>ห้ามนำเนื้อหาไปขายต่อ / ห้ามอัปโหลดลงที่อื่นทุกกรณี</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-bullhorn text-brand-main mt-0.5"></i> <span>ห้ามฝากร้าน โฆษณา แชร์สิ่งที่ไม่เกี่ยวข้อง (ลบทันที)</span></li>
                                <li class="flex items-start gap-1.5"><i class="fa-solid fa-book text-brand-text mt-0.5"></i> <span><strong>ดูบทเรียนให้ครบก่อนสอบถาม:</strong> คำถามที่มีในบทเรียนแล้ว ทีมงานจะไม่ตอบซ้ำ</span></li>
                            </ul>
                            <div class="bg-[#F5ECE9] p-3 rounded-xl border border-[#EFE5E2] text-brand-text font-bold text-center mt-2">
                                <i class="fa-solid fa-triangle-exclamation mr-1 text-brand-main"></i> หากตรวจพบการละเมิดกฎ<br>
                                ปรับ 5,000.- ต่อ 1 กรณี<br>
                                <span class="text-[10px] font-medium">(หากมีการเผยแพร่เนื้อหา ข้อความละ 500.- ดำเนินการทันที)</span>
                            </div>
                            <div class="border-t border-[#EFE5E2] pt-3 text-center">
                                <strong class="text-brand-text flex items-center justify-center mb-2 text-xs"><i class="fa-solid fa-location-dot mr-1 text-brand-main"></i> เงื่อนไขเพิ่มเติม <i class="fa-solid fa-location-dot ml-1 text-brand-main"></i></strong>
                                ขอความกรุณาไม่นำสิ่งที่สอนไปประยุกต์ใช้กับ <span class="text-brand-main font-bold">“ผลงานผู้อื่นโดยตรง”</span> นะคะ ให้ยึดตามเนื้อหา หรือออกแบบสไตล์ตัวเอง ไม่อ้างอิงผลงานท่านอื่นค่ะ
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ==================== PAGE 6: CONTACT ==================== -->
        <div id="page-contact" class="page">
            <div class="gradient-bg pt-10 px-6 pb-20 relative rounded-b-[40px]">
                <div class="flex justify-between items-center mb-6">
                    <div class="w-8 h-8 bg-brand-light/80 rounded-full flex items-center justify-center text-brand-main backdrop-blur-md shadow-sm cursor-pointer border border-brand-main/20" onclick="switchTab('page-home', 0)">
                        <i class="fa-solid fa-chevron-left text-sm"></i>
                    </div>
                    <div class="text-brand-text font-outfit text-xl font-bold tracking-wide brand-title">PINKJULIELAND</div>
                    <div class="w-8"></div>
                </div>
                <div class="text-center mb-2 z-10 relative">
                    <h1 class="font-outfit text-sm font-medium text-brand-subtext">Contact Us</h1>
                    <div class="text-2xl font-bold mt-1 text-brand-text flex justify-center items-center">
                        ช่องทางติดต่อ <i class="fa-regular fa-comments ml-2 text-white drop-shadow-sm"></i>
                    </div>
                </div>
            </div>

            <div class="px-5 -mt-10 relative z-10 pb-8">
                <div class="bg-white rounded-[24px] shadow-app border border-brand-light p-8 flex justify-center gap-8">
                    <a href="https://www.facebook.com/profile.php?id=61554192600355" target="_blank" class="flex flex-col items-center gap-2 group">
                        <div class="w-16 h-16 rounded-full border-2 border-brand-light bg-brand-light/30 text-brand-main flex items-center justify-center text-3xl group-hover:bg-[#8A6F65] group-hover:text-white group-hover:border-[#8A6F65] transition-all shadow-sm">
                            <i class="fa-brands fa-facebook-f"></i>
                        </div>
                        <span class="text-xs font-semibold text-brand-text group-hover:text-[#8A6F65] transition-colors">Facebook</span>
                    </a>
                    <a href="https://lin.ee/t0qYbAl" target="_blank" class="flex flex-col items-center gap-2 group">
                        <div class="w-16 h-16 rounded-full border-2 border-brand-light bg-brand-light/30 text-brand-main flex items-center justify-center text-3xl group-hover:bg-brand-text group-hover:text-white group-hover:border-brand-text transition-all shadow-sm">
                            <i class="fa-brands fa-line"></i>
                        </div>
                        <span class="text-xs font-semibold text-brand-text group-hover:text-brand-text transition-colors">Line</span>
                    </a>
                    <a href="https://www.instagram.com/pinkjulie.land" target="_blank" class="flex flex-col items-center gap-2 group">
                        <div class="w-16 h-16 rounded-full border-2 border-brand-light bg-brand-light/30 text-brand-main flex items-center justify-center text-3xl group-hover:bg-brand-main group-hover:text-white group-hover:border-brand-main transition-all shadow-sm">
                            <i class="fa-brands fa-instagram"></i>
                        </div>
                        <span class="text-xs font-semibold text-brand-text group-hover:text-brand-main transition-colors">Instagram</span>
                    </a>
                </div>
            </div>
        </div>

        <!-- ==================== BOTTOM NAVIGATION ==================== -->
        <div class="fixed bottom-0 left-0 right-0 bg-white/95 backdrop-blur-md border-t border-brand-light px-6 py-3 z-50 shadow-nav max-w-[430px] mx-auto rounded-t-3xl">
            <div class="flex justify-between items-end pb-2">
                <div class="flex flex-col items-center gap-1 cursor-pointer w-1/4 text-brand-main" onclick="switchTab('page-home', 0)" id="nav-item-0">
                    <i class="fa-solid fa-house text-xl mb-0.5"></i>
                    <span class="text-[9px] font-semibold">หน้าแรก</span>
                </div>
                <div class="flex flex-col items-center gap-1 cursor-pointer w-1/4 text-brand-subtext hover:text-brand-main transition-colors" onclick="switchTab('page-website', 1)" id="nav-item-1">
                    <i class="fa-solid fa-laptop-code text-xl mb-0.5"></i>
                    <span class="text-[9px] font-medium">รับทำเว็บ</span>
                </div>
                <div class="relative w-1/4 flex justify-center" onclick="switchTab('page-services', -1)">
                    <div class="absolute -top-10 w-14 h-14 bg-gradient-to-tr from-brand-main to-pink-300 rounded-full flex items-center justify-center text-white text-2xl shadow-lg shadow-pink-300/50 border-4 border-white cursor-pointer transform hover:scale-105 transition-transform">
                        <i class="fa-solid fa-layer-group"></i>
                    </div>
                    <span class="text-[9px] font-bold text-brand-main mt-5">บริการทั้งหมด</span>
                </div>
                <div class="flex flex-col items-center gap-1 cursor-pointer w-1/4 text-brand-subtext hover:text-brand-main transition-colors" onclick="switchTab('page-goodnotes', 2)" id="nav-item-2">
                    <i class="fa-solid fa-book-open text-xl mb-0.5"></i>
                    <span class="text-[9px] font-medium">แอป GN</span>
                </div>
                <div class="flex flex-col items-center gap-1 cursor-pointer w-1/4 text-brand-subtext hover:text-brand-main transition-colors" onclick="switchTab('page-contact', 3)" id="nav-item-3">
                    <i class="fa-regular fa-comment-dots text-xl mb-0.5"></i>
                    <span class="text-[9px] font-medium">ติดต่อ</span>
                </div>
            </div>
        </div>

    </div>

    <!-- Script for Tab Switching & Templates -->
    <script>
        const templates = {
            bright: [
                { name: "✨ ธีมสดใส - ลูกอม", url: "https://t03.cozyw75.workers.dev" },
                { name: "✨ ธีมสดใส - ผลไม้", url: "https://t04.cozyw75.workers.dev" },
                { name: "✨ ธีมสดใส - ท้องฟ้า", url: "https://t05.cozyw75.workers.dev" }
            ],
            dark: [
                { name: "🌙 ธีมมืด - หรูหรา", url: "https://t06.cozyw75.workers.dev" },
                { name: "🌙 ธีมมืด - มินิมอล", url: "https://t07.cozyw75.workers.dev" },
                { name: "🌙 ธีมมืด - คลาสสิค", url: "https://t08.cozyw75.workers.dev" }
            ],
            pastel: [
                { name: "🎀 ธีมพาสเทล - หวานแหวว", url: "https://t09.cozyw75.workers.dev" },
                { name: "🎀 ธีมพาสเทล - ละมุน", url: "https://t10.cozyw75.workers.dev" },
                { name: "🎀 ธีมพาสเทล - เจ้าหญิง", url: "https://t11.cozyw75.workers.dev" }
            ]
        };

        const titles = {
            bright: "<i class='fa-solid fa-sun text-brand-main mr-2'></i> เทมเพลตโทนสดใส",
            dark: "<i class='fa-solid fa-moon text-[#8A6F65] mr-2'></i> เทมเพลตโทนมืด",
            pastel: "<i class='fa-solid fa-candy-cane text-brand-text mr-2'></i> เทมเพลตพาสเทล"
        };

        function switchTab(pageId, navIndex) {
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            document.getElementById(pageId).classList.add('active');
            window.scrollTo(0, 0);

            if(pageId !== 'page-services') {
                document.getElementById('template-links-container').classList.add('hidden');
            }

            if (navIndex >= 0) {
                for (let i = 0; i <= 3; i++) {
                    const item = document.getElementById(`nav-item-${i}`);
                    if (item) {
                        if (i === navIndex) {
                            item.classList.remove('text-brand-subtext');
                            item.classList.add('text-brand-main');
                            item.querySelector('span').classList.replace('font-medium', 'font-semibold');
                        } else {
                            item.classList.remove('text-brand-main');
                            item.classList.add('text-brand-subtext');
                            item.querySelector('span').classList.replace('font-semibold', 'font-medium');
                        }
                    }
                }
            } else {
                for (let i = 0; i <= 3; i++) {
                    const item = document.getElementById(`nav-item-${i}`);
                    if (item) {
                        item.classList.remove('text-brand-main');
                        item.classList.add('text-brand-subtext');
                        item.querySelector('span').classList.replace('font-semibold', 'font-medium');
                    }
                }
            }
        }

        function toggleCategory(cat) {
            const container = document.getElementById('template-links-container');
            const titleEl = document.getElementById('template-title');
            const listEl = document.getElementById('template-list');

            if (!container || !titleEl || !listEl) return;

            titleEl.innerHTML = titles[cat];
            listEl.innerHTML = '';

            templates[cat].forEach(tmpl => {
                const a = document.createElement('a');
                a.href = tmpl.url;
                a.target = '_blank';
                a.className = 'block w-full p-3 mb-2 rounded-xl bg-brand-light/30 border border-brand-light hover:bg-[#FFD1E0] hover:border-[#FF9EBB] transition-colors text-xs font-medium text-brand-text flex justify-between items-center group';
                a.innerHTML = `
                    <span>${tmpl.name}</span>
                    <i class="fa-solid fa-arrow-up-right-from-square text-[10px] text-brand-main opacity-50 group-hover:opacity-100 transition-opacity"></i>
                `;
                listEl.appendChild(a);
            });

            container.classList.remove('hidden');
            container.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>
</body>
</html>
