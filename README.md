<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>100 Powodów - Dla Marty ❤️</title>
    <style>
        body {
            /* Czerwone tło z różowymi i błękitnymi serduszkami w SVG */
            background-color: #ff1a1a;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="120" height="120"><text x="10" y="40" font-size="30" fill="%23ffb6c1">❤</text><text x="70" y="90" font-size="30" fill="%2387cefa">❤</text></svg>');
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            overflow-x: hidden;
            text-align: center;
        }

        h1 {
            color: #9b30ff; /* Ładny fioletowy kolorek */
            font-size: 2.8rem;
            text-shadow: 2px 2px 0px #fff, 4px 4px 5px rgba(0,0,0,0.4);
            margin-top: 30px;
            margin-bottom: 50px;
            max-width: 900px;
        }

        /* Kontener na prezent 3D */
        #gift-container {
            width: 200px;
            height: 200px;
            perspective: 800px;
            cursor: pointer;
            margin-bottom: 20px;
            transition: transform 0.3s ease;
        }

        #gift-container:hover {
            transform: scale(1.1);
        }

        /* Kostka 3D */
        .cube {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transform: rotateX(-15deg) rotateY(45deg);
            transition: transform 0.5s ease;
            animation: float 3s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% { transform: rotateX(-15deg) rotateY(45deg) translateY(0); }
            50% { transform: rotateX(-15deg) rotateY(45deg) translateY(-15px); }
        }

        .side {
            position: absolute;
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, #ff1493, #c71585); /* Ciemnoróżowy prezent */
            border: 5px solid #ffd700; /* Złota wstążka */
            box-sizing: border-box;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px;
            box-shadow: inset 0 0 20px rgba(0,0,0,0.2);
        }

        /* Pozycjonowanie boków prezentu */
        .front  { transform: translateZ(100px); }
        .back   { transform: rotateY(180deg) translateZ(100px); }
        .right  { transform: rotateY(90deg) translateZ(100px); }
        .left   { transform: rotateY(-90deg) translateZ(100px); }
        .top    { transform: rotateX(90deg) translateZ(100px); background: #ff69b4; }
        .bottom { transform: rotateX(-90deg) translateZ(100px); background: #8b008b; }

        .ribbon-vertical { position: absolute; width: 30px; height: 100%; background: #ffd700; left: 85px; }
        .ribbon-horizontal { position: absolute; width: 100%; height: 30px; background: #ffd700; top: 85px; }

        /* Papierowe serduszko */
        #heart-wrapper {
            display: none;
            flex-direction: column;
            align-items: center;
            animation: popIn 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .paper-heart {
            background-color: #ffb6c1; /* Różowy papier */
            width: 380px;
            height: 340px;
            position: relative;
            /* Tworzenie kształtu serca w CSS */
            clip-path: path('M190,100 C190,100 160,10 95,10 C25,10 0,65 0,115 C0,200 190,320 190,330 C190,320 380,200 380,115 C380,65 355,10 285,10 C220,10 190,100 190,100 Z');
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 15px 25px rgba(0,0,0,0.3);
            text-align: center;
            margin-bottom: 30px;
        }

        /* Tekst na serduszku */
        #reason-text {
            color: #d02090;
            font-size: 1.3rem;
            font-weight: bold;
            width: 250px;
            margin-top: -30px;
            padding: 10px;
            font-family: 'Comic Sans MS', cursive, sans-serif;
        }

        @keyframes popIn {
            0% { transform: scale(0.1); opacity: 0; }
            80% { transform: scale(1.1); opacity: 1; }
            100% { transform: scale(1); opacity: 1; }
        }

        /* Przycisk odnowienia */
        #reset-btn {
            padding: 15px 40px;
            background: #9b30ff;
            color: white;
            border: 3px solid white;
            border-radius: 30px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.4);
            transition: all 0.2s ease;
        }

        #reset-btn:hover {
            background: #8a2be2;
            transform: scale(1.05);
        }
    </style>
