# TODO

Nedodělané věci po rozšíření kapitol W2–W11 (listopad 2026).

## Ověřit před zveřejněním

- [ ] **Sestavit web lokálně** (`bundle exec jekyll serve`) a zkontrolovat vykreslení nových tabulek, rovnic a calloutů (`> [!NOTE]`, `> [!IMPORTANT]`, `> [!WARNING]`) – po úpravách nebylo ověřeno. Týká se kapitol 021, 031, 040, 041, 051, 060, 061, 100, 101, 110.
- [ ] Zvlášť zkontrolovat rovnice `$$ … $$` uvnitř calloutů (počítané příklady v `061_W6_Stream_Power_Index_application.md`).

## Obrázky

- [ ] **Autorská práva – W3** (`031_W3_long_prof.md`): nově vložené obrázky jsou skeny z učebnic včetně původních popisků. Rozhodnout, zda je lze zveřejnit na GitHub Pages, případně je překreslit nebo nahradit:
  - `figures/W3/long_profile.png` (Bierman & Montgomery, Key Concepts in Geomorphology)
  - `figures/W3/knickpoint_migration.png` (Burbank & Anderson, 2011)
  - `figures/W3/knickpoint_propagation.png` (Burbank & Anderson, 2011)
- [ ] Totéž zvážit u dříve použitých obrázků z Willett et al. (2014) ve W5 a Burbank & Anderson ve W4 (`slip_accumulation.png`).
- [ ] **Bierman & Montgomery** (`031`): doplnit rok a vydání do popisku obrázku a položku do seznamu literatury.
- [ ] **Laneova rovnováha** (`041_W4_…Indicators.md`): popisek obrázku `lane_balance.png` končí nedopsaným „Source“ – doplnit zdroj.
- [ ] **W5** (`051_W5_application_chi.md`): potvrdit záměnu prvního obrázku – místo duplicitního `victim_chi.jpg` je použit `drainage_divide.jpg`.
- [ ] `figures/W3/knickpoint.png` zůstává nepoužitý – vložit, nebo smazat.

## Literatura

- [ ] Překontrolovat citace doplněné bez DOI (psané zpaměti):
  - Bull & McFadden (1977), Hack (1973), Lane (1955), Keller & Pinter (2002) – `041`
  - Gilbert (1877) – `031`
  - Burbank & Anderson (2011) – `031`, `040`, `041`
  - England & Molnar (1990), Geology 18, 1173–1177 – `040` (DOI se nepodařilo ověřit)
- [ ] **W11** (`110_…Applied_Geomorphology.md`): u nepálské studie (Baglung District) doplnit autory a rok; zatím jen odkaz „source“.
- [ ] Sjednotit styl citací v `111_W11_Applications_Case_Studies.md` (stále odkazy typu „([ScienceDirect][10])“) s kapitolou 110.

## Obsah

- [ ] **W4 úvod** (`040`): potvrdit odstranění pasáže o geomorfologických markerech (je celá v `041`) a sloučení sekcí „Types of Tectonic Forcing“ a „Modes of tectonic forcing“.
- [ ] **W6** (`061`): počítané příklady používají ilustrativní hodnoty (ksn = 100 m^0.9, E = 0,1 mm/rok, K = 10⁻⁶); případně nahradit daty z reálného povodí.
- [ ] Křížové odkazy mezi kapitolami jsou jen textové („see W3“) – případně převést na skutečné odkazy.

## Kapitoly, které zatím nebyly procházeny

- [ ] `010_W1_systems.md`, `011_W1_quantitative.md`
- [ ] `020_W2_DEM_Terrain_metrics.md` (překlepy „there area“; sekce Runoff Processes je jen jeden odstavec)
- [ ] `030_W3_river_network.md` (v seznamu „Key geometric properties“ je dvakrát Bifurcation Ratio a duplicitně Stream Density / Drainage Density; chybí uzavírací závorka v popisku obrázku)
- [ ] `050_W5_Chi_Analysis.md` (sekce „Interpretation of Chi plots“ končí větou „Here's how to interpret Chi plots:“ bez pokračování)
- [ ] `070`, `071` (W7), `080`, `081` (W8), `090`, `091` (W9), `111` (W11), `120` (W12)
- [ ] `000-frontmatter/015-preface.md` je prázdný
- [ ] `020-seminars/W1-seminar.md` je jen zárodek (5 řádků)
