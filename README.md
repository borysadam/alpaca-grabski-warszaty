# alpaca@grabski

    DELETEME: w miejsce ❓ wstaw prognozowany czas

 - Data: 16.12.2022
 - Godzina: 8:55
 - Czas trwania: 3h
 - 2 grupy
 - 2 części
    - Teoria - wspólnie
    - Praktyka - grupy oddzielnie, identyczny materiał, identyczne zadania (rozdzielimy się)
  
# Opis 
Strona warsztatów. Stwrórz własna alpakę z dowolnymi szczegółami!
Autorzy: Jan żółty, Janusz Pawlacz
# Zawartość strony

### HTML

### JS

# Zadania praktyczne

## 1. Dodaj kontrolkę do zmiany alpaki
<b>HTML</b>
<label for="controlAlpaca">Choose your alpaca</label>
<div id="controlAlpaca" class="panel">
    <span id="spanAlpaca">alpaca0</span>
    <button onclick="<...>">
        <i class="fa-solid <...> fa-xl"></i>
    </button>
</div>
<b>JS</b>
/**
 * @description This function draws an alpaca or only it's snout.
 * It's asynchronous, so remember to call it using `await`, so images are drawn in correct order.
 * @param {number} i 0 or 1 to choose from two alpacas.
 * @param {boolean} isSnout Choose whether to draw an alpaca (false) or only it's snout (true).
 */
async function drawAlpaca(i, isSnout) {
	const src = `<... template string>`;
	await drawImage(src, 50, 128, 1);
}

## 2. Dodaj kontrolkę do zmiany czapki/okulary/rzecz w pyszczku
<b>HTML</b>
<label for="controlHat">Wear your favourite hat</label>
<div id="controlHat" class="panel">
    <button onclick="<...>">
        <i class="fa-solid <...> fa-xl"></i>
    </button>
    <span id="spanHatItem">none</span>
    <button onclick="<...>">
        <i class="fa-solid <...> fa-xl"></i>
    </button>
</div>
<b>JS</b>
/**
 * @description This function draws a <...>.
 * It's asynchronous, so remember to call it using `await`, so images are drawn in correct order.
 * @param {*} i 0 for none and 1-3 to choose from three hats.
 */
async function draw<...>Item(i) {
	const item = <...>ItemProperties[i];
	if (item.name !== 'none') {
		ctx.clearRect(0, 0, canvas.width, 285);
		const { name, x, y, scale } = item;
		const src = `./assets/img/item/hat/${name}.png`;
		await drawImage(src, x, y, scale);
	}
}

## 3. Dodaj element canvas
<div class="designer container">
    <canvas id="canvas" width="384" height="512"></canvas>
</div>

## 4. Dodaj współrzędne i skalę czapki/okularów/rzeczy w pyszczku w pliku item-properties.js
const <...> ItemProperties = [
	{ name: 'none' },
	{ name: '<...>', x: 0, y: 0, scale: 1 },
	{ name: '<...>', x: 0, y: 0, scale: 1 },
	{ name: '<...>', x: 0, y: 0, scale: 1 },
]


## 5. Osadź w stronie skrypt główny
Dodaj do storny główny skrypt JS. Mozesz to zrobić w sekcji HEAD strony lub przed końcowym znacznikiem BODY.
<script src="index.js"></script>

## 6. Osadź w stronie skrypt zawierający informacje z puntu 4
<script src="item-properties.js"></script> <!-- Script at the end of page body speeds up loading -->





