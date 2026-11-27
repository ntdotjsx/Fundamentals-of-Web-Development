---
layout: default
transition: fade-out
---

<div class="h-full flex flex-col justify-between py-2">
  <div
    v-motion
    :initial="{ opacity: 0, y: -12 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 480 } }"
    class="flex items-center justify-between"
  >
    <span class="eyebrow-mono !mb-0">
      <carbon:rocket class="w-4 h-4" />
      <span>COURSE OVERVIEW • 10 DAYS</span>
    </span>
    <span class="font-mono text-xs text-white/75 tracking-wider">MINI CAFE FULL-STACK</span>
  </div>
  <div
    v-motion
    :initial="{ opacity: 0, y: 18 }"
    :enter="{ opacity: 1, y: 0, transition: { delay: 100, duration: 560 } }"
    class="my-auto max-w-4xl"
  >
    <div class="font-mono text-base font-bold text-white/75 tracking-widest mb-2">
      0% → 100% IN 10 DAYS
    </div>
    <h1 class="!text-[3.35rem] !leading-[1.08] font-extrabold text-white mb-4">
      Fundamentals of<br />Web Development
    </h1>
    <p class="text-[20px] text-white/85 max-w-2xl leading-relaxed m-0">
      จากศูนย์สู่ระบบร้านคาเฟ่จริง <strong>Mini Cafe Full-Stack</strong>
      ด้วย HTML5, CSS3, JavaScript, PHP, MariaDB และ Docker Compose
    </p>
  </div>
  <div
    v-motion
    :initial="{ opacity: 0, y: 14 }"
    :enter="{ opacity: 1, y: 0, transition: { delay: 260, duration: 540 } }"
    class="pt-4 border-t border-white/25 flex items-center justify-between gap-2"
  >
    <div class="flex items-center gap-2.5 flex-wrap">
      <div class="logo-chip animate-float" style="animation-delay: 0s" title="VS Code"><img src="/logos/vscode.svg" alt="VS Code" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 0.2s" title="Chrome"><img src="/logos/chrome.svg" alt="Chrome" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 0.4s" title="HTML5"><img src="/logos/html5.svg" alt="HTML5" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 0.6s" title="CSS3"><img src="/logos/css3.svg" alt="CSS3" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 0.8s" title="JavaScript"><img src="/logos/javascript.svg" alt="JavaScript" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 1.0s" title="PHP 8.3"><img src="/logos/php.svg" alt="PHP" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 1.2s" title="Apache"><img src="/logos/apache.svg" alt="Apache" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 1.4s" title="Docker"><img src="/logos/docker.svg" alt="Docker" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 1.6s" title="MariaDB"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
      <div class="logo-chip animate-float" style="animation-delay: 1.8s" title="phpMyAdmin"><img src="/logos/phpmyadmin.svg" alt="phpMyAdmin" /></div>
    </div>
    <span class="font-mono text-xs text-white/70 hidden sm:inline">10 TECHNOLOGIES</span>
  </div>
</div>

<!--
สวัสดีทุกคนครับ! ยินดีต้อนรับเข้าสู่หลักสูตร Fundamentals of Web Development 0% ถึง 100% ใน 10 วัน
วันนี้เราจะมาเห็นภาพรวมทั้งหมดก่อนเริ่มลงมือจริง ว่าตลอด 10 วันนี้เราจะได้เรียนเทคโนโลยีอะไรบ้าง (ทั้ง 10 โลโก้ด้านล่าง) และเราจะปั้นโปรเจกต์ Mini Cafe Full-Stack ออกมาเป็นรูปเป็นร่างได้ยังไง
-->

---
transition: slide-left
---

