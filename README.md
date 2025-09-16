<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Happy Birthday — For Anuuuuuu 💖</title>
    <style>
        :root {
            --glass: rgba(255, 255, 255, 0.06);
            --accent: #ff6f91;
            --accent2: #ff9a9e;
            --text: #fff;
            --card-bg: rgba(255, 255, 255, 0.06);
            --shadow: 0 8px 30px rgba(0, 0, 0, 0.28);
            --radius: 18px;
        }

        * {
            box-sizing: border-box
        }

        html,
        body {
            height: 100%
        }

        body {
            margin: 0;
            font-family: "Segoe UI", "Noto Sans", system-ui, -apple-system, Roboto, "Helvetica Neue", Arial;
            background: linear-gradient(135deg, #1f2330 0%, #3a2740 50%, #6b3b58 100%);
            color: var(--text);
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            overflow-x: hidden;
            line-height: 1.65;
        }

        /* Top nav / ToC */
        #toc {
            position: fixed;
            top: 18px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1200;
            background: linear-gradient(90deg, rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.25));
            padding: 10px 18px;
            border-radius: 999px;
            box-shadow: var(--shadow);
            display: flex;
            gap: 10px;
            align-items: center;
            backdrop-filter: blur(6px) saturate(120%);
        }

        #toc a {
            color: var(--text);
            text-decoration: none;
            font-weight: 600;
            font-size: 14px;
            padding: 8px 12px;
            border-radius: 999px;
            transition: all .22s ease;
            opacity: 0.95;
        }

        #toc a:hover {
            transform: translateY(-3px);
            color: #ffe9f0;
            text-shadow: 0 4px 20px rgba(255, 105, 135, 0.12)
        }

        /* Side mini TOC for quick nav */
        #side-toc {
            position: fixed;
            right: 18px;
            top: 110px;
            width: 260px;
            max-height: 66vh;
            overflow: auto;
            padding: 12px;
            border-radius: 12px;
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.03), rgba(255, 255, 255, 0.02));
            box-shadow: var(--shadow);
            backdrop-filter: blur(6px);
            z-index: 1100;
        }

        #side-toc h4 {
            margin: 6px 0 10px 0;
            font-size: 14px;
            color: #fff8;
            text-align: center
        }

        #side-toc ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            flex-direction: column;
            gap: 6px
        }

        #side-toc li a {
            color: #fff;
            text-decoration: none;
            font-size: 13px;
            padding: 8px 10px;
            border-radius: 10px;
            display: block;
            transition: background .18s;
        }

        #side-toc li a:hover {
            background: rgba(255, 255, 255, 0.03)
        }

        /* Page sections */
        main {
            padding-top: 80px
        }

        section {
            min-height: 100vh;
            padding: 72px 10% 90px 10%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: left;
            gap: 28px;
            position: relative;
        }

        .card {
            width: 100%;
            max-width: 980px;
            background: var(--card-bg);
            border-radius: var(--radius);
            padding: 38px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(6px) saturate(120%);
        }

        h1,
        h2 {
            margin: 0 0 14px 0;
            font-weight: 700;
        }

        h1 {
            font-size: 34px;
            letter-spacing: 0.4px
        }

        h2 {
            font-size: 26px
        }

        p {
            font-size: 17px;
            color: #fffefe;
            margin-bottom: 18px;
            white-space: pre-wrap;
        }

        .lead {
            font-size: 18px;
            color: #fff;
            opacity: 0.98;
            margin-bottom: 18px
        }

        .small {
            font-size: 14px;
            color: #fff8
        }

        .accent {
            display: inline-block;
            padding: 6px 12px;
            border-radius: 999px;
            background: linear-gradient(90deg, var(--accent), var(--accent2));
            color: #320018;
            font-weight: 700;
            margin-left: 6px;
        }

        .footer-nav {
            margin-top: 18px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .btn {
            background: rgba(255, 255, 255, 0.04);
            padding: 10px 14px;
            border-radius: 10px;
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            border: 1px solid rgba(255, 255, 255, 0.03);
        }

        .btn:hover {
            transform: translateY(-3px)
        }

        /* Floating hearts */
        .heart {
            position: fixed;
            width: 18px;
            height: 18px;
            transform: rotate(45deg);
            top: 110%;
            opacity: 0.92;
            z-index: 800;
            pointer-events: none;
            background: linear-gradient(180deg, #ff7aa2, #ff5a87);
            border-radius: 2px;
            box-shadow: 0 8px 30px rgba(255, 105, 135, 0.12);
        }

        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: inherit;
            top: -9px;
            left: 0;
        }

        .heart:after {
            left: -9px;
            top: 0
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(45deg);
                opacity: 0.95
            }

            100% {
                transform: translateY(-120vh) rotate(45deg);
                opacity: 0
            }
        }

        /* Section backgrounds (subtle variety) */
        section:nth-of-type(odd) {
            background: linear-gradient(135deg, #2b1530 0%, #4a2740 100%);
        }

        section:nth-of-type(even) {
            background: linear-gradient(135deg, #23192a 0%, #44303f 100%);
        }

        /* Responsive tweaks */
        @media (max-width:920px) {
            #side-toc {
                display: none
            }

            section {
                padding: 60px 6% 80px 6%
            }

            h1 {
                font-size: 28px
            }

            h2 {
                font-size: 22px
            }
        }
    </style>
</head>

<body>
    <!-- Top quick links -->
    <div id="toc" aria-hidden="false">
        <a href="#page1">Home</a>
        <a href="#page2">Letters</a>
        <a href="#page9">Memories</a>
        <a href="#page13">Promises</a>
        <a href="#page17">Dreams</a>
        <a href="#page20">Final</a>
    </div>

    <!-- Side mini table of contents -->
    <aside id="side-toc" aria-hidden="false">
        <h4>Chapters — Jump to a page</h4>
        <ul>
            <li><a href="#page1">1 • Welcome</a></li>
            <li><a href="#page2">2 • Morning Letter</a></li>
            <li><a href="#page3">3 • Midday Letter</a></li>
            <li><a href="#page4">4 • Night Letter</a></li>
            <li><a href="#page5">5 • Confession — Missing You</a></li>
            <li><a href="#page6">6 • Confession — Little Things</a></li>
            <li><a href="#page7">7 • Confession — Fears & Hopes</a></li>
            <li><a href="#page8">8 • Memory — First Message</a></li>
            <li><a href="#page9">9 • Memory — Call That Changed Me</a></li>
            <li><a href="#page10">10 • Reasons — Your Voice</a></li>
            <li><a href="#page11">11 • Reasons — Your Care</a></li>
            <li><a href="#page12">12 • Reasons — Your Strength</a></li>
            <li><a href="#page13">13 • Promise — Short Term</a></li>
            <li><a href="#page14">14 • Promise — When We Meet</a></li>
            <li><a href="#page15">15 • Promise — Long Term</a></li>
            <li><a href="#page16">16 • Gratitude</a></li>
            <li><a href="#page17">17 • Dream — Little Days</a></li>
            <li><a href="#page18">18 • Dream — Big Plans</a></li>
            <li><a href="#page19">19 • Soft Confession — Jealousy & Care</a></li>
            <li><a href="#page20">20 • Final Wishes</a></li>
        </ul>
    </aside>

    <main>
        <!-- 1: Welcome -->
        <section id="page1" aria-labelledby="title1">
            <div class="card">
                <h1 id="title1">Happy Birthday, <span class="accent">Anumehaaaaa</span></h1>
                <p class="lead">
                    Aaj ka din bahut khaas hai — tumhara din. Dooriyon ke bawajood main chahta hoon ke tumhe lage main
                    tumhare bilkul kareeb hoon. Yeh site maine isliye banaya taaki tum jab bhi chaho, kabooliyat ke
                    saath, mere emotions ko padh sako; har paragraph mere dil ka ek tukda hai jo tumhare liye ghar
                    bhejne jaisi feeling de.
                </p>

                <p>
                    Main tumhare liye itna bolna chahta hoon ki kabhi kabhi lafz kam pad jaate hain. Yeh pages tumhare
                    liye — lamhon ka ek collection hain: late-night calls, silly memes, unplanned video calls, cute
                    gussa aur pyare se "okay let's patch up" messages. Jab tum inhe padhogi, har sentence mein mera sach
                    milega.
                </p>

                <p>
                    <!-- Replace [Her Name] with her actual name before sharing. Aur haan — agar tum chaho main har paragraph mein tumhare personal memories bhi daal dunga (date/place details) — bas mujhe bata dena. -->
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page2">Start the Letters ➜</a>
                    <a class="btn" href="#page20">Jump to Final ➜</a>
                </div>
            </div>
        </section>

        <!-- 2: Morning Letter -->
        <section id="page2" aria-labelledby="title2">
            <div class="card">
                <h2 id="title2">💌 Morning Letter — When I Wake Up</h2>

                <p>
                    Good morning meri jaan — chahe tum physically mere saath na ho, mera subah tumse shuru hota hai.
                    Subah ki pehli chai, pehli soch, pehli smile— sab tumhari taraf lean karte hain. Jab tumhari good
                    morning message aati hai, mera din set ho jata hai. Wo choti si typing delay bhi jab tum busy ho,
                    mujhe pareshan nahi karti kyunki main jaanta hoon tum wapas aaogi.
                </p>

                <p>
                    Main aksar imagine karta hoon ek aisi morning jahan tum mere samne ho. Tum ek oversized hoodie pehne
                    hogi, ungli se apne baal piche kar rahi hogi, aur main tumhe chhed raha hoga ki tumhe mera sweater
                    chahiye. Bas woh normalness mere liye ek dream hai jo main roz dekhna chahta hoon.
                </p>

                <p>
                    Long-distance mein humari subahیں digital hoti hain — notes, voice messages, photos of your
                    breakfast. Par har chhoti cheez mere liye giant memory ban jaati hai. Tumhari voice note mujhe ek
                    reminder hai ki koi mujhe itna pyaar karta hai ke subah ki simplicity bhi special ban jaati hai.
                </p>

                <div class="small">— Tumhara, jo subah tumhare naam se start karta hai</div>
                <div class="footer-nav">
                    <a class="btn" href="#page3">Midday Letter ➜</a>
                </div>
            </div>
        </section>

        <!-- 3: Midday Letter -->
        <section id="page3" aria-labelledby="title3">
            <div class="card">
                <h2 id="title3">💌 Midday Letter — Little Reminders</h2>

                <p>
                    Jab main office ya college mein busy hota hoon, tum ek sudden meme bhej deti ho, ya ek silly selfie,
                    aur main bas muskuraa deta hoon. Yeh chhote interruptions meri monotonous day ko break kar dete
                    hain. Tumne mujhe sikhaya hai ki love ka matlab grand gestures se zyada daily presence hai — digital
                    presence bhi ek tarah ki dedication hai.
                </p>

                <p>
                    Kabhi kabhi main tumhare messages ko save kar ke rehta hoon, bas future ke liye — taaki jab hum ek
                    saath baithe to main unhe read karwa saku aur tumhara reaction dekh saku. Woh saved messages mere
                    liye ek chhota library hain jise main roz visit karta hoon.
                </p>

                <p>
                    Maine seekha hai ki LDR mein small things count karte hain: on-time replies, late-night "are you
                    awake?" checks, surprise food deliveries, ya simple "tum kaisi ho?" texts. Yeh chhoti cheezein
                    tumhari care ko dikhati hain aur mujhe lagta hai hum dono yahi chhote rituals banate rahenge.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page4">Night Letter ➜</a>
                </div>
            </div>
        </section>

        <!-- 4: Night Letter -->
        <section id="page4" aria-labelledby="title4">
            <div class="card">
                <h2 id="title4">💌 Night Letter — When The World Sleeps</h2>

                <p>
                    Raat ko jab sab so jata hai, hum dono ki calls sabse special hoti hain. Tumhara face screen pe,
                    thoda dim light mein, tum relative quietly baat karte ho — aur main har lafz ko cherish karta hoon.
                    Humari longest calls, sapno ki planning aur secret jokes — sab raaton mein bante hain. Woh raat
                    mujhe lagta hai hum actually present hote hain, distance disappears for a while.
                </p>

                <p>
                    Kabhi kabhi jab tum so jati ho aur main tumhari breathing sunta hoon on call, main sochta hoon ki
                    kaash yeh moment physically ho. Tumhari thandi forehead aur tumhari relaxed shoulder — imagine karte
                    hi ek alag peace milta hai. Until we meet, main har raat is digital intimacy ko sacred rakhta hoon.
                </p>

                <p>
                    Agar koi tumse puchhe ki long-distance tough hai ya nahi, main bas ek example dunga — that night
                    when we both cried, when we talked for hours, when we promised a future. Those nights define our
                    love more than any romantic scene.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page5">Confession — Missing You ➜</a>
                </div>
            </div>
        </section>

        <!-- 5: Confession - Missing You -->
        <section id="page5" aria-labelledby="title5">
            <div class="card">
                <h2 id="title5">🌹 Confession — I Miss You</h2>

                <p>
                    Sach bolun to main tumhe itna miss karta hoon ke kabhi kabhi aankhon mein aansu aa jaate hain —
                    especially jab koi chhota sa trigger aa jata hai: koi song jo tumhe yaad dilata hai, koi place jahan
                    humne baat ki thi, ya koi movie jise hum next week dekhna chahte they. Yeh feeling heavy hoti hai —
                    par uss heaviness ke beech ek warmth bhi hoti hai — because even missing you proves how much you
                    matter to me.
                </p>

                <p>
                    Mujhe tumhari simple presence ki aadat hai: tumhara laugh, tumhari foot-tap while watching, tumhari
                    sleepy voice. All these ordinary things I miss in an extraordinary way. Par main believe karta hoon
                    ye temporary hai — and every day of missing is a day closer to meeting you.
                </p>

                <p>
                    Confession complete: I count days but more than that I collect reasons to meet you soon. Har missed
                    moment ko main ek promise mein convert karta hoon: ek din tumhe sab compensate karunga — extra hugs,
                    extra laughs, extra time. Until then, meri longing tumhare liye ek silent love letter rahegi.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page6">Confession — Little Things ➜</a>
                </div>
            </div>
        </section>

        <!-- 6: Confession - Little Things -->
        <section id="page6" aria-labelledby="title6">
            <div class="card">
                <h2 id="title6">🌹 Confession — I Notice Everything</h2>

                <p>
                    Main tumhari chhoti chhoti cheezein notice karta hoon: jab tum late ho to thoda defensive tone aata
                    hai, ya jab tum excited hoti ho to words tez tez aa jaate hain; woh slight silence jab kuch
                    pareshani hoti hai — main sab dekh leta hoon. Tum sochti hogi ke tum hidden ho sakti ho, par tum
                    literally visible ho har uss chhoti emotion mein.
                </p>

                <p>
                    Main tumhari messages ke andar se rhythm pakad leta hoon — tumhara "OK" aur tumhara "Ok" dono ka
                    matlab alag hota hai mere liye. Main in nuances ko read karke tumhe support karta hoon — kabhi silly
                    pep talk, kabhi simple meme, kabhi quiet suno. Yeh little attentions hi sabse bada pyaar ban jaate
                    hain.
                </p>

                <p>
                    Aaj main confess karta hoon: main tumhare normal self ko zyada prefer karta hoon — no- makeup, no
                    filter, no effort. Bas tum jaisi ho, waisi hi ho — aur main ussi version ko sadaah cherish karta
                    hoon.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page7">Confession — Fears & Hopes ➜</a>
                </div>
            </div>
        </section>

        <!-- 7: Confession - Fears & Hopes -->
        <section id="page7" aria-labelledby="title7">
            <div class="card">
                <h2 id="title7">🌹 Confession — My Fears & Hopes</h2>

                <p>
                    Ek chhota sa fear hai mera: kabhi kabhi main dar jata hoon ki distance humare beech kuch
                    misunderstandings la de. Par phir main yaad karta hoon humari clarity — jo tumhara honesty aur mera
                    patience produce karte hain. Humne already prove kiya hai ki hum complicated emotions ko talk karke
                    solve kar sakte hain.
                </p>

                <p>
                    Hopes ki baat karun to bohot bright hain: main imagine karta hoon ek ghar jahan hum dono apne normal
                    routines share karte hain — tum apni morning routine, main apni work routine, and still we make time
                    for each other. Main chahta hoon humari planning strong ho — travel plans, career support, future
                    savings — sab kuch aligned ho taki jab hum milen to life smoothly start ho jaye.
                </p>

                <p>
                    Confession: I fear losing you but I hope more — I hope we build such strong trust that distance
                    becomes a small chapter in our bigger story. Aur main har din is hope ko nurture karta hoon.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page8">Memory — First Message ➜</a>
                </div>
            </div>
        </section>

        <!-- 8: Memory - First Message -->
        <section id="page8" aria-labelledby="title8">
            <div class="card">
                <h2 id="title8">📸 Memory — Our First Message</h2>

                <p>
                    Mujhe humari pehli chat yaad hai — thoda awkward, thoda curious, aur bohot saari hesitations. Par
                    woh ek line thi jisne sab change kar diya — ek casual "hi" jo gradually became "how are you?" and
                    then "tell me more about yourself." That slow conversation converted into comfort, and from comfort
                    grew trust.
                </p>

                <p>
                    You posted a photo that day and I remember thinking, "I want to know her world." Us excitement ne
                    mujhe gentle bana diya. It amazed me how two strangers can slowly stitch a friendship that becomes
                    the core of a relationship. Even with screens and timezones, we managed to create a space for
                    honesty.
                </p>

                <p>
                    Aaj wo pehli message jo lagbhag nothing thi, mere liye ek treasure hai — proof that simple
                    beginnings can lead to deep connections. I still have that screenshot saved somewhere, and every
                    time I open it I smile like a kid.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page9">Memory — Call That Changed Me ➜</a>
                </div>
            </div>
        </section>

        <!-- 9: Memory - Call That Changed Me -->
        <section id="page9" aria-labelledby="title9">
            <div class="card">
                <h2 id="title9">📸 Memory — The Call That Changed Me</h2>

                <p>
                    Ek call thi jab tum thodi upset thi. Main bas sunta raha — bina kisi advice ke, bas listening mode
                    mein. Us call ke baad tumne kaha "thank you" aur main realize kiya — presence se zyada powerful kuch
                    bhi nahi. Us call ne mujhe sikhaya ki relationship ka matlab show-off se nahi, consistent supportive
                    presence se hota hai.
                </p>

                <p>
                    Us raat humne common fears share kiye, future fantasies discuss kiye, aur chhote se plans banaye.
                    Woh call sirf ek call nahi thi — woh turning point tha: 'yeh relationship real hai, yeh care real
                    hai'.
                </p>

                <p>
                    Tab se main har conversation mein zyada mindful hu. Kabhi kabhi main patterns note karta hoon: tum
                    jab thak jati ho tab tum quiet ho jaati ho, aur mujhe bas tumse puchna hota hai "Are you okay?" Us
                    simple question se humare beech sab clear ho jata hai.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page10">Reasons — Your Voice ➜</a>
                </div>
            </div>
        </section>

        <!-- 10: Reasons - Your Voice -->
        <section id="page10" aria-labelledby="title10">
            <div class="card">
                <h2 id="title10">❤️ Reason I Love You — Your Voice</h2>

                <p>
                    Tumhari voice mere liye anchor hai. Chahe tum excited ho ya tired, tumhari tone har baar kuch keh
                    jaati hai. I replay your voice notes on tough days, and they make everything better. Long-distance
                    mein tumhari voice is like a home audio — it grounds me.
                </p>

                <p>
                    Tumhari voice mein ek comfort hai jo words se zyada kaam karti hai. Ek soft "I'm fine" bhi mujhe
                    pata de deta hai ke tum well ho, aur ek excited "listen!" mujhe instantly engaged kar deta hai. Yeh
                    intimacy mein ek special channel hai — aur main iss channel ko sacred maanta hoon.
                </p>

                <p>
                    Isliye main promise karta hoon ki jab hum milenge, main tumhari voice ko aur zyada ghar mein sunna
                    chahta hoon — tum jaisi ho waisi hi, bina filter ke.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page11">Reasons — Your Care ➜</a>
                </div>
            </div>
        </section>

        <!-- 11: Reasons - Your Care -->
        <section id="page11" aria-labelledby="title11">
            <div class="card">
                <h2 id="title11">❤️ Reason I Love You — Your Care</h2>

                <p>
                    Tum har choti zarurat notice karti ho. Jab main kisi tough situation se guzarta hoon, tum ek simple
                    "how are you handling it?" bhejti ho — aur wo feel hi alag hoti hai. Tumhara care performative nahi,
                    iska evidence tumhare consistent support mein milta hai.
                </p>

                <p>
                    Tumhare thoughtful gestures — surprise snacks delivery, late-night motivational texts, ya bas ek
                    "tum strong ho" message — sab mere liye huge. Yeh sab proof hai ki pyaar action se bhi bolta hai,
                    not just words.
                </p>

                <p>
                    Main tumhare is practical pyaar ko admire karta hoon, because it makes our long-distance reality
                    manageable and hopeful.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page12">Reasons — Your Strength ➜</a>
                </div>
            </div>
        </section>

        <!-- 12: Reasons - Your Strength -->
        <section id="page12" aria-labelledby="title12">
            <div class="card">
                <h2 id="title12">❤️ Reason I Love You — Your Strength</h2>

                <p>
                    Tum quietly strong ho. Jab life throws challenges, tum protocol se handle karti ho — plan, execute,
                    reflect. Tumhara resilience mujhe inspire karta hai to be better. Main tumhari independence respect
                    karta hoon and also want to be the safe place where you can rest.
                </p>

                <p>
                    Tumhara strength showy nahi — it's gentle, practical, and deeply human. That's the kind of strength
                    I want to build my life around. Mere liye tum sirf partner nahi, ek teammate ho.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page13">Promises ➜</a>
                </div>
            </div>
        </section>

        <!-- 13: Promise - Short Term -->
        <section id="page13" aria-labelledby="title13">
            <div class="card">
                <h2 id="title13">💍 Promise — Small Commitments</h2>

                <p>
                    Aaj se main promise karta hoon: har week ek dedicated "us" hour fix karunga — bina distractions,
                    sirf tumhare liye. Agar tum busy ho, main patiently wait karunga — par humari consistency maintain
                    hogi. Chhote commitments create trust — aur main unko take seriously.
                </p>

                <p>
                    Main tumhare birthday month mein extra effort dalunga — surprise messages, small thoughtful things,
                    aur ek plan for our first meeting progress karunga. Yeh small steps humare big dream ko reality
                    banayenge.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page14">Promise — When We Meet ➜</a>
                </div>
            </div>
        </section>

        <!-- 14: Promise - When We Meet -->
        <section id="page14" aria-labelledby="title14">
            <div class="card">
                <h2 id="title14">💍 Promise — The First Meet</h2>

                <p>
                    Jab wo din aayega jab hum milenge, main tumhe pehli baar dekh kar dono haathon se hug karunga— itna
                    tight ke tumhe lage duniya khatam ho gayi. Main plan karunga simple but meaningful day: ek long
                    walk, coffee, humari favourite music aur ek moment jahan hum sirf aapas mein baat karenge.
                </p>

                <p>
                    Main promise karta hoon ki main tumhare liye present rahunga — no phone distractions, no forced
                    plans. Bas pure time tumhara. Main chahunga ki hum saath milkar kuch small traditions banaye — ek
                    secret handshake, ek silly inside joke, aur ek annual "first meet anniversary".
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page15">Promise — Long Term ➜</a>
                </div>
            </div>
        </section>

        <!-- 15: Promise - Long Term -->
        <section id="page15" aria-labelledby="title15">
            <div class="card">
                <h2 id="title15">💍 Promise — For Life</h2>

                <p>
                    Long-term promise simple hai: I will choose you. Har tough decision aane par, main tumhari
                    priorities consider karunga. Hum career decisions, relocation, family discussions sab saath karenge.
                    Main tumhara partner banunga in planning, not just in romance.
                </p>

                <p>
                    Financial security, emotional safety, aur mutual growth — in teeno cheezon pe main kaam karunga.
                    Main chahta hoon humari compatibility reality se match kare — aur uske liye hum daily small
                    exercises karenge: clarity calls, honest feedback, and weekly check-ins for growth.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page16">Gratitude ➜</a>
                </div>
            </div>
        </section>

        <!-- 16: Gratitude -->
        <section id="page16" aria-labelledby="title16">
            <div class="card">
                <h2 id="title16">🙏 Gratitude — Thank You</h2>

                <p>
                    Thank you for staying. Thank you for choosing to continue conversations even on your worst days.
                    Thank you for believing that distance is hard but not impossible. Your patience, your encouragement,
                    your small comforting words — they all matter in ways I can't express fully.
                </p>

                <p>
                    I am grateful for your trust — it's the foundation of everything. Jab tum apni vulnerability dikhati
                    ho, mujhe lagta hai humara bond deeper ho jata hai. Aaj main publicly (well, within this secret
                    website) say kar raha hoon — main lucky hu ke tum mere saath ho.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page17">Dreams ➜</a>
                </div>
            </div>
        </section>

        <!-- 17: Dream - Little Days -->
        <section id="page17" aria-labelledby="title17">
            <div class="card">
                <h2 id="title17">🌈 Dream — Little Days Together</h2>

                <p>
                    I dream simple things — lazy Sundays, making tea together, reading the same book and texting our
                    favourite lines, trying new recipes and failing together, fixing a leaky tap hand in hand. These
                    little ordinary days are what I want most — consistent, comfortable, and deeply ours.
                </p>

                <p>
                    I imagine morning sunlight falling on our balcony while you sip tea and I make a silly face to make
                    you laugh. I imagine us falling into the habit of saying "good night" in person. It's small, but
                    these little rituals are what make a relationship real and resilient.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page18">Dream — Big Plans ➜</a>
                </div>
            </div>
        </section>

        <!-- 18: Dream - Big Plans -->
        <section id="page18" aria-labelledby="title18">
            <div class="card">
                <h2 id="title18">🌈 Dream — Big Plans</h2>

                <p>
                    Big plans matter too — building a life where both our careers and our relationship thrive. I dream
                    of choosing a city together (or designing a work mode) that respects both our ambitions. I dream
                    about us saving for travel, maybe a small house filled with books and plants, and a shelf of
                    memories from every place we've been.
                </p>

                <p>
                    I also dream of supporting your personal goals — whatever they are. If you want to study abroad,
                    I'll be your study partner; if you want to change careers, I'll be your pillar. Big dreams need
                    practical planning, and I want to be your teammate in all of it.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page19">Soft Confession ➜</a>
                </div>
            </div>
        </section>

        <!-- 19: Soft Confession - Jealousy & Care -->
        <section id="page19" aria-labelledby="title19">
            <div class="card">
                <h2 id="title19">💖 Soft Confession — Jealousy & Care</h2>

                <p>
                    Ek soft confession: kabhi kabhi I feel a pinch of jealousy — not because I don't trust you, but
                    because I love you so much that the thought of you giving attention to someone else stings. But I
                    always convert that pinch into awareness — I tell myself to be better, to be more present, to
                    communicate more.
                </p>

                <p>
                    My care is rarely loud — it's in planning your surprise, in remembering your preferences, in sending
                    you a playlist that matches your mood. I want you to always feel secure with me — not possessive,
                    but secure that I'm there for you.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page20">Final Wishes ➜</a>
                </div>
            </div>
        </section>

        <!-- 20: Final Wishes -->
        <section id="page20" aria-labelledby="title20">
            <div class="card">
                <h2 id="title20">🎁 Final Birthday Wishes</h2>

                <p>
                    Happy Birthday meri jaan. Aaj main har un lamhon ke liye shukr guzar hoon jo tumne mujhe diye —
                    late-night calls, random stickers, honest convos, caring texts, tiny fights that quickly become
                    funny stories. Har ek cheez mere liye priceless hai.
                </p>

                <p>
                    My only real wish for you is a life of peace, health, fulfillment and small daily joys. I promise to
                    try my best to bring you laughter more than tears, support more than criticism, and presence more
                    than promises. Aur jab hum milenge, main tumse itni heartfelt baatein karunga ke subah tak baatein
                    chalengi.
                </p>

                <p style="font-weight:700; font-size:18px; margin-top:12px">
                    I love you beyond borders. Distance may delay our meetings but it will never dilute my love for you.
                    This website is a small universe of my feelings — keep it safe, re-read when you miss me, and know
                    that every word here is real. Happy birthday, meri forever.
                </p>

                <div class="footer-nav">
                    <a class="btn" href="#page1">Back to Start ➜</a>
                    <a class="btn" href="#page2">Read Letters Again ➜</a>
                </div>
            </div>
        </section>
    </main>

    <script>
        /* Floating hearts generator — gentle, non-intrusive */
        const colors = ["#ff8fb1", "#ff6f91", "#ffb4c6", "#ffd1e0"];
        function createHeart() {
            const el = document.createElement('div');
            el.className = 'heart';
            const size = 10 + Math.random() * 20;
            el.style.width = size + 'px'; el.style.height = size + 'px';
            el.style.left = Math.random() * 92 + 'vw';
            el.style.top = 100 + Math.random() * 40 + 'vh'; // start off-screen
            el.style.background = colors[Math.floor(Math.random() * colors.length)];
            el.style.zIndex = 500 + Math.floor(Math.random() * 200);
            document.body.appendChild(el);
            const dur = 9000 + Math.random() * 8000;
            el.style.animation = `floatUp ${dur}ms linear forwards`;
            setTimeout(() => el.remove(), dur + 200);
        }
        // Subtle pace so it's romantic but not distracting
        setInterval(createHeart, 700);

        // Smooth focus behavior for side nav
        document.querySelectorAll('#side-toc a, #toc a, .btn').forEach(a => {
            a.addEventListener('click', (e) => {
                const href = a.getAttribute('href');
                if (!href || !href.startsWith('#')) return;
                const id = href.slice(1);
                setTimeout(() => {
                    const t = document.getElementById(id);
                    if (t) {
                        t.setAttribute('tabindex', '-1');
                        t.focus({ preventScroll: true });
                        window.scrollTo({ top: t.getBoundingClientRect().top + window.pageYOffset - 60, behavior: 'smooth' });
                    }
                }, 10);
            });
        });
    </script>

    <!--
    USAGE NOTES:
    1) Replace [Her Name] in the top with her real name.
    2) You can save this as `index.html` and open in any browser.
    3) If you want personal memories (dates/places) inserted into specific pages, send them and I'll patch lines.
    4) Want background music? Tell me the song (or upload MP3) and I'll add a tasteful player (note: many browsers block autoplay).
    5) If you want copy-friendly "print" version or a PDF export, I can generate that too.
  -->
</body>

</html>
