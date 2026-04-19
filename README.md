<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dla Marty ❤️</title>
    <style>
        body {
            /* Łagodniejsze, matowe tło */
            background-color: #d63031;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100"><text x="10" y="30" font-size="20" fill="%23fab1a0" opacity="0.4">❤</text><text x="60" y="80" font-size="20" fill="%2374b9ff" opacity="0.4">❤</text></svg>');
            font-family: 'Montserrat', sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center; /* Centrowanie w pionie */
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            overflow: hidden;
            text-align: center;
        }

        h1 {
            color: #2d3436; /* Ciemny, elegancki kolor zamiast jaskrawego fioletu */
            font-size: 3.5rem; /* Większy tytuł */
            font-weight: 900;
            text-shadow: 3px 3px 0px #ffffff;
            margin-bottom: 40px;
            margin-top: 0;
            line-height: 1.2;
            max-width: 800px;
            z-index: 10;
        }

        /* Kontener na prezent */
        #main-stage {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            width: 100%;
        }

        #gift-container {
            width: 180px;
            height: 180px;
            perspective: 1000px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        #gift-container:hover {
            transform: scale(1.15);
        }

        .cube {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transform: rotateX(-15deg) rotateY(45deg);
            animation: float 4s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% { transform: rotateX(-15deg) rotateY(45deg) translateY(0); }
            50% { transform: rotateX(-15deg) rotateY(45deg) translateY(-20px); }
        }

        .side {
            position: absolute;
            width: 180px;
            height: 180px;
            background: #e84393; /* Spokojniejszy róż */
            border: 4px solid #f9ca24; /* Złota wstążka */
            box-sizing: border-box;
            box-shadow: inset 0 0 30px rgba(0,0,0,0.1);
        }

        .front  { transform: translateZ(90px); }
        .back   { transform: rotateY(180deg) translateZ(90px); }
        .right  { transform: rotateY(90deg) translateZ(90px); }
        .left   { transform: rotateY(-90deg) translateZ(90px); }
        .top    { transform: rotateX(90deg) translateZ(90px); background: #fd79a8; }
        .bottom { transform: rotateX(-90deg) translateZ(90px); }

        .ribbon-v { position: absolute; width: 30px; height: 100%; background: #f9ca24; left: 75px; }
        .ribbon-h { position: absolute; width: 100%; height: 30px; background: #f9ca24; top: 75px; }

        /* Karta z powodem */
        #heart-wrapper {
            display: none;
            flex-direction: column;
            align-items: center;
            animation: popIn 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .paper-heart {
            background-color: #ffcccc; /* Pastelowy róż papieru */
            width: 350px;
            height: 320px;
            clip-path: path('M175,90 C175,90 150,10 85,10 C20,10 0,60 0,110 C0,180 175,300 175,310 C175,300 350,180 350,110 C350,60 330,10 265,10 C200,10 175,90 175,90 Z');
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            padding: 20px;
        }

        #reason-text {
            color: #630e3a;
            font-size: 1.2rem;
            font-weight: bold;
            max-width: 240px;
            margin-top: -40px;
        }

        @keyframes popIn {
            0% { transform: scale(0); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        #reset-btn {
            margin-top: 25px;
            padding: 12px 30px;
            background: #2d3436;
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            transition: 0.3s;
        }

        #reset-btn:hover {
            background: #000;
            transform: translateY(-3px);
        }
    </style>
</head>
<body>

    <div id="main-stage">
        <h1>100 powodów przez które kocham w h*j moją dziewczynę Martę</h1>

        <div id="gift-container" onclick="openGift()">
            <div class="cube">
                <div class="side front"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
                <div class="side back"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
                <div class="side right"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
                <div class="side left"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
                <div class="side top"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
                <div class="side bottom"><div class="ribbon-v"></div><div class="ribbon-h"></div></div>
            </div>
        </div>

        <div id="heart-wrapper">
            <div class="paper-heart">
                <p id="reason-text"></p>
            </div>
            <button id="reset-btn" onclick="resetGift()">Wylosuj kolejny powód 🎁</button>
        </div>
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
            "Za to, że jesteś te parę centymetrów niższa ode mnie – to sprawia, że idealnie pasujesz do moich ramion.",
            "Za Twoją naturalność i to, że nie musisz nic udawać.",
            "Za nasze „umysłowe bluetooth” – rozumiemy się bez słów.",
            "Za to, że masz tak samo świetne poczucie humoru jak ja.",
            "Za to, że nie obrażasz się na mój czarny humor, tylko jeszcze go podkręcasz.",
            "Za to, że tolerujesz i szanujesz moje poglądy polityczne.",
            "Za to, że przy Tobie mogę być kompletnym świrem.",
            "Za nasze wspólne żarty, których nikt poza nami nie ogarnia.",
            "Za to, że każda wiadomość od Ciebie to od razu banan na mojej twarzy.",
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
            "Za to, że Marta to po prostu najlepsze co mnie spotkało.",
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

        function openGift() {
            document.getElementById('gift-container').style.display = 'none';
            const wrapper = document.getElementById('heart-wrapper');
            const text = document.getElementById('reason-text');
            const randomReason = reasons[Math.floor(Math.random() * reasons.length)];
            text.innerText = randomReason;
            wrapper.style.display = 'flex';
        }

        function resetGift() {
            document.getElementById('gift-container').style.display = 'block';
            document.getElementById('heart-wrapper').style.display = 'none';
        }
    </script>
</body>
</html>