<div class="h-full grid grid-cols-12 gap-10 items-center">
  <div
    v-motion
    :initial="{ opacity: 0, x: -20 }"
    :enter="{ opacity: 1, x: 0, transition: { duration: 500 } }"
    class="col-span-5 pr-6 border-r border-white/25"
  >
    <div class="eyebrow-mono">
      <carbon:chat class="w-4 h-4" />
      <span>PHILOSOPHY</span>
    </div>
    <h1 class="!text-[2.65rem] !leading-[1.15] font-extrabold text-white mb-4">
      เหมือนรุ่นพี่<br />มานั่งเล่าให้ฟัง<br />ข้างๆ
    </h1>
    <p class="text-[16px] text-white/80 m-0">
      ไม่ท่องจำทฤษฎีแห้งๆ แต่เข้าใจผ่านเรื่องใกล้ตัวและลงมือทำจริงทุกวัน
    </p>
  </div>
  <div class="col-span-7 flex flex-col">
    <div v-click class="hairline-row py-4 flex items-baseline gap-5">
      <span class="font-mono text-2xl font-bold text-white/45">01</span>
      <div>
        <div class="text-[19px] font-bold text-white">ค่อยๆ ปูพื้นทีละก้าวจาก 0%</div>
        <div class="text-[14.5px] text-white/75">เปิดเว็บหน้าแรกในชีวิตได้จริงภายใน 15 นาที</div>
      </div>
    </div>
    <div v-click class="hairline-row py-4 flex items-baseline gap-5">
      <span class="font-mono text-2xl font-bold text-white/45">02</span>
      <div>
        <div class="text-[19px] font-bold text-white">เปรียบเทียบกับเรื่องใกล้ตัว</div>
        <div class="text-[14.5px] text-white/75">เข้าใจภาพรวมเว็บได้ทันทีเหมือนการสร้างบ้าน 1 หลัง</div>
      </div>
    </div>
    <div v-click class="hairline-row py-4 flex items-baseline gap-5">
      <span class="font-mono text-2xl font-bold text-white/45">03</span>
      <div>
        <div class="text-[19px] font-bold text-white">มีรูปภาพและ ER-Diagram</div>
        <div class="text-[14.5px] text-white/75">วาดพิมพ์เขียวฐานข้อมูลก่อนลงมือเขียนโค้ดจริง</div>
      </div>
    </div>
    <div v-click class="hairline-row py-4 flex items-baseline gap-5">
      <span class="font-mono text-2xl font-bold text-white/45">04</span>
      <div>
        <div class="text-[19px] font-bold text-white">ลงมือทำโปรเจกต์จริงทุกวัน</div>
        <div class="text-[14.5px] text-white/75">ต่อยอดทีละวันจนจบเป็นระบบ Mini Cafe Full-Stack</div>
      </div>
    </div>
  </div>
</div>

<!--
สไตล์การเรียนของเราจะไม่เน้นท่องจำทฤษฎีแบบน่าเบื่อ แต่จะเป็นฟีลรุ่นพี่มานั่งเล่าให้ฟังข้างๆ
ค่อยๆ ปูพื้นจากศูนย์ เปรียบเทียบกับเรื่องใกล้ตัว วาดแผนภาพให้เห็นภาพชัดๆ รวมถึง ER-Diagram และลงมือทำจริงทุกวันจนครบ 10 วันครับ
-->

---
transition: slide-left
---

<div class="h-full grid grid-cols-12 gap-8 items-center">
  <div
    v-motion
    :initial="{ opacity: 0, x: -18 }"
    :enter="{ opacity: 1, x: 0, transition: { duration: 480 } }"
    class="col-span-4"
  >
    <div class="eyebrow-mono">
      <carbon:tools class="w-4 h-4" />
      <span>TECH STACK 1/2</span>
    </div>
    <h1 class="!text-[2.5rem] !leading-[1.12] font-extrabold text-white mb-3">
      Frontend<br />& Core Tools
    </h1>
    <div class="font-mono text-3xl font-bold text-white/35">DAY 01—07</div>
  </div>
  <div class="col-span-8 flex flex-col">
    <div v-motion :initial="{ opacity: 0, x: 16 }" :enter="{ opacity: 1, x: 0, transition: { delay: 80, duration: 400 } }" class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/vscode.svg" alt="VS Code" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">VS Code</div>
        <div class="text-[13.5px] text-white/80">Code Editor คู่ใจ + Extension Live Server</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 1–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/chrome.svg" alt="Chrome" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">Browser & DevTools</div>
        <div class="text-[13.5px] text-white/80">แสดงผลเว็บ, Inspect CSS, ทดสอบมือถือ และ Console</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 1–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/html5.svg" alt="HTML5" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">HTML5</div>
        <div class="text-[13.5px] text-white/80">โครงสร้างและเนื้อหาเว็บ (Semantic HTML, Forms, Tags)</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 1–5</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/css3.svg" alt="CSS3" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">CSS3</div>
        <div class="text-[13.5px] text-white/80">Box Model, Flexbox, CSS Grid, Responsive & Variables</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 2–5</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/javascript.svg" alt="JavaScript" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">JavaScript</div>
        <div class="text-[13.5px] text-white/80">สมองและ Logic ของหน้าเว็บ (Functions, DOM & Events)</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 6–7</span>
    </div>
  </div>
</div>

