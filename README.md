# IsiBheqe soHlamvu: learn it, and the consonant chart

**Live site:** https://barc-prog.github.io/isibheqe-chart/

A teaching page and an interactive consonant chart for **IsiBheqe soHlamvu** (isiZulu) / **Ditema tsa Dinoko** (Sesotho), a featural syllabary for the siNtu (Southern Bantu) languages. Tap any symbol or example word to hear it.

## The pages

- `index.html` is the teaching page (the main address). It covers where the script comes from, then four steps: *Ibheqe* (the syllable), *Onkamisa* (vowels), *Ongwaqa* (consonants) and *Uphimbo, lerothodi* (the marks).
- `chart.html` is the consonant chart. It has two modes, row by row (`?mode=steps`) and the whole chart (`?mode=whole`).
- `learn.html` forwards to the main page so that old links keep working.
- `site.css` holds the styles shared by both pages.
- `archive/` holds files the site no longer uses (see `archive/README.md`).

## Who made what

- **The script:** its creators, through isibheqe.org.za. Pule kaJanolintji (co-creator and linguist) checks the linguistics on this site.
- **This site:** Bandile Ngidi, a collaborator on the script, not its creator.
- **Recordings:** Bandile Ngidi.
- **Images and text from isibheqe.org.za** (© Isibheqe Sohlamvu / Ditema tsa Dinoko) are used with permission. The chart's symbols are drawn in the isibheqe.org.za demo shapes; a redraw in the new keyboard and font shapes is planned.
- **From Wikimedia Commons:** the consonant shapes graphic by Pule kaJanolintshi and Francis Burger (CC BY-SA 4.0), and the three mark diagrams by Lucas (Chromarrays, CC0).
- **Spellings and IPA** are checked against the PanSALB orthography and spelling rules for the nine languages.

The site's credits section has the full list.

## Corrections

Spotted a wrong symbol, spelling, sound or word? Open an issue on this repository, or tell Bandile in the isiBheqe WhatsApp group. Linguistic corrections go to Pule before they change the chart.

## How the chart works

The chart is generated from data. Each cell is one JSON entry inside `chart.html` (`<script type="application/json" id="chart-data">`). It holds the symbol image, IPA, spellings per language group, the syllable recording (`snd`) and example words. A cell without `snd` shows "no recording yet". To add a recording, put the file in `audio/cues/` and set that cell's `snd` to its path.

The symbol images were drawn with the script's glyph engine (`isibheqe-glyphs.js`, `isibheqe-rendering.js`, from isibheqe.org.za). The engine isn't in this repository and is never edited here.
