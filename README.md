# Hádej vlajku! 🚩

Jednoduchá hra v prohlížeči, ve které děti hádají vlajky zemí světa.
Celé je to **jeden soubor `index.html`** – žádný server, žádná instalace, žádné závislosti.
Sourozenec hry [PokéHádej](https://github.com/mlutonsky/pokeguess), jen s vlajkami.

## Jak hrát

Otevři [`index.html`](index.html) v prohlížeči (nebo soubor přetáhni do okna prohlížeče).

Hra má **dva režimy**, přepínají se tlačítky nahoře:

- 🏳️ **Hádej zemi** – zobrazí se vlajka, dítě vybírá ze tří názvů zemí.
- 🚩 **Hádej vlajku** – zobrazí se název země, dítě vybírá ze tří vlajek.

Po každé odpovědi se správná možnost zvýrazní zeleně, ostatní se ztlumí, a ukáže se
krátká zpětná vazba se skóre ✓ / ✗.

### 🔊 Čtení názvů nahlas

U každého názvu je oddělené tlačítko **„Poslechni"**, které název země přečte nahlas
**česky** (přes systémový hlas prohlížeče – Web Speech API, `cs-CZ`). Je záměrně **mimo**
odpovědní tlačítko, aby si dítě mohlo poslechnout název, aniž by omylem zvolilo
špatnou odpověď. Skvělé pro děti, které ještě neumí číst.

## Pro koho je to dělané

Primárně pro **malé děti** na **tabletu na šířku**:

- velká tlačítka a dotykové plochy, velká čitelná písma,
- klidné, nerušivé rozhraní vyplňující celou obrazovku,
- funguje i na mobilu (na výšku se názvy přeskládají pod sebe).

## Technické detaily

- Čistý **HTML + CSS + JavaScript**, bez build kroku a bez frameworků.
- České názvy zemí jsou v souboru napevno; vlajky se načítají z
  [flagcdn.com](https://flagcdn.com) podle ISO 3166-1 kódů zemí, proto je k běhu
  potřeba **připojení k internetu**.
- Čtení názvů využívá `speechSynthesis` (Web Speech API) s českým hlasem – kvalita
  hlasu závisí na zařízení a prohlížeči (na zařízeních bez českého hlasu se použije
  výchozí systémový hlas).
- Nová trojice se v každém kole nepřekrývá s tou předchozí, takže se země hned neopakují.

## Poznámka

Vlajky jsou veřejně dostupné státní symboly. Projekt je neoficiální, určený jen pro
zábavu a učení.