<!--
มาดูอาวุธชุดแรกที่เราจะใช้กันครับ ฝั่งเครื่องมือหลักและหน้าบ้าน (Frontend)
มี VS Code กับ Chrome DevTools ที่อยู่กับเราตั้งแต่ Day 1 ถึง Day 10
ตามด้วย 3 ทหารเสือหน้าบ้านอย่าง HTML5, CSS3 และ JavaScript ในช่วง Day 1 ถึง Day 7 ครับ
-->

---
transition: slide-left
---

<div class="h-full grid grid-cols-12 gap-8 items-center">
  <div class="col-span-8 flex flex-col">
    <div v-motion :initial="{ opacity: 0, x: -16 }" :enter="{ opacity: 1, x: 0, transition: { delay: 80, duration: 400 } }" class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/php.svg" alt="PHP" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">PHP 8.3</div>
        <div class="text-[13.5px] text-white/80">Backend, Server-side Rendering, PDO + Prepared Statements</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 8–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/apache.svg" alt="Apache" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">Apache HTTP Server</div>
        <div class="text-[13.5px] text-white/80">เว็บเซิร์ฟเวอร์รันโค้ด PHP ใน Container <code>php:8.3-apache</code></div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 8–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/docker.svg" alt="Docker" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">Docker & Compose</div>
        <div class="text-[13.5px] text-white/80">เปิด PHP + MariaDB + phpMyAdmin พร้อมกันด้วยคำสั่งเดียว</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 8–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">MariaDB 11 & SQL</div>
        <div class="text-[13.5px] text-white/80">ฐานข้อมูลเชิงสัมพันธ์ เก็บหมวดหมู่ เมนู และออเดอร์ถาวร</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 8–10</span>
    </div>
    <div v-click class="hairline-row py-3 flex items-center gap-4">
      <div class="logo-chip-sm"><img src="/logos/phpmyadmin.svg" alt="phpMyAdmin" /></div>
      <div class="flex-1 min-w-0">
        <div class="text-[17px] font-bold text-white">phpMyAdmin</div>
        <div class="text-[13.5px] text-white/80">หน้าเว็บจัดการฐานข้อมูล MariaDB และรัน SQL แบบเห็นภาพ</div>
      </div>
      <span class="font-mono text-xs text-white/70 shrink-0">DAY 8–10</span>
    </div>
  </div>
  <div
    v-motion
    :initial="{ opacity: 0, x: 18 }"
    :enter="{ opacity: 1, x: 0, transition: { duration: 480 } }"
    class="col-span-4 text-right"
  >
    <div class="eyebrow-mono justify-end">
      <span>TECH STACK 2/2</span>
      <carbon:tools class="w-4 h-4" />
    </div>
    <h1 class="!text-[2.5rem] !leading-[1.12] font-extrabold text-white mb-3">
      Backend<br />& Infra
    </h1>
    <div class="font-mono text-3xl font-bold text-white/35">DAY 08—10</div>
  </div>
</div>

<!--
และนี่คืออาวุธชุดหลังที่เราจะได้จับกันในช่วง Day 8–10 ครับ
มี PHP 8.3 รันบน Apache HTTP Server, มี Docker Compose ช่วยเปิดระบบทั้งหมดด้วยคำสั่งเดียวไม่ติดปัญหาเครื่องใครเครื่องมัน,
เก็บข้อมูลจริงใน MariaDB 11 และเปิดดูตารางแบบเห็นภาพผ่าน phpMyAdmin ครับ
-->

---
transition: slide-left
---

