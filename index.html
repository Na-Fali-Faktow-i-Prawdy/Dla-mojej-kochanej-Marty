<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dla Marty ❤️</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@900&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            /* Matowe, eleganckie czerwone tło */
            background-color: #a31616;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100"><text x="15" y="40" font-size="25" fill="%23ff8da1" opacity="0.3">❤</text><text x="60" y="85" font-size="25" fill="%23a2d2ff" opacity="0.3">❤</text></svg>');
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center; /* To trzyma wszystko na środku */
            overflow: hidden;
            font-family: 'Montserrat', sans-serif;
            text-align: center;
        }

        h1 {
            /* Wielki fioletowy tytuł z obrysem */
            color: #8a2be2;
            font-size: 4rem; /* Bardzo duży */
            text-transform: uppercase;
            letter-spacing: -2px;
            paint-order: stroke fill;
            -webkit-text-stroke: 10px white; /* Biały gruby obrys, żeby się nie zlewało */
            margin-bottom: 50px;
            padding: 0 20px;
            z-index: 10;
        }

        /* Kontener na prezent 3D */
        #gift-box {
            width: 200px;
            height: 200px;
            perspective: 1000px;
            cursor: pointer;
            transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        #gift-box:hover {
            transform: scale(1.1) rotate(5deg);
        }

        .cube {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transform: rotateX(-15deg) rotateY(45deg);
            animation: float 3s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% { transform: rotateX(-15deg) rotateY(45deg) translateY(0); }
            50% { transform: rotateX(-15deg) rotateY(45deg) translateY(-30px); }
        }

        .side {
            position: absolute;
            width: 200px;
            height: 200px;
            background: #ff4d6d; /* Ładny różowy prezent */
            border: 5px solid #ffd700; /* Złota wstążka */
            box-shadow: inset 0 0 40px rgba(0,0,0,0.2);
        }

        .front  { transform: translateZ(100px); }
        .back   { transform: rotateY(180deg) translateZ(100px); }
        .right  { transform: rotateY(90deg) translateZ(100px); }
        .left   { transform: rotateY(-90deg) translateZ(100px); }
        .top    { transform: rotateX(90deg) translateZ(100px); background: #ff758f; }
        .bottom { transform: rotateX(-90deg) translateZ(100px); background: #c9184a; }

        .v-ribbon { position: absolute; width: 40px; height: 100%; background: #ffd700; left: 80px; }
        .h-ribbon { position: absolute; width: 100%; height: 40px; background: #ffd700; top: 80px; }

        /* Serduszko papierowe */
        #heart-container {
            display: none;
            flex-direction: column;
            align-items: center;
            animation: pop 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .heart-paper {
            background-color: #ffb3c1;
            width: 450px;
            height: 400px;
            clip-path: path('M225,100 C225,100 190,10 110,10 C30,10 0,70 0,130 C0,220 225,360 225,380 C225,360 450,220 450,130 C450,70 420,10 340,10 C260,10 225,100 225,100 Z');
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        #reason-text {
            font-family: 'Dancing Script', crossorigin;
            font-size: 1.8rem;
            color: #590d22;
            max-width: 300px;
            margin-top: -50px;
            line-height: 1.3;
        }

        @keyframes pop {
            0% { transform: scale(0); }
            100% { transform: scale(1); }
        }

        #refresh-btn {
            margin-top: 30px;
            padding: 15px 40px;
            background: #ffffff;
            color: #a31616;
            border: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: 0.3s;
        }

        #refresh-btn:hover {
            transform: translateY(-5px);
            background: #ffb3c1;
        }

        /* Responsywność dla telefonów */
        @media (max-width: 600px) {
            h1 { font-size: 2rem; -webkit-text-stroke: 5px white; }
            .heart-paper { width: 320px; height: 300px; }
            #reason-text { font-size: 1.3rem; max-width: 200px; }
        }
    </style>
</head>
<body>

    <h1 id="main-title">100 powodów przez które kocham w h*j moją dziewczynę Martę</h1>

    <div id="gift-box" onclick="showReason()">
        <div class="cube">
            <div class="side front"><div class="v-ribbon"></div><div class="h-ribbon"></div></div>
            <div class="side back"><div class="v-ribbon"></div><div class="h-ribbon"></div></div>
            <div class="side right"><div class="v-ribbon"></div><div class="h-ribbon"></div></div>
            <div class="side left"><div class="v-ribbon"></div><div class="h-ribbon"></div></div>
            <div class="side top"><div class="v-ribbon"></div><div class="h-ribbon"></div></div>
            <div class="side bottom"></div>
        </div>
    </div>

    <div id="heart-container">
        <div class="heart-paper">
            <p id="reason-text"></p>
        </div>
        <button id="refresh-btn" onclick="resetPage()">Wylosuj jeszcze raz! 🎁</button>
    </div>

    <script>
        const reasons = [
            "Za Twoje przepiękne zielono-brązowe oczy, w których zawsze się gubię.",
            "Za Twój niesamowity głos, kiedy śpiewasz – mógłbym Cię słuchać godzinami.",
            "Za to, że masz talent do wszystkiego, czego się dotkniesz.",
            "Za te wszystkie piękne bransoletki, które potrafisz wyczarować.",
            "Za to, że gotujesz lepiej niż ktokolwiek inny na świecie.",
            "Za Twój najpiękniejszy uśmiech, który rozjaśnia mi każdy dzień.",
            "Za Twoją idealną figurę, która zawsze mnie zachwyca.",
            "Za to, że jesteś te parę centymetrów niższa ode mnie.",
            "Za Twoją naturalność i to, że nie musisz nic udawać.",
            "Za nasze „umysłowe bluetooth” – rozumiemy się bez słów.",
            "Za to, że masz tak samo świetne poczucie humoru jak ja.",
            "Za to, że nie obrażasz się na mój czarny humor.",
            "Za to, że tolerujesz i szanujesz moje poglądy polityczne.",
            "Za to, że przy Tobie mogę być kompletnym świrem.",
            "Za nasze wspólne żarty, których nikt poza nami nie ogarnia.",
            "Za to, że każda wiadomość od Ciebie to uśmiech na mojej twarzy.",
            "Za nasze nocne rozmowy o wszystkim i o niczym.",
            "Za to, że zawsze mnie wspierasz, kiedy mam gorszy dzień.",
            "Za to, że szczerze się o mnie martwisz.",
            "Za poczucie, że zawsze stoisz po mojej stronie.",
            "Za Twoją cierpliwość do moich głupich pomysłów.",
            "Za to, że wierzysz we mnie bardziej niż ja sam.",
            "Za Twoją lojalność, która daje mi bezpieczeństwo.",
            "Za to, że zawsze znajdziesz dla mnie czas.",
            "Za sposób, w jaki marszczysz czoło przy skupieniu.",
            "Za to, jak uroczo wyglądasz, kiedy się złościsz.",
            "Za to, że jesteś moją pierwszą myślą po przebudzeniu.",
            "Za Twój zapach na moich bluzach.",
            "Za to, że Marta to najlepsze co mnie spotkało.",
            "Za precyzję z jaką robisz bransoletki.",
            "Za to, że jesteś mądrzejsza od absolutnie wszystkich których znam.",
            "Za Twoją błyskotliwość w każdej rozmowie.",
            "Za to, że każda piosenka o miłości przypomina mi o Tobie.",
            "Za to, jak uroczo wyglądasz w czapce.",
            "Za Twoją szczerość prosto w oczy.",
            "Za to, że potrafisz mnie przegadać w debatach.",
            "Za Twoje dłonie idealnie pasujące do moich.",
            "Za to, że jesteś moją największą motywacją.",
            "Za to, jak twardo bronisz swojego zdania.",
            "Za nasze wspólne oglądanie filmów i granie.",
            "Za to, że znasz moje sekrety i dalej przy mnie jesteś.",
            "Za Twoje fochy kończące się słodkimi przeprosinami.",
            "Za zapach Twoich włosów przy przytulaniu.",
            "Za ciszę z Tobą, która nie jest niezręczna.",
            "Za Twoją energię do działania.",
            "Za SMS-y ratujące mój słaby dzień.",
            "Za to, że jesteś moim bezpiecznym miejscem.",
            "Za trudne rozmowy, których się nie boisz.",
            "Za bycie wzorem utalentowanego człowieka.",
            "Za wspólne spacery bez celu.",
            "Za pasję, z jaką opowiadasz o marzeniach.",
            "Za to, że wyczujesz mój gorszy humor bez słów.",
            "Za bycie bohaterką moich wspomnień.",
            "Za Twój styl, w którym wyglądasz jak milion dolarów.",
            "Za to, że nie udajesz nikogo innego.",
            "Za to, że nie muszę przy Tobie zakładać maski.",
            "Za to, jak mrużysz oczy na słońcu.",
            "Za to, że godzina bez Ciebie to wieczność.",
            "Za to, jak słodko wymawiasz moje imię.",
            "Za wspólne jedzenie pizzy.",
            "Za inspirowanie mnie do rozwoju.",
            "Za Twoje serce, w którym mam swoje miejsce.",
            "Za niespodzianki w najmniej spodziewanych momentach.",
            "Za Twoją kreatywność, której wszyscy zazdroszczą.",
            "Za bycie jedynym priorytetowym powiadomieniem.",
            "Za akceptację moich dziwnych hobby.",
            "Za wiarę, że z Tobą podbiję świat.",
            "Za blask słońca w Twoich oczach.",
            "Za naukę czegoś nowego w każdej rozmowie.",
            "Za reakcje na moje memy.",
            "Za bycie moją drugą połówką.",
            "Za to, że przy Tobie czuję się ważny.",
            "Za każdą wycieczkę, nawet do sklepu.",
            "Za Twój spokój, gdy ja panikuję.",
            "Za naturalne piękno rano bez filtrów.",
            "Za to, że dzięki Tobie bardziej o siebie dbam.",
            "Za codzienne dobranoc.",
            "Za bycie definicją szczęścia.",
            "Za to, że uważnie mnie słuchasz.",
            "Za wspólne zdjęcia, na których jesteśmy wariatami.",
            "Za rozczulające spojrzenia.",
            "Za upór w dążeniu do celu.",
            "Za to, że jesteś najbardziej utalentowaną dziewczyną jaką znam.",
            "Za to, że nigdy bym Cię nie zamienił.",
            "Za bycie moim słońcem po burzy.",
            "Za to, jak uroczo ziewasz.",
            "Za bycie po prostu niesamowitą Martą.",
            "Za trzymanie mnie za rękę.",
            "Za zapominanie przy Tobie o problemach w szkole.",
            "Za połączenie delikatności z silnym charakterem.",
            "Za bycie blisko serca mimo kilometrów.",
            "Za nasz własny, osobny świat.",
            "Za blask w oczach przy robieniu tego co kochasz.",
            "Za uśmiech do telefonu przez Ciebie.",
            "Za Twoją empatię do innych.",
            "Za bycie siłą napędową w poniedziałki.",
            "Za bycie bohaterką moich snów.",
            "Za to, że kocham Cię dziś mocniej niż wczoraj.",
            "Za bycie po prostu moją Martą.",
            "Za to, że kocham Cię w h*j!"
        ];

        function showReason() {
            document.getElementById('gift-box').style.display = 'none';
            document.getElementById('main-title').style.display = 'none';
            const container = document.getElementById('heart-container');
            const text = document.getElementById('reason-text');
            
            const randomReason = reasons[Math.floor(Math.random() * reasons.length)];
            text.innerText = randomReason;
            
            container.style.display = 'flex';
        }

        function resetPage() {
            document.getElementById('gift-box').style.display = 'block';
            document.getElementById('main-title').style.display = 'block';
            document.getElementById('heart-container').style.display = 'none';
        }
    </script>
</body>
</html>
