<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<title>Sinh nhật Hello Kitty pastel 🎀</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500;600;700&family=Quicksand:wght@500;600;700&display=swap');

*{box-sizing:border-box;margin:0;padding:0}
:root{--pink:#ff5d9e;--blue:#75d7ff;--gold:#ffd85a;--night:#07091b}
html,body{width:100%;height:100%;overflow:hidden}
body{font-family:Quicksand,sans-serif;background:var(--night);color:#fff}
button,input,textarea{font:inherit}

/* =========================
   APP CHÍNH
========================= */
#app{
    height:100%;display:flex;
    background:radial-gradient(circle at 70% 40%,#241447,#090516 70%);
    overflow:hidden;
}
.stage{position:relative;flex:1;min-width:0;overflow:hidden}
#stars{position:absolute;inset:0;width:100%;height:100%}

.moon-main{
    position:absolute;right:7%;top:6%;
    width:min(22vw,220px);height:min(22vw,220px);
    border-radius:50%;
    background:radial-gradient(circle at 30% 28%,#fff 0,#fff8d7 34%,#f6cf61 70%,#b47c18 100%);
    box-shadow:0 0 50px #ffe58b,0 0 120px rgba(255,203,67,.35);
    animation:moonFloat 4s ease-in-out infinite alternate;z-index:2;
}
.moon-main:after{
    content:"";position:absolute;inset:0;border-radius:50%;
    background:
      radial-gradient(circle at 42% 40%,rgba(160,110,0,.14) 0 8%,transparent 9%),
      radial-gradient(circle at 67% 35%,rgba(160,110,0,.12) 0 10%,transparent 11%);
}
@keyframes moonFloat{to{transform:translateY(-9px) scale(1.03)}}

.layer{position:absolute;inset:0;pointer-events:none}

/* =========================
   KHÔNG GIAN SINH NHẬT PASTEL
========================= */

/* MÂY */
.cloud{
    position:absolute;
    width:180px;
    height:55px;
    border-radius:50%;
    background:rgba(255,255,255,.10);
    filter:blur(2px);
    opacity:.45;
    z-index:1;
    pointer-events:none;
    transform-style:preserve-3d;
}

.cloud::before,
.cloud::after{
    content:"";
    position:absolute;
    border-radius:50%;
    background:inherit;
}

.cloud::before{
    width:90px;
    height:90px;
    left:30px;
    bottom:0;
}

.cloud::after{
    width:115px;
    height:75px;
    right:20px;
    bottom:0;
}

.cloud1{
    left:-40px;
    top:22%;
    transform:translateZ(-1700px) scale(1.3);
    animation:cloudMove1 18s ease-in-out infinite alternate;
}

.cloud2{
    right:-60px;
    top:42%;
    transform:translateZ(-2100px) scale(.9);
    animation:cloudMove2 22s ease-in-out infinite alternate;
}

.cloud3{
    left:35%;
    top:8%;
    transform:translateZ(-2500px) scale(.7);
    opacity:.25;
    animation:cloudMove3 25s ease-in-out infinite alternate;
}

@keyframes cloudMove1{
    from{margin-left:-30px}
    to{margin-left:70px}
}

@keyframes cloudMove2{
    from{margin-right:-20px}
    to{margin-right:80px}
}

@keyframes cloudMove3{
    from{transform:translateZ(-2500px) translateX(-40px) scale(.7)}
    to{transform:translateZ(-2500px) translateX(60px) scale(.7)}
}


/* =========================
   SAO LẤP LÁNH PHÍA XA
========================= */

.star-group{
    position:absolute;
    color:#fff7c7;
    font-size:22px;
    text-shadow:
        0 0 8px #fff,
        0 0 18px #ffe68a,
        0 0 30px #fff0a0;
    z-index:1;
    pointer-events:none;
    transform-style:preserve-3d;
    animation:starTwinkle 2s ease-in-out infinite alternate;
}

.sg1{
    left:12%;
    top:18%;
    transform:translateZ(-2200px) scale(.8);
}

.sg2{
    left:25%;
    top:52%;
    transform:translateZ(-1800px) scale(.55);
    animation-delay:.7s;
}

.sg3{
    right:18%;
    top:25%;
    transform:translateZ(-2400px) scale(.7);
    animation-delay:1.2s;
}

.sg4{
    right:32%;
    top:62%;
    transform:translateZ(-1600px) scale(.5);
    animation-delay:.4s;
}

.sg5{
    left:52%;
    top:14%;
    transform:translateZ(-2800px) scale(.45);
    animation-delay:1.5s;
}

@keyframes starTwinkle{
    from{
        opacity:.25;
        scale:.7;
    }
    to{
        opacity:1;
        scale:1.15;
    }
}


/* =========================
   HOA TRÔI PHÍA SAU
========================= */

.moon-flower{
    position:absolute;
    z-index:2;
    pointer-events:none;
    filter:
        drop-shadow(0 0 8px rgba(255,180,220,.7))
        drop-shadow(0 0 18px rgba(255,120,200,.35));
    transform-style:preserve-3d;
    opacity:.65;
}

.mf1{
    left:7%;
    top:67%;
    font-size:38px;
    transform:translateZ(-1300px) rotate(-15deg);
    animation:flowerFloat1 7s ease-in-out infinite alternate;
}

.mf2{
    right:10%;
    top:72%;
    font-size:30px;
    transform:translateZ(-1800px) rotate(20deg);
    animation:flowerFloat2 9s ease-in-out infinite alternate;
}

.mf3{
    right:25%;
    top:35%;
    font-size:25px;
    transform:translateZ(-2200px);
    animation:flowerFloat1 8s ease-in-out infinite alternate;
}

@keyframes flowerFloat1{
    to{
        transform:
            translateZ(-1300px)
            translateY(-25px)
            rotate(15deg);
    }
}

@keyframes flowerFloat2{
    to{
        transform:
            translateZ(-1800px)
            translateY(-35px)
            rotate(-15deg);
    }
}


/* =========================
   TRÁI TIM PHÍA XA
========================= */

.bg-heart{
    position:absolute;
    color:#ff8fca;
    font-family:Arial;
    text-shadow:
        0 0 8px #ff72b6,
        0 0 22px #ff72b6;
    z-index:1;
    pointer-events:none;
    opacity:.4;
    transform-style:preserve-3d;
    animation:bgHeartFloat 6s ease-in-out infinite alternate;
}

.bh1{
    left:17%;
    top:35%;
    font-size:45px;
    transform:translateZ(-1700px);
}

.bh2{
    right:16%;
    top:48%;
    font-size:65px;
    transform:translateZ(-2300px);
    animation-delay:1.5s;
}

.bh3{
    left:42%;
    top:72%;
    font-size:32px;
    transform:translateZ(-1400px);
    animation-delay:3s;
}

@keyframes bgHeartFloat{
    from{
        transform:
            translateZ(-1800px)
            translateY(15px)
            rotate(-8deg);
    }
    to{
        transform:
            translateZ(-1800px)
            translateY(-20px)
            rotate(8deg);
    }
}


/* =========================
   VÒNG SÁNG MẶT TRĂNG
========================= */

.moon-ring{
    position:absolute;
    left:50%;
    top:50%;
    border:1px solid rgba(255,235,150,.12);
    border-radius:50%;
    pointer-events:none;
    z-index:0;
    transform-style:preserve-3d;
}
/* =========================
   🌙 MẶT TRĂNG TRONG KHÔNG GIAN - RÕ NÉT
========================= */

.space-moon{
    position:absolute;
    left:50%;
    top:50%;
    width:190px;
    height:190px;

    margin-left:-95px;
    margin-top:-95px;

    border-radius:50%;

    /* mặt trăng rõ nét */
    background:
        radial-gradient(circle at 32% 28%,
            #fffef0 0%,
            #fff7c2 28%,
            #ffe99a 55%,
            #e8bd62 78%,
            #b98238 100%
        );

    box-shadow:
        0 0 25px rgba(255,238,155,.95),
        0 0 60px rgba(255,220,100,.65),
        0 0 110px rgba(255,210,80,.3);

    z-index:4;
    transform-style:preserve-3d;

    transform:
        translateZ(-900px)
        rotateY(-12deg);

    opacity:.98;
}

/* Các hố trên mặt trăng */
.space-moon::before{
    content:"";

    position:absolute;
    inset:0;

    border-radius:50%;

    background:
        radial-gradient(circle at 25% 32%,
            rgba(150,105,45,.28) 0 8px,
            transparent 9px
        ),
        radial-gradient(circle at 62% 25%,
            rgba(150,105,45,.22) 0 13px,
            transparent 14px
        ),
        radial-gradient(circle at 72% 58%,
            rgba(150,105,45,.24) 0 10px,
            transparent 11px
        ),
        radial-gradient(circle at 38% 68%,
            rgba(150,105,45,.2) 0 15px,
            transparent 16px
        ),
        radial-gradient(circle at 52% 45%,
            rgba(150,105,45,.2) 0 7px,
            transparent 8px
        );

    opacity:.8;
}

/* Ánh sáng viền */
.space-moon::after{
    content:"";

    position:absolute;
    inset:-8px;

    border-radius:50%;

    border:2px solid rgba(255,245,190,.55);

    box-shadow:
        0 0 18px rgba(255,235,150,.8),
        inset 0 0 25px rgba(255,255,210,.25);

    pointer-events:none;
}


/* =========================
   🐇 THỎ CƯỠI MẶT TRĂNG
========================= */

.rabbit-moon{
    position:absolute;

    left:50%;
    top:50%;

    margin-left:-42px;
    margin-top:-105px;

    font-size:72px;

    z-index:6;

    transform:
        translateZ(-760px)
        rotate(-8deg);

    filter:
        drop-shadow(0 0 8px rgba(255,255,255,.9))
        drop-shadow(0 0 18px rgba(255,220,130,.65));

    transform-style:preserve-3d;

    animation:
        rabbitFloat 4s ease-in-out infinite alternate;
}

@keyframes rabbitFloat{
    from{
        transform:
            translateZ(-760px)
            translateY(4px)
            rotate(-8deg);
    }

    to{
        transform:
            translateZ(-760px)
            translateY(-7px)
            rotate(6deg);
    }
}


/* =========================
   🏮 ĐÈN LỒNG NHỎ PHÍA XA
========================= */

.space-lantern{
    position:absolute;

    font-size:32px;

    z-index:3;

    filter:
        drop-shadow(0 0 8px #ff9b45)
        drop-shadow(0 0 20px #ff6b38);

    transform-style:preserve-3d;

    animation:
        spaceLanternFloat 6s ease-in-out infinite alternate;
}

.sl1{
    left:18%;
    top:27%;
    transform:translateZ(-1300px) scale(.7);
}

.sl2{
    right:16%;
    top:31%;
    transform:translateZ(-1700px) scale(.55);
    animation-delay:-2s;
}

.sl3{
    left:76%;
    top:68%;
    transform:translateZ(-1100px) scale(.45);
    animation-delay:-4s;
}

@keyframes spaceLanternFloat{
    from{
        margin-top:8px;
        rotate:-4deg;
    }

    to{
        margin-top:-18px;
        rotate:5deg;
    }
}


/* =========================
   ☄️ SAO BĂNG
========================= */

.shooting-star{
    position:absolute;

    width:90px;
    height:2px;

    background:
        linear-gradient(
            90deg,
            transparent,
            rgba(255,255,255,.4),
            #fff,
            transparent
        );

    border-radius:50%;

    box-shadow:
        0 0 8px #fff,
        0 0 18px #ffe99a;

    opacity:.75;

    z-index:2;

    transform:
        translateZ(-1500px)
        rotate(-25deg);

    animation:
        shootingStar 5s linear infinite;
}

.ss1{
    left:5%;
    top:20%;
}

.ss2{
    right:5%;
    top:48%;
    transform:
        translateZ(-1900px)
        rotate(-25deg)
        scale(.7);

    animation-delay:2.5s;
}

@keyframes shootingStar{
    0%{
        opacity:0;
        transform:
            translate3d(-80px,-30px,-1500px)
            rotate(-25deg);
    }

    15%{
        opacity:1;
    }

    45%{
        opacity:.8;
    }

    100%{
        opacity:0;
        transform:
            translate3d(280px,140px,-1500px)
            rotate(-25deg);
    }
}


/* =========================
   🌸 CÁNH HOA BAY TRONG KHÔNG GIAN
========================= */

.space-petal{
    position:absolute;

    z-index:3;

    font-size:28px;

    filter:
        drop-shadow(0 0 6px rgba(255,130,190,.8));

    transform-style:preserve-3d;

    animation:
        spacePetal 8s ease-in-out infinite alternate;
}

.sp1{
    left:14%;
    top:57%;
    transform:translateZ(-1100px) rotate(20deg);
}

.sp2{
    right:14%;
    top:19%;
    transform:translateZ(-1500px) rotate(-20deg);
    animation-delay:-3s;
}

.sp3{
    left:68%;
    top:78%;
    transform:translateZ(-1900px) scale(.6);
    animation-delay:-5s;
}

@keyframes spacePetal{
    from{
        translate:0 15px;
        rotate:-15deg;
    }

    to{
        translate:35px -25px;
        rotate:25deg;
    }
}


/* =========================
   ✨ BỤI SAO XUNG QUANH MẶT TRĂNG
========================= */

.moon-dust{
    position:absolute;

    left:50%;
    top:50%;

    width:500px;
    height:500px;

    margin-left:-250px;
    margin-top:-250px;

    border-radius:50%;

    z-index:2;

    transform:
        translateZ(-1000px);

    pointer-events:none;

    background:
        radial-gradient(circle at 20% 30%, #fff 0 2px, transparent 3px),
        radial-gradient(circle at 75% 22%, #fff7bd 0 2px, transparent 3px),
        radial-gradient(circle at 85% 65%, #fff 0 2px, transparent 3px),
        radial-gradient(circle at 25% 78%, #ffeeb0 0 2px, transparent 3px),
        radial-gradient(circle at 55% 12%, #fff 0 1px, transparent 2px),
        radial-gradient(circle at 43% 88%, #fff 0 2px, transparent 3px);

    opacity:.8;

    animation:
        dustRotate 30s linear infinite;
}

@keyframes dustRotate{
    to{
        transform:
            translateZ(-1000px)
            rotateZ(360deg);
    }
}

.ring1{
    width:520px;
    height:520px;
    margin-left:-260px;
    margin-top:-260px;
    transform:translateZ(-1800px);
    box-shadow:
        0 0 40px rgba(255,220,100,.08),
        inset 0 0 40px rgba(255,220,100,.04);
    animation:ringPulse 7s ease-in-out infinite alternate;
}

.ring2{
    width:850px;
    height:850px;
    margin-left:-425px;
    margin-top:-425px;
    transform:translateZ(-2500px);
    opacity:.5;
    animation:ringPulse 10s ease-in-out infinite alternate-reverse;
}

@keyframes ringPulse{
    from{opacity:.15;scale:.94}
    to{opacity:.5;scale:1.05}
}
/* =========================
   CHỮ BAY - NHIỀU + ĐỔI MÀU
========================= */
.float-text{
    position:absolute;white-space:nowrap;
    font:700 clamp(20px,2.2vw,34px) 'Dancing Script',cursive;
    animation:riseFull 12s cubic-bezier(.22,.61,.36,1) forwards;
    filter:drop-shadow(0 0 7px currentColor) drop-shadow(0 0 14px currentColor);
    animation-timing-function:cubic-bezier(.22,.61,.36,1);
    z-index:10;pointer-events:none;will-change:transform,opacity,color;
}
@keyframes riseFull{

    /* =========================
       BẮT ĐẦU Ở GIỮA
    ========================= */
    0%{
        transform:
            translate3d(
                var(--startX),
                110vh,
                var(--depth)
            )
            rotate(-12deg)
            scale(.45);

        opacity:0;
        color:#ff5d9e;
    }

    /* Xuất hiện */
    8%{
        opacity:1;
        color:#ff5d9e;
    }

    /* Bắt đầu tỏa nhẹ */
    25%{
        transform:
            translate3d(
                var(--x25),
                78vh,
                var(--depth)
            )
            rotate(-5deg)
            scale(.75);

        opacity:1;
        color:#ff72b6;
    }

    /* Tỏa rộng hơn */
    45%{
        transform:
            translate3d(
                var(--x45),
                53vh,
                var(--depth)
            )
            rotate(4deg)
            scale(.95);

        opacity:1;
        color:#e978ff;
    }

    /* Tỏa mạnh ra ngoài */
    65%{
        transform:
            translate3d(
                var(--x65),
                30vh,
                var(--depth)
            )
            rotate(-4deg)
            scale(1.02);

        opacity:.95;
        color:#8f9dff;
    }

    /* Gần ra khỏi màn hình */
    82%{
        transform:
            translate3d(
                var(--x82),
                8vh,
                var(--depth)
            )
            rotate(5deg)
            scale(1.05);

        opacity:.8;
        color:#72dfff;
    }

    /* Bắt đầu biến mất */
    92%{
        transform:
            translate3d(
                var(--endX),
                -5vh,
                var(--depth)
            )
            rotate(7deg)
            scale(1.08);

        opacity:.35;
    }

    /* Biến mất hoàn toàn */
    100%{
        transform:
            translate3d(
                var(--endX),
                -18vh,
                var(--depth)
            )
            rotate(8deg)
            scale(1.1);

        opacity:0;
    }
}

/* =========================
   ẢNH BAY FULL VIỀN
========================= */
.photo{
    position:absolute;width:120px;height:150px;padding:5px;
    background:#fff;border-radius:10px;
    box-shadow:0 12px 30px #0009,0 0 20px rgba(255,255,255,.15);
    transform-style:preserve-3d;
    animation:photoFloat linear forwards;
    z-index:8;pointer-events:none;will-change:transform,opacity;
}
.photo img{
    width:100%;height:100%;object-fit:cover;border-radius:6px;display:block;
}
@keyframes photoFloat{
    0%{
        transform:
            translate3d(var(--photoX), var(--edgeY), -150px)
            rotateZ(var(--rotate))
            rotateY(-18deg)
            scale(1.15);
        opacity:0;
        filter:blur(0);
    }

    8%{
        opacity:.98;
    }

    25%{
        transform:
            translate3d(var(--photoMidX), 72vh, -450px)
            rotateZ(calc(var(--rotate) * .7))
            rotateY(-12deg)
            scale(1);
        opacity:.98;
    }

    45%{
        transform:
            translate3d(
                calc(var(--photoMidX) + 2vw),
                52vh,
                -850px
            )
            rotateZ(calc(var(--rotate) * .35))
            rotateY(5deg)
            scale(.82);
        opacity:.9;
    }

    65%{
        transform:
            translate3d(
                calc(var(--photoEndX) - 1vw),
                35vh,
                -1250px
            )
            rotateZ(calc(var(--rotate) * -.35))
            rotateY(15deg)
            scale(.58);
        opacity:.65;
    }

    82%{
        transform:
            translate3d(
                var(--photoEndX),
                15vh,
                -1700px
            )
            rotateZ(calc(var(--rotate) * -.6))
            rotateY(25deg)
            scale(.35);
        opacity:.35;
        filter:blur(2px);
    }

    100%{
        transform:
            translate3d(
                var(--photoEndX),
                -15vh,
                -2200px
            )
            rotateZ(var(--rotate))
            rotateY(35deg)
            scale(.08);
        opacity:0;
        filter:blur(7px);
    }
}

/* =========================
   HẠT / TIM / CÁNH HOA
========================= */
.heart,.petal,.light{
    position:absolute;pointer-events:none;animation:particle linear forwards;
}
.heart{font-size:22px}.petal{font-size:18px}
.light{
    width:5px;height:5px;border-radius:50%;background:#fff;
    box-shadow:0 0 15px 5px #ffe79a;
}
@keyframes particle{
    0%{transform:translateY(105vh) rotate(0) scale(.5);opacity:0}
    15%{opacity:1}
    100%{
        transform:translateY(-100px) translateX(var(--drift))
        rotate(300deg) scale(1.2);opacity:0;
    }
}

.lantern{
    position:absolute;width:32px;height:43px;
    border-radius:9px 9px 13px 13px;
    background:linear-gradient(#ffbd45,#e73732 65%,#9d1b32);
    box-shadow:0 0 22px #ff682d99;z-index:3;
    animation:lantern 5s ease-in-out infinite alternate;
}
.lantern:after{
    content:"";position:absolute;bottom:-6px;left:50%;
    width:9px;height:7px;transform:translateX(-50%);
    background:#ffd95a;box-shadow:0 0 12px #ffd95a;
}
.l1{left:9%;top:12%}.l2{left:27%;top:23%;transform:scale(.75);animation-delay:-2s}
.l3{right:28%;top:18%;transform:scale(.65);animation-delay:-1s}
@keyframes lantern{to{transform:translateY(-18px) rotate(4deg)}}

/* =========================
   NAV + THƯ
========================= */
.nav{position:absolute;right:16px;top:16px;z-index:20;display:flex;gap:9px}
.nav button{
    width:44px;height:44px;border-radius:50%;
    border:1px solid #ffffff44;background:#ffffff18;color:#fff;
    backdrop-filter:blur(8px);cursor:pointer;
}
/* =========================
   LÁ THƯ TRUNG THU
========================= */

.letter{
    position:absolute;
    z-index:30;
    left:50%;
    top:50%;

    width:min(88%,460px);
    max-height:78vh;
    overflow:auto;

    transform:
        translate(-50%,-50%)
        scale(.7)
        rotateX(-18deg)
        rotateZ(-2deg);

    opacity:0;
    pointer-events:none;

    /* giấy thư */
    background:
        radial-gradient(
            circle at 20% 20%,
            rgba(255,255,255,.9),
            transparent 25%
        ),
        linear-gradient(
            135deg,
            #fffdf5,
            #fff3dc
        );

    color:#714b42;

    border:2px solid #f1b6c9;
    border-radius:22px;

    padding:42px 30px 32px;

    box-shadow:
        0 30px 80px rgba(0,0,0,.55),
        0 0 35px rgba(255,150,200,.28),
        inset 0 0 25px rgba(255,190,210,.2);

    transition:
        .65s cubic-bezier(.2,.9,.2,1);

    backdrop-filter:blur(10px);
}

/* viền trang trí */
.letter::before{
    content:"";
    position:absolute;
    inset:10px;

    border:1px dashed #e7a9bb;
    border-radius:15px;

    pointer-events:none;
}

/* góc hoa */
.letter::after{
    content:"🌸";
    position:absolute;

    right:14px;
    top:8px;

    width:42px;
    height:42px;

    display:flex;
    align-items:center;
    justify-content:center;

    font-size:40px;

    filter:
        drop-shadow(0 0 7px rgba(255,100,170,.5));

    pointer-events:none;
}


/* Khi mở */

.letter.open{
    opacity:1;
    pointer-events:auto;

    transform:
        translate(-50%,-50%)
        scale(1)
        rotateX(0)
        rotateZ(0);
}


/* Tiêu đề */

.letter h2{
    position:relative;

    text-align:center;

    color:#e56c9b;

    font:
        700 34px
        'Dancing Script',
        cursive;

    margin:
        0 0 18px;

    text-shadow:
        0 2px 8px rgba(229,108,155,.2);
}


/* thêm dòng trang trí */

.letter h2::after{
    content:"♡  🌙  ♡";

    display:block;

    font:
        18px
        'Quicksand',
        sans-serif;

    color:#f2a2bc;

    margin-top:3px;

    letter-spacing:5px;
}


/* Nội dung */

.letter-body{
    position:relative;

    font:
        600 20px/1.75
        'Dancing Script',
        cursive;

    white-space:pre-wrap;

    min-height:100px;

    color:#704a4a;
}


/* =========================
   NÚT X ĐÓNG LÁ THƯ
========================= */

.close{
    position:absolute;

    right:14px;
    top:8px;

    width:42px;
    height:42px;

    display:flex;
    align-items:center;
    justify-content:center;

    border:0;
    background:transparent;

    color:#d85b88;

    font:
        700 19px/1
        Arial,
        sans-serif;

    cursor:pointer;

    z-index:51;

    /* Đưa X vào đúng tâm bông hoa */
    padding:0;

    text-shadow:
        0 1px 3px rgba(255,255,255,.9),
        0 0 5px rgba(180,60,110,.35);

    transition:
        transform .25s ease,
        color .25s ease;
}

.close:hover{
    transform:scale(1.18) rotate(90deg);
    color:#c63f72;
}

.close:active{
    transform:scale(.9);
}

/* Hover */
.close:hover{
    transform:rotate(90deg) scale(1.12);

    background:#ffd0df;

    box-shadow:
        0 4px 18px rgba(220,90,140,.4),
        0 0 20px rgba(255,130,180,.45);
}

/* Khi bấm */
.close:active{
    transform:scale(.9);
}

/* =========================
   SIDEBAR
========================= */
.sidebar{
    width:350px;background:#fff;color:#333;padding:18px;
    overflow:auto;z-index:40;box-shadow:-8px 0 30px #0006;
}
.sidebar h2{font-size:20px;margin-bottom:15px}
label.title{font-weight:700;font-size:13px;display:block;margin:14px 0 7px}
textarea,input[type=text],input[type=url]{
    width:100%;border:1px solid #ddd;border-radius:10px;
    padding:10px;outline:none;
}
textarea{resize:vertical;min-height:90px}
.btn{
    border:0;border-radius:10px;padding:10px 12px;
    background:#ffedf5;color:#ed3e78;font-weight:700;
    cursor:pointer;margin-top:8px;
}
.row{display:flex;gap:7px;margin-bottom:7px}.row input{flex:1}
.small{font-size:12px;color:#777}
#previews{display:flex;flex-wrap:wrap;gap:7px;margin-top:8px}
#previews img{width:54px;height:54px;object-fit:cover;border-radius:7px}
.toggle{
    display:flex;justify-content:space-between;align-items:center;
    margin:12px 0;padding:9px 0;border-bottom:1px solid #eee;
}
.switch{width:44px;height:24px;position:relative}
.switch input{display:none}
.slider{
    position:absolute;inset:0;background:#ccc;border-radius:20px;cursor:pointer;
}
.slider:before{
    content:"";position:absolute;width:18px;height:18px;
    left:3px;top:3px;background:#fff;border-radius:50%;transition:.25s;
}
.switch input:checked+.slider{background:#ff5d9e}
.switch input:checked+.slider:before{transform:translateX(20px)}

/* Tối ưu hiệu năng mobile: giảm blur, shadow và 3D nặng. */
@media(max-width:800px){
    #stars{opacity:.45}
    .cloud{filter:none;opacity:.28}
    .moon-main{box-shadow:0 0 28px rgba(255,229,139,.45)}
    .photo{
        box-shadow:0 5px 14px rgba(0,0,0,.35);
        transform-style:flat;
        will-change:transform,opacity;
        animation-name:photoFloatMobile;
    }
    .light{box-shadow:none}
    .nav button{backdrop-filter:none}
}

@keyframes photoFloatMobile{
    0%{transform:translate3d(var(--photoX),var(--edgeY),0) rotateZ(var(--rotate)) scale(1);opacity:0}
    10%{opacity:.95}
    50%{transform:translate3d(var(--photoMidX),50vh,0) rotateZ(var(--rotate)) scale(.78);opacity:.85}
    100%{transform:translate3d(var(--photoEndX),-15vh,0) rotateZ(var(--rotate)) scale(.35);opacity:0}
}

@media(max-width:800px){
    #app{display:block}
    .stage{height:100%;width:100%}

    /* Điện thoại chỉ dùng để XEM món quà. Không cho mở phần chỉnh sửa. */
    .sidebar{display:none !important}
    #settingsBtn{display:none !important}

    .moon-main{width:125px;height:125px;right:8%;top:7%}
    .photo{width:92px;height:118px}
    .float-text{font-size:22px}
    .nav{right:12px;top:12px}
}
@media(min-width:801px){.mobile-settings{display:none}}
/* =========================
   ĐIỀU KHIỂN GÓC NHÌN 3D
========================= */

#stage{
    perspective:1200px;
    overflow:hidden;
    touch-action:none;
    cursor:grab;
}

#stage.dragging{
    cursor:grabbing;
}

.world{
    position:absolute;
    inset:0;

    transform-style:preserve-3d;

    transform:
        translate3d(0,0,var(--zoom,0px))
        rotateX(var(--rotX,0deg))
        rotateY(var(--rotY,0deg));

    will-change:transform;

    /* Không gian sâu hơn */
    perspective:1800px;
}

.world .layer,
.world .moon-main,
.world .lantern{
    transform-style:preserve-3d;
}

/* Chữ bay chậm */
.float-text{
    animation-duration:22s;
}

/* Ảnh bay chậm */
.photo{
    animation-duration:28s !important;
}

/* =========================
   LƯU MÓN QUÀ + QR
========================= */
.gift-actions{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:14px}
.gift-actions .btn{width:100%}
.qr-modal{position:fixed;inset:0;z-index:100;display:flex;align-items:center;justify-content:center;background:#02030bcc;backdrop-filter:blur(10px);opacity:0;visibility:hidden;pointer-events:none;transition:.25s}
.qr-modal.open{opacity:1;visibility:visible;pointer-events:auto}
.qr-card{width:min(92vw,390px);background:linear-gradient(145deg,#fff,#fff7fb);color:#222;border-radius:24px;padding:22px;text-align:center;box-shadow:0 20px 70px #0008}
.qr-card h3{margin-bottom:8px;color:#d63378}
.qr-card p{font-size:13px;line-height:1.5;color:#666;margin:8px 0 14px}
#qrCode{display:flex;justify-content:center;align-items:center;background:#fff;padding:12px;border-radius:14px;min-height:230px}
#qrCode img,#qrCode canvas{max-width:100%;height:auto!important}
.qr-actions{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:14px}
.storage-box{margin-top:14px;padding:12px;border:1px dashed #ffc1d8;border-radius:14px;background:#fff8fb}
.storage-box h3{margin:0 0 7px;font-size:14px;color:#d63378}
.storage-box input{margin-top:6px}
.storage-status{font-size:12px;color:#777;line-height:1.45;margin-top:7px}
.storage-status.ok{color:#16834b}
.storage-status.err{color:#c62828}
.file-upload-row{display:grid;grid-template-columns:1fr auto;gap:7px;align-items:center;margin-top:7px}
.file-upload-row .btn{margin-top:0}

@media(max-width:520px){.gift-actions{grid-template-columns:1fr}.qr-card{padding:18px}}

/* ===== HELLO KITTY BIRTHDAY • HỒNG PASTEL NHẠT ===== */
/* Nơ Hello Kitty bay chậm trong nền */
.kitty-bow{position:absolute;z-index:3;pointer-events:none;font-size:clamp(26px,4vw,48px);opacity:.7;filter:drop-shadow(0 5px 10px rgba(218,105,157,.22));animation:bowFloat 7s ease-in-out infinite alternate}
.bow-one{left:9%;top:18%;transform:rotate(-15deg)}
.bow-two{right:15%;top:42%;font-size:clamp(20px,3vw,36px);animation-delay:-2.5s}
.bow-three{left:25%;bottom:13%;font-size:clamp(18px,2.5vw,30px);animation-delay:-4s}
@keyframes bowFloat{from{translate:0 0;rotate:-12deg}to{translate:12px -18px;rotate:12deg}}

:root{--pink:#f4a6c8;--blue:#fbd9e8;--gold:#ffeaf2;--night:#fff3f8}
html,body{background:#fff1f7;color:#8b4568}
body{background:radial-gradient(ellipse at 18% 18%,rgba(255,255,255,.98),transparent 38%),radial-gradient(ellipse at 82% 25%,rgba(255,214,233,.7),transparent 38%),linear-gradient(145deg,#fffafd 0%,#ffedf5 48%,#fbdbea 100%);color:#8b4568}
#app{background:transparent}.stage,.world{background:transparent!important}.stage{perspective:1400px}.world{perspective:1800px;transform-style:preserve-3d}.layer{transform-style:preserve-3d!important;perspective:1800px}
#textLayer{overflow:visible;transform-style:preserve-3d;z-index:7;pointer-events:none}
.float-text{position:absolute;left:0;top:0;white-space:nowrap;color:#f28ab8;font-family:'Dancing Script',cursive;font-weight:700;letter-spacing:.2px;-webkit-text-stroke:.35px rgba(255,255,255,.9);text-shadow:0 1px 0 #fff,0 3px 0 #ffd2e5,0 7px 16px rgba(197,87,141,.24),0 0 18px rgba(255,145,193,.68);filter:drop-shadow(0 0 8px rgba(255,130,190,.5));transform-style:preserve-3d;backface-visibility:hidden;animation-name:riseFull;animation-timing-function:linear;animation-fill-mode:forwards;will-change:transform,opacity;z-index:10;pointer-events:none}
@keyframes riseFull{0%{transform:translate3d(var(--startX),110vh,calc(var(--depth) - 180px)) rotateY(-22deg) rotateZ(-12deg) scale(.45);opacity:0;color:#f7a0c7}8%{opacity:1;color:#f18bb9}25%{transform:translate3d(var(--x25),78vh,var(--depth)) rotateY(14deg) rotateZ(-5deg) scale(.75);opacity:1;color:#f7a0c7}45%{transform:translate3d(var(--x45),53vh,calc(var(--depth) + 100px)) rotateY(-18deg) rotateZ(4deg) scale(.95);opacity:1;color:#ec86b8}65%{transform:translate3d(var(--x65),30vh,var(--depth)) rotateY(18deg) rotateZ(-4deg) scale(1.02);opacity:.95;color:#d99acb}82%{transform:translate3d(var(--x82),8vh,calc(var(--depth) - 80px)) rotateY(-12deg) rotateZ(5deg) scale(1.05);opacity:.8;color:#f4a0c8}92%{transform:translate3d(var(--endX),-5vh,var(--depth)) rotateY(10deg) rotateZ(7deg) scale(1.08);opacity:.35}100%{transform:translate3d(var(--endX),-18vh,calc(var(--depth) + 120px)) rotateY(24deg) rotateZ(8deg) scale(1.1);opacity:0}}
#stars{opacity:.25}.cloud,.star-group{opacity:.35;filter:hue-rotate(300deg) saturate(.4)}.bg-heart{color:#f6a3ca;text-shadow:0 0 14px #ffd0e5}
.sidebar{display:flex!important;flex-direction:column;gap:12px;background:rgba(255,249,252,.97)!important;color:#8b4568;border:1px solid #f8c6dc!important;border-radius:22px;box-shadow:0 0 35px rgba(255,139,190,.18)}
.sidebar h2,.sidebar .title,.title{color:#d86f9f}.sidebar label,.sidebar p{color:#985878}.btn,button{border-color:#f7bfd8}.btn{background:linear-gradient(135deg,#ffe4ef,#f7bad5)!important;color:#85445f!important;box-shadow:0 5px 15px rgba(236,111,166,.14)}input,textarea{background:#fffafd!important;color:#84415f!important;border-color:#ffd0e3!important}.photo{border-color:#fff!important;box-shadow:0 8px 24px rgba(213,91,146,.2)}


/* ===== TỐI ƯU ĐIỆN THOẠI: nhẹ, mượt, dễ nhìn ===== */
html, body { min-height:100%; overscroll-behavior:none; -webkit-tap-highlight-color:transparent; }
#app, .stage, #stage, .world { width:100%; height:100%; min-height:0; }
#stage { touch-action:pan-y; }
#stars { pointer-events:none; }
@media (max-width:800px) {
  body { font-size:14px; }
  .world, .layer { transform-style:preserve-3d; }
  .cloud, .star-group { filter:none !important; opacity:.2 !important; }
  .moon-main { width:clamp(76px,22vw,112px); height:clamp(76px,22vw,112px); box-shadow:0 0 18px rgba(255,190,220,.35) !important; }
  .float-text {
    font-size:clamp(18px,4.8vw,24px) !important;
    letter-spacing:0 !important;
    -webkit-text-stroke:0 !important;
    text-shadow:0 1px 0 #fff, 0 3px 7px rgba(207,102,153,.2), 0 0 8px rgba(255,170,205,.4) !important;
    filter:none !important;
    animation-name:riseMobile !important;
    backface-visibility:hidden;
  }
  @keyframes riseMobile {
    0% { transform:translate3d(var(--startX),108vh,calc(var(--depth)*.45)) rotateY(-12deg) rotateZ(-7deg) scale(.62); opacity:0; }
    12% { opacity:1; }
    50% { transform:translate3d(var(--x45),50vh,var(--depth)) rotateY(8deg) rotateZ(2deg) scale(.88); opacity:.95; }
    82% { transform:translate3d(var(--x82),12vh,calc(var(--depth)*.5)) rotateY(-7deg) rotateZ(-2deg) scale(1); opacity:.72; }
    100% { transform:translate3d(var(--endX),-18vh,0) rotateY(10deg) rotateZ(4deg) scale(1.04); opacity:0; }
  }
  .photo { box-shadow:0 4px 10px rgba(180,85,130,.16) !important; filter:none !important; }
  .heart, .petal, .light { filter:none !important; text-shadow:none !important; }
  .kitty-bow { filter:none !important; opacity:.48; }
  .btn, button { min-height:42px; }
}
@media (prefers-reduced-motion: reduce) {
  .cloud, .star-group, .kitty-bow, .moon-main { animation:none !important; }
}

</style>
</head>

<body>

<!-- =========================
     APP
========================= -->
<div id="app">

    <div class="stage" id="stage">

    <!-- KHÔNG GIAN 3D -->
    <div class="world" id="world">

    <canvas id="stars"></canvas>


    <!-- ☁️ Mây phía sau -->
    <div class="cloud cloud1"></div>
    <div class="cloud cloud2"></div>
    <div class="cloud cloud3"></div>

    <!-- ✨ Các cụm sao -->
    <div class="star-group sg1">✦</div>
    <div class="star-group sg2">✧</div>
    <div class="star-group sg3">✦</div>
    <div class="star-group sg4">✧</div>
    <div class="star-group sg5">✦</div>


    <!-- 💕 Trái tim phát sáng phía xa -->
    <div class="bg-heart bh1">♡</div>
    <div class="bg-heart bh2">♡</div>
    <div class="bg-heart bh3">♡</div>

    <!-- Nơ sinh nhật pastel -->
    <div class="kitty-bow bow-one">🎀</div>
    <div class="kitty-bow bow-two">🎀</div>
    <div class="kitty-bow bow-three">🎀</div>

    <!-- Nội dung bay -->
    <div class="layer" id="textLayer"></div>
    <div class="layer" id="photoLayer"></div>
    <div class="layer" id="particleLayer"></div>

</div>


    <div class="nav">
            <button id="musicBtn" title="Nhạc">🔊</button>
            <button id="settingsBtn" class="mobile-settings" title="Cài đặt">⚙️</button>
        </div>



    </div>


    <!-- SIDEBAR -->
    <aside class="sidebar" id="sidebar">

        <h2>🎀 Quà sinh nhật Hello Kitty</h2>

        <label class="title">✨ Lời chúc bay</label>
        <div id="textInputs"></div>
        <button class="btn" id="addText">＋ Thêm câu</button>

        <label class="title">🖼️ Ảnh kỷ niệm</label>
        <input id="photoInput" type="file" accept="image/*" multiple>
        <div id="previews"></div>

        

        <label class="title">🎵 Nhạc nền</label>
        <input id="musicUrl" type="url" value="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=lofi-study-112191.mp3" placeholder="URL file MP3">
        <button class="btn" id="loadMusic">Đổi nhạc từ URL</button>
        

        

        

        <div class="toggle">
            <span>🖼️ Bật ảnh bay</span>
            <label class="switch">
                <input id="photoToggle" type="checkbox" checked>
                <span class="slider"></span>
            </label>
        </div>

        <div class="toggle">
            <span>💖 Bật hiệu ứng tim</span>
            <label class="switch">
                <input id="particleToggle" type="checkbox" checked>
                <span class="slider"></span>
            </label>
        </div>



        <p class="small">
            Chọn lời chúc, ảnh và nhạc để tạo không gian sinh nhật hồng pastel dành tặng người ấy nhé 💗
        </p>

    </aside>
</div>

<audio id="audio" loop></audio>




<script>
/* =========================
   BIẾN
========================= */

const $ = s => document.querySelector(s);

const textLayer = $("#textLayer");
const photoLayer = $("#photoLayer");
const particleLayer = $("#particleLayer");


let texts = [
    "Chúc mừng sinh nhật em 🎂💗",
    "Iu em nhiều lắm",
    "Em là cô gái đáng yêu nhất 🎀",
    "Chúc em luôn hạnh phúc 💕",
    "Chúc em luôn rạng rỡ ✨",
    "Thương em nhiều lắm",
    "Happy Birthday, my love 🎀"
];

let photos = [];

let audioOn = false;
let typeTimer = null;


/* =========================
   ẢNH MẶC ĐỊNH
========================= */

const samplePhotos = [
    "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=500",
    "https://images.unsplash.com/photo-1517841905240-472988babdf9?w=500"
];

photos = [...samplePhotos];


/* =========================
   CHỮ BAY
========================= */

function renderTextInputs(){

    $("#textInputs").innerHTML = "";

    texts.forEach((t,i)=>{

        const d = document.createElement("div");

        d.className = "row";

        d.innerHTML = `
            <input type="text" value="${escapeHtml(t)}">
            <button class="btn">×</button>
        `;

        d.querySelector("input").oninput =
            e => texts[i] = e.target.value;

        d.querySelector("button").onclick = ()=>{

            texts.splice(i,1);

            renderTextInputs();
        };

        $("#textInputs").appendChild(d);
    });
}


function escapeHtml(s){

    return s.replace(
        /[&<>"']/g,
        m => ({
            "&":"&amp;",
            "<":"&lt;",
            ">":"&gt;",
            '"':"&quot;",
            "'":"&#39;"
        }[m])
    );
}


$("#addText").onclick = ()=>{

    texts.push("Lời chúc mới 💕");

    renderTextInputs();
};


/* =========================
   PREVIEW ẢNH + NÚT XÓA
========================= */

function renderPreviews(){

    $("#previews").innerHTML = "";

    photos.forEach((src, i)=>{

        const box = document.createElement("div");

        box.style.position = "relative";
        box.style.width = "54px";
        box.style.height = "54px";

        const im = new Image();

        im.src = src;

        im.style.width = "54px";
        im.style.height = "54px";
        im.style.objectFit = "cover";
        im.style.borderRadius = "7px";
        im.style.display = "block";

        /* NÚT XÓA */
        const del = document.createElement("button");

        del.textContent = "×";

        del.style.position = "absolute";
        del.style.right = "-6px";
        del.style.top = "-6px";

        del.style.width = "20px";
        del.style.height = "20px";

        del.style.padding = "0";
        del.style.margin = "0";

        del.style.border = "2px solid white";
        del.style.borderRadius = "50%";

        del.style.background = "#ff4f81";
        del.style.color = "white";

        del.style.font = "bold 14px Arial";
        del.style.lineHeight = "16px";

        del.style.cursor = "pointer";
        del.style.zIndex = "10";

        del.title = "Xóa ảnh";

        /* BẤM X → XÓA ẢNH */
        del.onclick = () => {

            photos.splice(i, 1);

            renderPreviews();
        };

        box.appendChild(im);
        box.appendChild(del);

        $("#previews").appendChild(box);
    });
}


/* =========================
   CHỌN ẢNH
========================= */

/* =========================
   CHỌN ẢNH - LƯU CỤC BỘ
========================= */
$("#photoInput").onchange = e => {
    const files = [...e.target.files];
    files.forEach(file => {
        if(!file.type.startsWith("image/")) return;
        const reader = new FileReader();
        reader.onload = () => { photos.push(reader.result); renderPreviews(); };
        reader.readAsDataURL(file);
    });
    e.target.value = "";
};

/* =========================
   SPAWN CHỮ
   NHIỀU HƠN + FULL MÀN HÌNH
========================= */

function spawnText(){

    if(!texts.length) return;
    const maxLiveTexts = isMobileDevice ? 9 : 18;
    if (textLayer.childElementCount >= maxLiveTexts) return;

    const t = document.createElement("div");

    t.className = "float-text";

    t.textContent =
        texts[Math.floor(Math.random()*texts.length)];

    /* =========================
       VỊ TRÍ XUẤT HIỆN
       TOÀN BỘ MÀN HÌNH
    ========================= */

    const startX =
        -5 + Math.random()*110;

    /* =========================
       ĐIỂM KẾT THÚC
       Vẫn bay lên nhưng X thay đổi nhẹ
    ========================= */

    const endX =
        startX + (Math.random()*30 - 15);

    /* =========================
       CÁC ĐIỂM TRUNG GIAN
    ========================= */

    const x25 =
        startX + (endX-startX)*0.25;

    const x45 =
        startX + (endX-startX)*0.45;

    const x65 =
        startX + (endX-startX)*0.65;

    const x82 =
        startX + (endX-startX)*0.82;

    /* =========================
       ĐỘ SÂU 3D
       LÙI RA XA
    ========================= */

    const depth = 100 - Math.random()*900;

    /* =========================
       GÁN BIẾN CSS
    ========================= */

    t.style.setProperty(
        "--startX",
        startX + "vw"
    );

    t.style.setProperty(
        "--x25",
        x25 + "vw"
    );

    t.style.setProperty(
        "--x45",
        x45 + "vw"
    );

    t.style.setProperty(
        "--x65",
        x65 + "vw"
    );

    t.style.setProperty(
        "--x82",
        x82 + "vw"
    );

    t.style.setProperty(
        "--endX",
        endX + "vw"
    );

    t.style.setProperty(
        "--depth",
        depth + "px"
    );

    /* =========================
       THỜI GIAN BAY
    ========================= */

    const duration = isMobileDevice
        ? 13 + Math.random()*4
        : 16 + Math.random()*8;

    t.style.animationDuration =
        duration + "s";

    /* =========================
       THÊM VÀO MÀN HÌNH
    ========================= */

    textLayer.appendChild(t);

    /* =========================
       TỰ XÓA
    ========================= */

    setTimeout(
        ()=>{
            t.remove();
        },
        (duration + 1)*1000
    );
}

    
/* =========================
   SPAWN ẢNH
   FULL VIỀN
========================= */

function spawnPhoto(){

    if(
        !$("#photoToggle").checked ||
        !photos.length
    ) return;

    const p = document.createElement("div");

    p.className = "photo";

    const img = document.createElement("img");

    img.src =
        photos[
            Math.floor(
                Math.random()*photos.length
            )
        ];

    img.alt = "";

    p.appendChild(img);


    let startX;
    let endX;
    let midX;

    const side = Math.random();

    if(side < .25){

        startX = -15;
        midX = Math.random()*35-10;
        endX = Math.random()*50;

    }else if(side < .5){

        startX = 85 + Math.random()*20;
        midX = 50 + Math.random()*40;
        endX = 50 + Math.random()*50;

    }else{

        startX = Math.random()*100;
        midX = Math.random()*100;
        endX = Math.random()*100;
    }

    if(side >= .75){

        startX = Math.random()<.5 ? -10 : 95;
        midX = Math.random()*100;
        endX = Math.random()<.5 ? -10 : 95;
    }


    p.style.left = "0";

    p.style.setProperty(
        "--photoX",
        startX+"vw"
    );

    p.style.setProperty(
        "--photoMidX",
        midX+"vw"
    );

    p.style.setProperty(
        "--photoEndX",
        endX+"vw"
    );
/* Độ sâu của ảnh */
const photoDepth =
    Math.random()*2400 - 1400;

p.style.setProperty(
    "--photoDepth",
    photoDepth + "px"
);

    p.style.setProperty(
        "--rotate",
        (Math.random()*30-15)+"deg"
    );


    const scale = .75 + Math.random()*.5;
// Đưa ảnh xuất phát từ nhiều phía của rìa màn hình
const edgeSide = Math.floor(Math.random() * 4);

let edgeX, edgeY;

if(edgeSide === 0){
    edgeX = -15 - Math.random()*20;
    edgeY = Math.random()*110;
}else if(edgeSide === 1){
    edgeX = 105 + Math.random()*20;
    edgeY = Math.random()*110;
}else if(edgeSide === 2){
    edgeX = Math.random()*110;
    edgeY = -15 - Math.random()*20;
}else{
    edgeX = Math.random()*110;
    edgeY = 105 + Math.random()*20;
}

p.style.setProperty("--photoX", edgeX + "vw");
p.style.setProperty("--edgeY", edgeY + "vh");
    p.style.width =
        (120*scale)+"px";

    p.style.height =
        (150*scale)+"px";

    const duration =
    25 + Math.random()*10;

p.style.animationDuration =
    duration + "s";

photoLayer.appendChild(p);

setTimeout(
    ()=>p.remove(),
    (duration + 3) * 1000
);
}


/* =========================
   PARTICLE
========================= */

function spawnParticle(){

    if(!$("#particleToggle").checked) return;
    const maxParticles = isMobileDevice ? 12 : 28;
    if (particleLayer.childElementCount >= maxParticles) return;

    const e = document.createElement("div");
    const r = Math.random();

    e.className =
        r < .45
        ? "heart"
        : r < .72
        ? "petal"
        : "light";

    e.textContent =
        e.className === "heart"
        ? (Math.random()<.5 ? "💗" : "❤️")
        : e.className === "petal"
        ? "🎀"
        : "";

    e.style.left =
        Math.random()*100+"%";

    e.style.setProperty(
        "--drift",
        (Math.random()*180-90)+"px"
    );

    e.style.animationDuration =
        (5+Math.random()*6)+"s";

    particleLayer.appendChild(e);

    setTimeout(
        ()=>e.remove(),
        12000
    );
}


/* =========================
   HIỆU NĂNG ĐIỆN THOẠI
   Giảm số lượng phần tử động để máy yếu không bị lag.
========================= */
const isMobileDevice = window.matchMedia("(max-width: 800px)").matches ||
    /Android|iPhone|iPad|iPod|Mobile/i.test(navigator.userAgent);

/* NHIỀU CHỮ */
const initialTextCount = isMobileDevice ? 4 : 12;
const textIntervalMs = isMobileDevice ? 2100 : 850;
const photoIntervalMs = isMobileDevice ? 5200 : 2200;
const particleIntervalMs = isMobileDevice ? 1900 : 750;

for(let i = 0; i < initialTextCount; i++){
    setTimeout(spawnText, i * (isMobileDevice ? 450 : 220));
}

setInterval(spawnText, textIntervalMs);
setInterval(spawnPhoto, photoIntervalMs);
setInterval(spawnParticle, particleIntervalMs);


/* =========================
   SETTINGS MOBILE
========================= */
const settingsBtn = $("#settingsBtn");
if(settingsBtn){ settingsBtn.onclick = () => $("#sidebar").classList.toggle("open"); }

/* =========================
   NHẠC
========================= */

function loadAudio(){

    $("#audio").src =
        $("#musicUrl").value.trim();

    $("#audio").load();
}


$("#loadMusic").onclick = ()=>{

    loadAudio();

    audioOn = false;

    $("#musicBtn").textContent = "🔇";
};


$("#musicBtn").onclick = async ()=>{

    if(!$("#audio").src){

        loadAudio();
    }

    if(audioOn){

        $("#audio").pause();

        audioOn = false;

        $("#musicBtn").textContent = "🔇";

    }else{

        try{

            await $("#audio").play();

            audioOn = true;

            $("#musicBtn").textContent = "🔊";

        }catch{

            alert(
                "Trình duyệt đang chặn nhạc. Hãy bấm lại nút nhạc."
            );
        }
    }
};


/* =========================
   SAO
========================= */

function stars(canvas){

    const c = canvas;
    const x = c.getContext("2d");

    const pts = [];


    function resize(){

        c.width = innerWidth;
        c.height = innerHeight;
    }


    resize();

    addEventListener(
        "resize",
        resize
    );


    const starCount = isMobileDevice ? 70 : 180;

    for(let i=0;i<starCount;i++){

        pts.push({
            x:Math.random(),
            y:Math.random(),
            r:Math.random()*1.8,
            a:Math.random(),
            v:Math.random()*.008
        });
    }


    function draw(){

        if(document.hidden) return;

        x.clearRect(
            0,
            0,
            c.width,
            c.height
        );


        for(const p of pts){

            p.a += p.v;

            if(
                p.a > 1 ||
                p.a < .1
            ){

                p.v *= -1;
            }


            x.globalAlpha = p.a;

            x.fillStyle = "#fff";

            x.beginPath();

            x.arc(
                p.x*c.width,
                p.y*c.height,
                p.r,
                0,
                7
            );

            x.fill();
        }


        requestAnimationFrame(draw);
    }


    draw();
    document.addEventListener("visibilitychange", () => {
        if (!document.hidden) requestAnimationFrame(draw);
    }, { passive:true });
}


stars($("#stars"));

/* =========================
   ĐIỀU KHIỂN GÓC NHÌN
   CHUỘT + CẢM ỨNG
========================= */

const stage = document.getElementById("stage");
const world = document.getElementById("world");

let rotX = 0;
let rotY = 0;
let zoom = 0;

let dragging = false;

let lastX = 0;
let lastY = 0;

const MAX_ROT_X = 80;
const MAX_ROT_Y = 360;

const MIN_ZOOM = -350;
const MAX_ZOOM = 350;


/* Cập nhật góc nhìn */
function updateView(){

    world.style.setProperty(
        "--rotX",
        rotX + "deg"
    );

    world.style.setProperty(
        "--rotY",
        rotY + "deg"
    );

    world.style.setProperty(
        "--zoom",
        zoom + "px"
    );
}


/* =========================
   KÉO CHUỘT
========================= */

stage.addEventListener("pointerdown", e => {

    if(
        e.target.closest(".nav") ||
        e.target.closest(".letter") ||
        e.target.closest(".sidebar")
    ){
        return;
    }

    dragging = true;

    lastX = e.clientX;
    lastY = e.clientY;

    stage.classList.add("dragging");

    stage.setPointerCapture(e.pointerId);
});


stage.addEventListener("pointermove", e => {

    if(!dragging) return;

    const dx =
        e.clientX - lastX;

    const dy =
        e.clientY - lastY;

    lastX = e.clientX;
    lastY = e.clientY;

    /* Trái / phải */
    rotY += dx * 0.35;

    /* Lên / xuống */
    rotX -= dy * 0.30;

    /* Xoay trái/phải tự do */
rotY %= 360;

    rotY =
        Math.max(
            -MAX_ROT_Y,
            Math.min(MAX_ROT_Y,rotY)
        );

    updateView();
});


function stopDragging(){

    dragging = false;

    stage.classList.remove("dragging");
}


stage.addEventListener(
    "pointerup",
    stopDragging
);

stage.addEventListener(
    "pointercancel",
    stopDragging
);


/* =========================
   LĂN CHUỘT = ZOOM
========================= */

stage.addEventListener("wheel",e=>{

    e.preventDefault();

    zoom -= e.deltaY * 0.35;

    zoom =
        Math.max(
            MIN_ZOOM,
            Math.min(MAX_ZOOM,zoom)
        );

    updateView();

},{
    passive:false
});


/* =========================
   ĐIỆN THOẠI - CHỤM 2 NGÓN
========================= */

let touchDistance = null;


stage.addEventListener(
    "touchstart",
    e=>{

        if(e.touches.length === 2){

            const dx =
                e.touches[0].clientX -
                e.touches[1].clientX;

            const dy =
                e.touches[0].clientY -
                e.touches[1].clientY;

            touchDistance =
                Math.hypot(dx,dy);
        }

    },{
        passive:false
    }
);


stage.addEventListener(
    "touchmove",
    e=>{

        if(e.touches.length !== 2)
            return;

        e.preventDefault();

        const dx =
            e.touches[0].clientX -
            e.touches[1].clientX;

        const dy =
            e.touches[0].clientY -
            e.touches[1].clientY;

        const distance =
            Math.hypot(dx,dy);

        if(touchDistance !== null){

            const change =
                distance - touchDistance;

            zoom += change * 1.2;

            zoom =
                Math.max(
                    MIN_ZOOM,
                    Math.min(MAX_ZOOM,zoom)
                );

            updateView();
        }

        touchDistance = distance;

    },{
        passive:false
    }
);


stage.addEventListener(
    "touchend",
    e=>{

        if(e.touches.length < 2){

            touchDistance = null;
        }

    },{
        passive:false
    }
);


/* Góc nhìn ban đầu */
updateView();
/* =========================
   KHỞI TẠO
========================= */

renderTextInputs();
renderPreviews();
loadAudio();
</script>

</body>
</html>