<div class="h-full flex flex-col justify-center">
  <div
    v-motion
    :initial="{ opacity: 0, y: -12 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 450 } }"
    class="mb-8"
  >
    <div class="eyebrow-mono">
      <carbon:cafe class="w-4 h-4" />
      <span>CAPSTONE PROJECT</span>
    </div>
    <h1 class="!text-[2.45rem] font-extrabold text-white m-0">
      Mini Cafe Full-Stack — พัฒนาการ 4 ช่วง
    </h1>
  </div>
  <div class="grid grid-cols-4 border-t border-white/25 pt-6">
    <div v-click class="pr-5 border-r border-white/20 flex flex-col justify-between min-h-[220px]">
      <div>
        <div class="font-mono text-4xl font-extrabold text-white/30 mb-2">01</div>
        <div class="font-mono text-xs text-white/75 mb-2">DAY 1–5</div>
        <h3 class="!text-[19px] font-bold text-white mb-2 m-0">หน้าร้าน Responsive</h3>
        <p class="text-[14px] text-white/80 m-0">เปิดสวยทั้งมือถือและคอมด้วย HTML5 + CSS3</p>
      </div>
      <div class="flex gap-2 mt-4">
        <div class="logo-chip-sm"><img src="/logos/html5.svg" alt="HTML5" /></div>
        <div class="logo-chip-sm"><img src="/logos/css3.svg" alt="CSS3" /></div>
      </div>
    </div>
    <div v-click class="px-5 border-r border-white/20 flex flex-col justify-between min-h-[220px]">
      <div>
        <div class="font-mono text-4xl font-extrabold text-white/30 mb-2">02</div>
        <div class="font-mono text-xs text-white/75 mb-2">DAY 6–7</div>
        <h3 class="!text-[19px] font-bold text-white mb-2 m-0">ตะกร้า & ส่วนลด</h3>
        <p class="text-[14px] text-white/80 m-0">เลือกเมนูและคำนวณราคาอัตโนมัติด้วย JS</p>
      </div>
      <div class="flex gap-2 mt-4">
        <div class="logo-chip-sm"><img src="/logos/javascript.svg" alt="JS" /></div>
      </div>
    </div>
    <div v-click class="px-5 border-r border-white/20 flex flex-col justify-between min-h-[220px]">
      <div>
        <div class="font-mono text-4xl font-extrabold text-white/30 mb-2">03</div>
        <div class="font-mono text-xs text-white/75 mb-2">DAY 8–9</div>
        <h3 class="!text-[19px] font-bold text-white mb-2 m-0">หลังบ้าน & Docker</h3>
        <p class="text-[14px] text-white/80 m-0">PHP + วาด ER-Diagram + Docker Compose</p>
      </div>
      <div class="flex gap-2 mt-4">
        <div class="logo-chip-sm"><img src="/logos/php.svg" alt="PHP" /></div>
        <div class="logo-chip-sm"><img src="/logos/docker.svg" alt="Docker" /></div>
      </div>
    </div>
    <div v-click class="pl-5 flex flex-col justify-between min-h-[220px]">
      <div>
        <div class="font-mono text-4xl font-extrabold text-white mb-2">04</div>
        <div class="font-mono text-xs text-white/90 mb-2">DAY 10 • LAUNCH</div>
        <h3 class="!text-[19px] font-bold text-white mb-2 m-0">ระบบจริง Full-Stack</h3>
        <p class="text-[14px] text-white/85 m-0">เพิ่ม/ลบเมนู และบันทึกออเดอร์ลง MariaDB จริง</p>
      </div>
      <div class="flex gap-2 mt-4">
        <div class="logo-chip-sm"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
        <div class="logo-chip-sm"><img src="/logos/phpmyadmin.svg" alt="phpMyAdmin" /></div>
      </div>
    </div>
  </div>
</div>

<!--
นี่คือวิวัฒนาการของโปรเจกต์ Mini Cafe ที่เราจะสร้างไปด้วยกันครับ
ช่วงที่ 1 ทำหน้าร้านให้สวย ช่วงที่ 2 เติมสมองให้กดสั่งซื้อคำนวณราคาได้ ช่วงที่ 3 วางหลังบ้านกับฐานข้อมูลและ Docker Compose
และช่วงที่ 4 Day 10 คือวันประกอบร่างเป็นระบบจริงที่บันทึกออเดอร์ลง MariaDB ได้เลยครับ!
-->

---
transition: slide-left
---