</head>
<body>

    <h1>100 powodów przez które kocham w h*j moją dziewczynę Martę</h1>

    <div id="gift-container" onclick="openGift()">
        <div class="cube" id="cube">
            <div class="side front"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div></div>
            <div class="side back"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div></div>
            <div class="side right"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div></div>
            <div class="side left"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div></div>
            <div class="side top"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div>🎀</div>
            <div class="side bottom"><div class="ribbon-vertical"></div><div class="ribbon-horizontal"></div></div>
        </div>
    </div>

    <div id="heart-wrapper">
        <div class="paper-heart">
            <p id="reason-text"></p>
        </div>
        <button id="reset-btn" onclick="resetGift()">Zaskocz mnie jeszcze raz! 🎁</button>
    </div>

    <script>
        // Wszystkie 100 powodów wylosowane z naszej listy
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
            "Za nasze „umysłowe bluetooth” – rozumiemy się bez słów i myślimy o tym samym.",
            "Za to, że masz tak samo świetne poczucie humoru jak ja.",
            "Za to, że nie obrażasz się na mój czarny humor, tylko jeszcze go podkręcasz.",
            "Za to, że tolerujesz i szanujesz moje poglądy polityczne.",
            "Za to, że przy Tobie mogę być kompletnym świrem i wiem, że mnie nie ocenisz.",
            "Za nasze wspólne żarty, których nikt poza nami nie ogarnia.",
            "Za to, że każda wiadomość od Ciebie to od razu banan na mojej twarzy.",
            "Za nasze nocne rozmowy o wszystkim i o niczym.",
            "Za to, że zawsze mnie wspierasz, kiedy mam gorszy dzień.",
            "Za to, że szczerze się o mnie martwisz i zawsze dbasz, żeby było mi dobrze.",
            "Za poczucie, że zawsze stoisz po mojej stronie, bez względu na wszystko.",
            "Za Twoją cierpliwość do moich głupich pomysłów i tekstów.",
            "Za to, że wierzysz we mnie bardziej niż ja sam w siebie.",
            "Za Twoją lojalność, która daje mi ogromne poczucie bezpieczeństwa.",
            "Za to, że zawsze znajdziesz dla mnie czas, nawet gdy masz dużo na głowie.",
            "Za sposób, w jaki marszczysz czoło, gdy się nad czymś bardzo skupiasz.",
            "Za to, jak uroczo wyglądasz, kiedy się złościsz.",
            "Za to, że jesteś moją pierwszą myślą zaraz po przebudzeniu.",
            "Za Twój zapach, który zostaje na moich bluzach po każdym spotkaniu.",
            "Za to, że Marta to po prostu najlepsze, co mogło mnie w życiu spotkać.",
            "Za to, jak precyzyjnie robisz bransoletki – widać w tym Twoją pasję.",
            "Za to, że jesteś mądrzejsza od absolutnie wszystkich ludzi, których znam.",
            "Za Twoją błyskotliwość, która sprawia, że każda rozmowa z Tobą jest ciekawa.",
            "Za to, że każda piosenka o miłości przypomina mi teraz o Tobie.",
            "Za to, jak uroczo wyglądasz w czapce albo z rozpuszczonymi włosami.",
            "Za Twoją szczerość, bo wiem, że zawsze powiesz mi prawdę prosto w oczy.",
            "Za to, że potrafisz mnie przegadać w debatach, co mega w Tobie szanuję.",
            "Za Twoje dłonie, które idealnie splatają się z moimi.",
            "Za to, że jesteś moją największą motywacją, żeby stawać się lepszym.",
            "Za to, jak twardo bronisz swojego zdania i swoich wartości.",
            "Za nasze wspólne oglądanie filmów i granie, gdzie czas płynie za szybko.",
            "Za to, że znasz moje najdziwniejsze sekrety i dalej chcesz ze mną być.",
            "Za Twoje „fochy”, które trwają krótko i kończą się najsłodszymi przeprosinami.",
            "Za to, jak pachną Twoje włosy, kiedy Cię przytulam na pożegnanie.",
            "Za ciszę z Tobą, która nigdy nie jest niezręczna.",
            "Za Twoją energię, która sprawia, że chce mi się działać.",
            "Za to, że wystarczy jeden Twój sms, żeby uratować mój słaby dzień.",
            "Za to, że jesteś moim „bezpiecznym miejscem” na ziemi.",
            "Za to, że nie boisz się rozmawiać ze mną na trudne i poważne tematy.",
            "Za to, że jesteś dla mnie wzorem, jak być dobrym i utalentowanym człowiekiem.",
            "Za wspólne spacery, na których moglibyśmy iść przed siebie bez końca.",
            "Za to, jak pasjonująco opowiadasz o swoich sukcesach i marzeniach.",
            "Za to, że zawsze wyczujesz, gdy coś mnie gryzie, zanim w ogóle to powiem.",
            "Za to, że jesteś główną bohaterką wszystkich moich najlepszych wspomnień.",
            "Za Twój unikalny styl, w którym zawsze wyglądasz jak milion dolarów.",
            "Za to, że jesteś wyjątkowa i nie próbujesz nikogo naśladować.",
            "Za to, że nie muszę przy Tobie zakładać żadnej maski.",
            "Za to, jak uroczo mrużysz oczy, gdy świeci na nie słońce.",
            "Za to, że każda godzina bez Ciebie ciągnie się jak tydzień.",
            "Za to, jak słodko wymawiasz moje imię w sytuacjach, gdy jesteśmy sami.",
            "Za wspólne jedzenie pizzy i innych rzeczy, które oboje uwielbiamy.",
            "Za to, że inspirujesz mnie do rozwijania moich własnych pasji.",
            "Za Twoje serce, w którym zawsze znajduję miejsce dla siebie.",
            "Za to, że potrafisz mnie zaskoczyć małym gestem w najmniej spodziewanym momencie.",
            "Za Twoją kreatywność, której zazdroszczą Ci pewnie wszyscy w szkole.",
            "Za to, że jesteś jedyną osobą, dla której zawsze mam włączone powiadomienia.",
            "Za to, że akceptujesz moje wszystkie dziwne fazy i hobby.",
            "Za poczucie, że z Tobą obok mogę osiągnąć wszystko, co sobie zaplanuję.",
            "Za to, jak pięknie odbija się światło w Twoich zielono-brązowych oczach.",
            "Za to, że każda nasza rozmowa uczy mnie czegoś nowego.",
            "Za Twoje reakcje na moje memy – nawet te najbardziej suche.",
            "Za to, że jesteś moją „drugą połówką” w każdym znaczeniu tego słowa.",
            "Za to, że sprawiasz, iż czuję się przy Tobie wyjątkowy i ważny.",
            "Za każdą wspólną wycieczkę, nawet jeśli to tylko wyjście do sklepu.",
            "Za Twój spokój i opanowanie, gdy ja zaczynam się czymś stresować.",
            "Za to, jak naturalnie piękna jesteś zaraz po obudzeniu, bez żadnych filtrów.",
            "Za to, że jesteś jedynym powodem, dla którego tak bardzo dbam o siebie.",
            "Za Twoje codzienne „dobranoc”, bez którego nie potrafię zasnąć.",
            "Za to, że jesteś definicją mojego szczęścia.",
            "Za to, że słuchasz mnie uważnie, nawet gdy gadam o głupotach.",
            "Za nasze wspólne zdjęcia, na których widać, jak bardzo jesteśmy zgrani.",
            "Za to, że potrafisz mnie rozczulić jednym, krótkim spojrzeniem.",
            "Za Twój upór, który sprawia, że zawsze osiągasz to, co chcesz.",
            "Za to, że jesteś najbardziej utalentowaną dziewczyną, jaką kiedykolwiek poznałem.",
            "Za to, że nigdy bym Cię nie zamienił na nikogo innego na tym świecie.",
            "Za to, że jesteś słońcem, które wychodzi u mnie po każdej burzy.",
            "Za to, jak uroczo ziewasz, gdy próbujesz udawać, że wcale nie jesteś śpiąca.",
            "Za to, że po prostu jesteś niesamowitą osobą, Marto.",
            "Za każdy moment, kiedy trzymasz mnie za rękę i nie puszczasz.",
            "Za to, że przy Tobie zapominam o wszystkim, co mnie denerwuje w szkole czy w domu.",
            "Za Twoją delikatność, która idzie w parze z mega silnym charakterem.",
            "Za to, że jesteś tak blisko mojego serca, nawet gdy dzielą nas kilometry.",
            "Za to, że stworzyliśmy nasz własny, mały świat, do którego nikt inny nie ma wstępu.",
            "Za blask w Twoich oczach, gdy opowiadasz o czymś, co naprawdę kochasz robić.",
            "Za to, że sprawiasz, że uśmiecham się do ekranu telefonu jak wariat.",
            "Za Twoją empatię i to, jak bardzo przejmujesz się losem innych.",
            "Za to, że jesteś moją siłą napędową w każdy poniedziałek.",
            "Za to, że jesteś bohaterką moich wszystkich najmilszych snów.",
            "Za to, że z każdym kolejnym dniem kocham Cię jeszcze bardziej niż wczoraj.",
            "Za to, że jesteś po prostu Martą – moją wyjątkową, jedyną dziewczyną.",
            "Za to, że kocham Cię w h*j i żadne słowa tego nigdy do końca nie opiszą!"
        ];

        // Funkcja ukrywająca prezent i pokazująca serce z tekstem
        function openGift() {
            const gift = document.getElementById('gift-container');
            const heartWrapper = document.getElementById('heart-wrapper');
            const textElement = document.getElementById('reason-text');
            
            // Losowanie powodu
            const randomIndex = Math.floor(Math.random() * reasons.length);
            const randomReason = reasons[randomIndex];
            
            // Podmiana tekstu
            textElement.innerText = randomReason;
            
            // Animacja zniknięcia prezentu i pojawienia się serca
            gift.style.display = 'none';
            heartWrapper.style.display = 'flex';
        }

        // Funkcja resetująca widok
        function resetGift() {
            const gift = document.getElementById('gift-container');
            const heartWrapper = document.getElementById('heart-wrapper');
            
            // Przywracanie prezentu
            heartWrapper.style.display = 'none';
            gift.style.display = 'block';
        }
    </script>
</body>
</html>
