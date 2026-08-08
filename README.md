<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Binary Rain Animation Background</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
            background-color: #000a16; /* খুব গাঢ় নেভি ব্লু ব্যাকগ্রাউন্ড */
        }

        .canvas-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: space-around;
            pointer-events: none; /* যাতে এই অ্যানিমেশন পেজের অন্যান্য কাজ বাধা না দেয় */
        }

        .binary-column {
            position: relative;
            width: 1ch; /* এক ক্যারেক্টারের প্রস্থ */
            color: rgba(0, 191, 255, 0.7); /* নীল রঙের বাইনারি সংখ্যা */
            font-family: 'Courier New', Courier, monospace;
            font-size: 1.2rem;
            writing-mode: vertical-rl; /* কলামগুলো উল্লম্বভাবে নিচে নামার জন্য */
            text-orientation: upright;
            animation: binary-rain-fall 10s linear infinite; /* নিচে পড়ার অ্যানিমেশন */
            opacity: 0; /* শুরু হবে স্বচ্ছ অবস্থায় */
        }

        /* অ্যানিমেশনের মাধ্যমে টেক্সট নিচে পড়া এবং দেখা যাওয়া */
        @keyframes binary-rain-fall {
            0% {
                transform: translateY(-100%);
                opacity: 0;
            }
            10% {
                opacity: 1; /* ধীরে ধীরে দৃশ্যমান হবে */
            }
            80% {
                opacity: 1;
            }
            100% {
                transform: translateY(100vh);
                opacity: 0; /* শেষে আবার স্বচ্ছ হয়ে যাবে */
            }
        }

        /* কলামগুলোতে random বাইনারি সংখ্যা যোগ করার জন্য CSS `::before` */
        .binary-column::before {
            content: "10100110101101001010111010011001010111010011010101011010011001010101110"; /* একটি কলামের জন্য ডামি বাইনারি */
            white-space: pre;
            display: inline-block;
        }

        /* বিভিন্ন কলামের জন্য ভিন্ন ভিন্ন সময় এবং ডিলে (delay) যোগ করা, যাতে র্যান্ডম মনে হয় */
        .binary-column:nth-child(2) { animation-duration: 8s; animation-delay: -2s; color: rgba(0, 255, 255, 0.6); }
        .binary-column:nth-child(3) { animation-duration: 12s; animation-delay: -5s; color: rgba(30, 144, 255, 0.8); }
        .binary-column:nth-child(4) { animation-duration: 9s; animation-delay: -1s; }
        .binary-column:nth-child(5) { animation-duration: 11s; animation-delay: -7s; color: rgba(0, 191, 255, 0.5); }
        .binary-column:nth-child(7) { animation-duration: 7s; animation-delay: -3s; color: rgba(0, 255, 255, 0.7); }
        .binary-column:nth-child(8) { animation-duration: 13s; animation-delay: -9s; }
        .binary-column:nth-child(10) { animation-duration: 10s; animation-delay: -4s; color: rgba(30, 144, 255, 0.6); }
        .binary-column:nth-child(12) { animation-duration: 12s; animation-delay: -6s; color: rgba(0, 191, 255, 0.7); }
        .binary-column:nth-child(13) { animation-duration: 8s; animation-delay: -1.5s; }
        .binary-column:nth-child(15) { animation-duration: 11s; animation-delay: -8s; color: rgba(0, 255, 255, 0.6); }
        
        /* আরও কলাম যোগ করতে চাইলে এখানে `.binary-column:nth-child(n)` এ স্টাইল যোগ করুন */
    </style>
</head>
<body>

    <div class="canvas-container">
        <!-- ৩০টি কলামের জন্য HTML। আপনি প্রয়োজন অনুযায়ী কলাম বাড়াতে বা কমাতে পারেন -->
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
        <div class="binary-column"></div> <div class="binary-column"></div>
    </div>

</body>
</html>





















<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a192f,100:172a45&height=220&section=header&text=Aminul%20Islam%20Efat&fontSize=40&fontColor=ffffff&animation=twinkling&desc=Ethical%20Hacker%20%7C%20Security%20Researcher%20%7C%20Computer%20Science%20Engineering&descSize=16&descAlignY=65" width="100%" alt="Aminul Islam Efat - Cyber Security Banner"/>
</p>