<div class="h-full flex flex-col justify-center">
  <div
    v-motion
    :initial="{ opacity: 0, y: -10 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 450 } }"
    class="mb-4"
  >
    <div class="eyebrow-mono">
      <carbon:home class="w-4 h-4" />
      <span>MENTAL MODEL</span>
    </div>
    <h1 class="!text-[2.2rem] font-extrabold text-white m-0">
      เว็บไซต์ก็เหมือนการสร้างบ้าน 1 หลัง
    </h1>
  </div>
  <div class="grid grid-cols-12 gap-7 items-stretch flex-1 max-h-[365px]">
    <div class="col-span-6">
      <HouseAnalogy :step="$clicks" />
    </div>
    <div class="col-span-6 flex flex-col justify-center">
      <div v-click="1" class="hairline-row py-3.5 flex items-center gap-4">
        <div class="logo-chip-sm"><img src="/logos/html5.svg" alt="HTML5" /></div>
        <div>
          <div class="text-[17px] font-bold text-white">HTML = โครงสร้าง อิฐ เสา กำแพง</div>
          <div class="text-[13.5px] text-white/80">กำหนดหัวข้อ รูปภาพ และปุ่มต่างๆ</div>
        </div>
      </div>
      <div v-click="2" class="hairline-row py-3.5 flex items-center gap-4">
        <div class="logo-chip-sm"><img src="/logos/css3.svg" alt="CSS3" /></div>
        <div>
          <div class="text-[17px] font-bold text-white">CSS = ทาสี ตกแต่ง จัดเฟอร์นิเจอร์</div>
          <div class="text-[13.5px] text-white/80">ทำให้สวย น่าอ่าน และรองรับทุกหน้าจอ</div>
        </div>
      </div>
      <div v-click="3" class="hairline-row py-3.5 flex items-center gap-4">
        <div class="logo-chip-sm"><img src="/logos/javascript.svg" alt="JavaScript" /></div>
        <div>
          <div class="text-[17px] font-bold text-white">JS = ระบบไฟฟ้า ประตูอัตโนมัติ กริ่ง</div>
          <div class="text-[13.5px] text-white/80">ทำให้หน้าเว็บโต้ตอบกับคนใช้งานได้</div>
        </div>
      </div>
      <div v-click="4" class="hairline-row py-3.5 flex items-center gap-4">
        <div class="flex -space-x-2 shrink-0">
          <div class="logo-chip-sm"><img src="/logos/php.svg" alt="PHP" /></div>
          <div class="logo-chip-sm"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
        </div>
        <div>
          <div class="text-[17px] font-bold text-white">PHP + MariaDB = ห้องครัว & คลังวัตถุดิบ</div>
          <div class="text-[13.5px] text-white/80">จัดการหลังบ้าน บันทึกออเดอร์ลงฐานข้อมูลถาวร</div>
        </div>
      </div>
    </div>
  </div>
</div>

<!--
ลองจินตนาการว่าการทำเว็บ 1 เว็บก็เหมือนการสร้างบ้าน 1 หลังครับ (กด Space ทีละครั้งเพื่อประกอบบ้านให้ดู)
1. HTML คือโครงสร้าง เสา กำแพง
2. CSS คือทาสี ตกแต่งร้านให้สวย
3. JavaScript คือเดินระบบไฟฟ้า เปิดไฟ ป้าย OPEN กริ่งหน้าบ้านให้โต้ตอบได้
4. PHP + MariaDB คือห้องครัวและตู้เก็บวัตถุดิบหลังบ้านที่เก็บออเดอร์ไว้ถาวรครับ
-->

---
transition: slide-left
---

<div class="mb-4 flex items-end justify-between">
  <div>
    <div class="eyebrow-mono">
      <carbon:code class="w-4 h-4" />
      <span>SHIKI MAGIC MOVE</span>
    </div>
    <h1 class="!text-[2.15rem] font-extrabold text-white m-0">
      โค้ด Mini Cafe ที่ค่อยๆ เติบโตทีละขั้น
    </h1>
  </div>
  <div class="flex items-center gap-2">
    <div class="logo-chip-sm"><img src="/logos/html5.svg" alt="HTML5" /></div>
    <div class="logo-chip-sm"><img src="/logos/css3.svg" alt="CSS3" /></div>
    <div class="logo-chip-sm"><img src="/logos/javascript.svg" alt="JS" /></div>
    <div class="logo-chip-sm"><img src="/logos/php.svg" alt="PHP" /></div>
  </div>
</div>

<div class="code-window">
<div class="code-window-bar">
  <div class="code-dots">
    <span class="bg-rose-400" />
    <span class="bg-amber-400" />
    <span class="bg-emerald-400" />
  </div>
  <span class="text-xs font-mono text-white/60">mini-cafe / Day 1 → Day 10</span>
</div>

````md magic-move {lines: true}
```html
<!-- Day 1–5: HTML5 โครงสร้างการ์ดเมนู -->
<div class="menu-card">
  <h3>Iced Latte</h3>
  <p>65 บาท</p>
  <button>สั่งเลย</button>
</div>
```

```html
<!-- Day 2–5: เติม CSS3 ตกแต่งการ์ดให้สวย -->
<style>
  .menu-card { padding: 1.5rem; border-radius: 1rem; background: #fff; }
</style>
<div class="menu-card">
  <h3>Iced Latte</h3>
  <p>65 บาท</p>
  <button>สั่งเลย</button>
</div>
```

```html
<!-- Day 6–7: เติม JavaScript กดใส่ตะกร้าและคำนวณราคา -->
<div class="menu-card">
  <h3>Iced Latte</h3>
  <p>65 บาท</p>
  <button onclick="addToCart('Iced Latte', 65)">สั่งเลย</button>
</div>
<script>
  let total = 0
  const addToCart = (name, price) => console.log(name, total += price)
</script>
```

