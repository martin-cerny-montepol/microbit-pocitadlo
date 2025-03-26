# Počítadlo

Počítání nechme na počítači! Může za nás počítat počet skoků pře švihadlo, stejně jako počet náklaďáků na křižovatce.

## Začněme od nuly

Když chceme, aby si počítač něco zapamatoval, třeba jen na chvíli, musíme vytvořit proměnnou `pocet`. Při startu ji pak nastavíme na její počáteční stav, coč bude `0`. 

Proměnnou `pocet` pak zobrazíme na displeji.

```blocks
let pocet = 0
pocet = 0
basic.showNumber(pocet)
```

## A přičítáme, a přičítáme, ...

Při každém stisku tlačítka A změníme proměnou `pocet` o +1 a výsledek znovu zobrazíme.

```blocks
input.onButtonPressed(Button.A, function () {
    pocet += 1
    basic.showNumber(pocet)
})
```

## Jenže počítadlo je moc "pomalé"

Budeme muset oddělit počítání a zobrazování, protože zobrazování čísla trvá moc dlouho. Zobrazovat budeme pořád dokola (opakuj stále), místo po každém stisku tlačítka.

```blocks
basic.forever(function () {
    basic.showNumber(pocet)
})
```

## Zpátky na nulu!

V tuto chvíli musíme micro:bit vypnout a zase zapnout, abychom počítadlo vynulovali. To je trochu otrava. Nastav microbit, aby počítadlo vynuloval při stisku tlačítka B.

```blocks
input.onButtonPressed(Button.B, function () {
    pocet = 0
})
```