```php
<?php
// Day 8–10: ส่งออเดอร์เข้าหลังบ้าน PHP + MariaDB (PDO)
$stmt = $pdo->prepare(
  'INSERT INTO orders (menu_name, price) VALUES (:name, :price)'
);
$stmt->execute([
  'name'  => 'Iced Latte',
  'price' => 65,
]);
```
````

</div>

<!--
ลองดูตัวอย่างโค้ดจริงของร้าน Mini Cafe ที่ค่อยๆ เติบโตทีละขั้นครับ (กด Space เพื่อดู Magic Move แปลงร่างโค้ด)
เริ่มจาก HTML ไม่กี่บรรทัด → เติม CSS ให้สวย → เติม JavaScript ให้กดสั่งและบวกเงินได้ → จนถึง PHP + PDO ที่บันทึกออเดอร์ลง MariaDB จริงๆ!
-->

---
transition: slide-left
---

<div class="mb-4 flex items-end justify-between">
  <div>
    <div class="eyebrow-mono">
      <carbon:container-software class="w-4 h-4" />
      <span>LINE HIGHLIGHT</span>
    </div>
    <h1 class="!text-[2.15rem] font-extrabold text-white m-0">
      เปิดทั้งระบบด้วยคำสั่งเดียว <code>docker compose up</code>
    </h1>
  </div>
  <div class="flex items-center gap-2">
    <div class="logo-chip-sm"><img src="/logos/docker.svg" alt="Docker" /></div>
    <div class="logo-chip-sm"><img src="/logos/apache.svg" alt="Apache" /></div>
    <div class="logo-chip-sm"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
    <div class="logo-chip-sm"><img src="/logos/phpmyadmin.svg" alt="phpMyAdmin" /></div>
  </div>
</div>

<div class="code-window">
<div class="code-window-bar">
  <div class="code-dots">
    <span class="bg-rose-400" />
    <span class="bg-amber-400" />
    <span class="bg-emerald-400" />
  </div>
  <span class="text-xs font-mono text-white/60">docker-compose.yml (Day 8–10)</span>
</div>

```yaml {all|2-5|6-10|11-14|all}{lines:true}
services:
  web:                          # 1. PHP 8.3 + Apache Web Server
    image: php:8.3-apache
    ports: ["8080:80"]
    volumes: ["./src:/var/www/html"]
  db:                           # 2. MariaDB 11 Database
    image: mariadb:11
    environment:
      MARIADB_DATABASE: mini_cafe
      MARIADB_ROOT_PASSWORD: secret
  phpmyadmin:                   # 3. หน้าเว็บจัดการฐานข้อมูล
    image: phpmyadmin:latest
    ports: ["8081:80"]
    depends_on: [db]
```

</div>

<!--
และนี่คือพระเอกของ Day 8–10 ครับ ไฟล์ docker-compose.yml
กด Space ทีละครั้งเพื่อโฟกัสทีละกล่อง:
1. web — รัน PHP 8.3 บน Apache HTTP Server
2. db — รันฐานข้อมูล MariaDB 11 เก็บเมนูและออเดอร์
3. phpmyadmin — เปิดหน้าเว็บจัดการฐานข้อมูลแบบเห็นภาพ รันได้เหมือนกัน 100% ทุกเครื่องด้วยคำสั่งเดียวครับ!
-->

---
transition: slide-left
---

<div class="h-full flex flex-col justify-center">
  <div
    v-motion
    :initial="{ opacity: 0, y: -12 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 450 } }"
    class="mb-12"
  >
    <div class="eyebrow-mono">
      <carbon:roadmap class="w-4 h-4" />
      <span>10-DAY ROADMAP</span>
    </div>
    <h1 class="!text-[2.4rem] font-extrabold text-white m-0">
      เส้นทางการเรียนทั้ง 10 วัน
    </h1>
  </div>
  <div class="relative">
    <div class="absolute top-3 left-4 right-4 h-[2px] bg-white/30" />
    <div class="grid grid-cols-4 gap-6 relative">
      <div v-click class="flex flex-col">
        <div class="w-6 h-6 rounded-full bg-white text-indigo-950 font-mono text-xs font-bold flex items-center justify-center shadow mb-5">1</div>
        <div class="font-mono text-xs text-white/70 mb-1">DAY 1–5</div>
        <div class="text-[20px] font-bold text-white mb-1">HTML, CSS</div>
        <p class="text-[14px] text-white/80 mb-4">สร้างหน้าร้าน Mini Cafe แบบ Responsive</p>
        <div class="flex gap-2">
          <div class="logo-chip-sm"><img src="/logos/html5.svg" alt="HTML5" /></div>
          <div class="logo-chip-sm"><img src="/logos/css3.svg" alt="CSS3" /></div>
        </div>
      </div>
      <div v-click class="flex flex-col">
        <div class="w-6 h-6 rounded-full bg-white text-indigo-950 font-mono text-xs font-bold flex items-center justify-center shadow mb-5">2</div>
        <div class="font-mono text-xs text-white/70 mb-1">DAY 6–7</div>
        <div class="text-[20px] font-bold text-white mb-1">JS & Logic</div>
        <p class="text-[14px] text-white/80 mb-4">ทำตะกร้าสินค้าและคำนวณราคาอัตโนมัติ</p>
        <div class="flex gap-2">
          <div class="logo-chip-sm"><img src="/logos/javascript.svg" alt="JS" /></div>
          <div class="logo-chip-sm"><img src="/logos/chrome.svg" alt="Chrome" /></div>
        </div>
      </div>
      <div v-click class="flex flex-col">
        <div class="w-6 h-6 rounded-full bg-white text-indigo-950 font-mono text-xs font-bold flex items-center justify-center shadow mb-5">3</div>
        <div class="font-mono text-xs text-white/70 mb-1">DAY 8–9</div>
        <div class="text-[20px] font-bold text-white mb-1">PHP & Docker</div>
        <p class="text-[14px] text-white/80 mb-4">ER-Diagram, Docker Compose & MariaDB</p>
        <div class="flex gap-2">
          <div class="logo-chip-sm"><img src="/logos/php.svg" alt="PHP" /></div>
          <div class="logo-chip-sm"><img src="/logos/docker.svg" alt="Docker" /></div>
          <div class="logo-chip-sm"><img src="/logos/mariadb.svg" alt="MariaDB" /></div>
        </div>
      </div>
      <div v-click class="flex flex-col">
        <div class="w-6 h-6 rounded-full bg-emerald-300 text-slate-950 font-mono text-xs font-bold flex items-center justify-center shadow mb-5">4</div>
        <div class="font-mono text-xs text-emerald-200 mb-1">DAY 10</div>
        <div class="text-[20px] font-bold text-white mb-1">Project จริง</div>
        <p class="text-[14px] text-white/85 mb-4">ส่งมอบระบบ Mini Cafe Full-Stack</p>
        <div class="flex gap-2">
          <div class="logo-chip-sm"><img src="/logos/apache.svg" alt="Apache" /></div>
          <div class="logo-chip-sm"><img src="/logos/phpmyadmin.svg" alt="phpMyAdmin" /></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!--
นี่คือแผนที่การเดินทางตลอด 10 วันแบบเห็นภาพชัดๆ ครับ
เราเดินทีละด่านจากซ้ายไปขวา: ปูพื้นหน้าบ้าน → เติม Logic JavaScript → ขึ้นหลังบ้าน PHP + Docker + MariaDB → และจบด้วยโปรเจกต์จริงใน Day 10
-->

---
transition: slide-left
---

<div class="h-full flex flex-col justify-center">
  <div
    v-motion
    :initial="{ opacity: 0, y: -12 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 450 } }"
    class="mb-6"
  >
    <div class="eyebrow-mono">
      <carbon:list-checked class="w-4 h-4" />
      <span>OUTCOMES</span>
    </div>
    <h1 class="!text-[2.25rem] font-extrabold text-white m-0">
      จบแต่ละช่วง คุณจะทำอะไรได้บ้าง
    </h1>
  </div>
  <div class="thin-glass px-7 py-3">
    <div v-click class="hairline-row py-4 grid grid-cols-12 gap-4 items-center">
      <span class="col-span-2 font-mono text-sm font-bold text-white/75">DAY 1–5</span>
      <span class="col-span-3 text-[16px] font-bold text-white">เริ่มต้นจากศูนย์</span>
      <span class="col-span-7 text-[15.5px] text-white/90">สร้างหน้าร้าน Mini Cafe ที่สวยและรองรับมือถือด้วยตัวเอง</span>
    </div>
    <div v-click class="hairline-row py-4 grid grid-cols-12 gap-4 items-center">
      <span class="col-span-2 font-mono text-sm font-bold text-white/75">DAY 6–7</span>
      <span class="col-span-3 text-[16px] font-bold text-white">เริ่มเขียนโปรแกรม</span>
      <span class="col-span-7 text-[15.5px] text-white/90">กดคลิก เพิ่ม/ลดเมนู และคำนวณราคารวมอัตโนมัติด้วย JS</span>
    </div>
    <div v-click class="hairline-row py-4 grid grid-cols-12 gap-4 items-center">
      <span class="col-span-2 font-mono text-sm font-bold text-white/75">DAY 8–9</span>
      <span class="col-span-3 text-[16px] font-bold text-white">Backend & Env</span>
      <span class="col-span-7 text-[15.5px] text-white/90">วาด ER-Diagram เป็น และเชื่อม PHP กับ MariaDB ผ่าน Docker</span>
    </div>
    <div v-click class="hairline-row py-4 grid grid-cols-12 gap-4 items-center">
      <span class="col-span-2 font-mono text-sm font-bold text-emerald-200">DAY 10</span>
      <span class="col-span-3 text-[16px] font-bold text-white">Project จริง</span>
      <span class="col-span-7 text-[15.5px] text-white font-semibold">ส่งมอบระบบ Mini Cafe จัดการเมนูและรับออเดอร์จริง</span>
    </div>
  </div>
</div>

<!--
ตารางนี้สรุปเป้าหมายของแต่ละช่วงไว้ให้เช็กตัวเองได้ง่ายๆ เลยครับ
พอจบช่วงไหน ให้ลองเช็กฝั่งขวาว่าเราทำสิ่งนั้นได้ด้วยตัวเองแล้วหรือยัง ถ้าทำได้แสดงว่าพร้อมลุยช่วงถัดไปเต็มร้อยครับ!
-->

---
transition: fade-out
---

<div class="h-full flex flex-col justify-between py-2">
  <div
    v-motion
    :initial="{ opacity: 0, y: -12 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 450 } }"
  >
    <div class="eyebrow-mono">
      <carbon:idea class="w-4 h-4" />
      <span>BEFORE DAY 1</span>
    </div>
    <h1 class="!text-[2.6rem] font-extrabold text-white m-0">
      ยังไม่ต้องลง Docker ในช่วงแรก
    </h1>
  </div>
  <div
    v-motion
    :initial="{ opacity: 0, y: 12 }"
    :enter="{ opacity: 1, y: 0, transition: { delay: 100, duration: 480 } }"
    class="thin-glass px-7 py-5 flex items-center justify-between gap-6"
  >
    <p class="text-[17.5px] text-white/90 m-0 leading-relaxed">
      ใน <strong>Day 1–7</strong> ใช้แค่ <strong>VS Code</strong> กับ <strong>Browser</strong> เพื่อโฟกัสพื้นฐานให้แน่นก่อน
      แล้วพอถึง <strong>Day 8</strong> ค่อยเปิด <strong>Docker Desktop</strong> พร้อมกันทีเดียว
    </p>
    <div class="flex items-center gap-2.5 shrink-0">
      <div class="logo-chip"><img src="/logos/vscode.svg" alt="VS Code" /></div>
      <div class="logo-chip"><img src="/logos/chrome.svg" alt="Chrome" /></div>
    </div>
  </div>
  <div class="grid grid-cols-4 gap-6 pt-5 border-t border-white/25">
    <div v-click>
      <div class="font-mono text-xs text-white/65 mb-1">DAY 01</div>
      <div class="text-[16px] font-bold text-white">เว็บแรกใน 15 นาที</div>
      <div class="text-[13px] text-white/75">VS Code, Browser & HTML</div>
    </div>
    <div v-click>
      <div class="font-mono text-xs text-white/65 mb-1">DAY 06</div>
      <div class="text-[16px] font-bold text-white">คิดแบบโปรแกรมเมอร์</div>
      <div class="text-[13px] text-white/75">JavaScript & Functions</div>
    </div>
    <div v-click>
      <div class="font-mono text-xs text-white/65 mb-1">DAY 08</div>
      <div class="text-[16px] font-bold text-white">โลก Backend</div>
      <div class="text-[13px] text-white/75">PHP CLI & Docker Compose</div>
    </div>
    <div v-click>
      <div class="font-mono text-xs text-emerald-200 mb-1">DAY 10</div>
      <div class="text-[16px] font-bold text-white">Mini Cafe ใช้งานจริง</div>
      <div class="text-[13px] text-white/80">PHP + MariaDB Full-Stack</div>
    </div>
  </div>
</div>

<!--
ก่อนจะแยกย้ายไปเริ่ม Day 1 มีเคล็ดลับเล็กๆ ที่ช่วยลดความกังวลได้เยอะเลยครับ:
ช่วง Day 1 ถึง Day 7 ยังไม่ต้องลง Docker นะครับ! แค่มี VS Code กับ Chrome หรือ Edge ก็ลุยได้ทันที
พอถึง Day 8 เราค่อยเปิด Docker Desktop พร้อมกันทีเดียว เตรียมตัวให้พร้อมแล้วไปลุย Day 1 กันเลยครับ!
-->
