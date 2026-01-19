# Úkol: Úprava projektu na GitHub

Vaším cílem je vyzkoušet si reálný postup, jak se přispívá do cizího repozitáře přes **fork + pull request**. 
Nejprve si vytvoříte kopii (fork) tohoto repozitáře pod svým GitHub účtem, stáhnete si ji do počítače ve Visual Studiu, 
provedete úpravy a nakonec vytvoříte **Pull Request** (návrh na spojení změn) zpět do původního repozitáře.

## Co máte v projektu udělat
V projektu je ukázková stránka kontaktu učitele. Vy doplníte **svůj kontakt**:

1) Vytvořte stránku:
- soubor: `Pages/Kontakty/<VaseJmenoBezDiakritikyBezMezer>.cshtml`
- název souboru pište bez diakritiky a bez mezer, např. `NovakJan`, `SvobodaTomas`, `KralovaEma`

2) Do stránky napište svůj krátký medailonek:
- vaše jméno (nadpis)
- alespoň 1 věta o sobě
- volitelně avatar (profilový obrázek)

3) Přidejte avatar (pokud chcete):
- soubor do: `wwwroot/img/kontakty/<soubor>.png` (nebo .jpg)
- např. `wwwroot/img/kontakty/novak-jan.png`

4) Upravte `Pages/Index.cshtml`:
- do seznamu doplňte odkaz na svou stránku ve tvaru:
  ```html
  <li><a href="~/kontakty/NovakJan">Jan Novák</a></li>
---

# Návod: GitHub od nuly až po Pull Request (pro Visual Studio)

Tento návod vás provede celým postupem: **GitHub účet → fork repozitáře → stažení do PC (clone) → změny → commit → push → pull request**.

---

## 0) Založení GitHub účtu (kdo ho nemá)
1. Otevřete GitHub v prohlížeči a klikněte na **Sign up**.
2. Vyplňte e-mail, heslo a uživatelské jméno.
3. Dokončete registraci a **potvrďte e-mail** (přijde vám ověřovací zpráva).
4. Přihlaste se na GitHub (**Sign in**).

> Poznámka: účet je zdarma a stačí pro tento úkol.

---

## 1) Vytvoření forku (kopie repozitáře pod vaším účtem)
Fork znamená, že si uděláte **vlastní kopii** zdrojového repozitáře, do které můžete commitovat.

1. Otevřete v prohlížeči **původní repozitář** (tj. tento, odkaz v zadání).
2. Vpravo nahoře klikněte na tlačítko **Fork**.
3. Vyberte svůj GitHub účet jako **Owner** a potvrďte vytvoření forku.

✅ Výsledek: máte svůj repozitář např. `github.com/VaseJmeno/RepoName`.

---

## 2) Přihlášení do GitHubu ve Visual Studiu
1. Otevřete **Visual Studio**.
2. Přihlaste se do GitHubu:
   - klikněte na ikonku účtu (vpravo nahoře), nebo
   - **File → Account Settings** (případně „Sign in“).
3. Pokud se otevře okno v prohlížeči, dokončete přihlášení tam.

---

## 3) Stažení (Clone) vašeho forku do PC
Důležité: klonujte **svůj fork**, ne původní zadaný repozitář.

1. Ve Visual Studiu zvolte **Clone a repository**.
2. Vložte URL **svého forku** z GitHubu (např. `https://github.com/VaseJmeno/RepoName`).
3. Vyberte složku na disku a potvrďte **Clone**.
4. Otevřete řešení/projekt (Solution).

---

## 4) Vytvoření vlastní větve (branch)
Větev je oddělená “pracovní verze” vašich změn. Změny nedělejte přímo do `main`.

1. Ve Visual Studiu otevřete Git okna (např. **Git Changes** / **Git Repository**).
2. Vytvořte novou větev (New Branch), např.:
   - `kontakty/NovakJan`
   - `feature/kontakt-novakjan`
3. Přepněte se na tuto větev (Checkout), pokud to VS neudělá automaticky.

---

## 5) Proveďte změny v projektu
Upravte projekt podle zadání výše (přidání stránky kontaktu, obrázku a odkazu do Indexu).

---

## 6) Ověření, že změny fungují
1. Spusťte aplikaci (F5 nebo Ctrl+F5).
2. Ověřte, že vaše stránka jde otevřít a vše se zobrazuje správně.

---

## 7) Commit (uložení změn do historie)
Commit je “uložení změn” do lokální git historie na vašem počítači.

1. Otevřete **Git Changes**.
2. Zkontrolujte seznam změněných souborů.
3. Napište **Commit message** (stručně a smysluplně), např.:
   - `Přidána kontaktní stránka: Jan Novak`
4. Klikněte **Commit**.

> Tip: je lepší mít 1–2 menší commity než jeden obří.

---

## 8) Push (odeslání změn na GitHub)
Push odešle vaše commity na GitHub do vašeho forku.

1. Klikněte **Push** (v Git Changes nebo v horní liště Git).
2. Po push se vaše větev objeví na GitHubu ve vašem forku.

---

## 9) Pull Request (PR) – návrh na spojení do původního (učitelova) repozitáře
Pull Request je žádost: „Prosím, vezměte moje změny a spojte je do původního repozitáře.“

### Varianta A: vytvoření PR z Visual Studia
1. Po push se často objeví nabídka **Create Pull Request** (banner/infobar).
2. Pokud ne, najděte možnost vytvoření PR v Git nabídce nebo v Git okně.
3. Zkontrolujte, že cílení je správně:
   - **Base repository** = učitelův repozitář (původní)
   - **Base branch** = `main`
   - **Head repository** = váš fork
   - **Compare branch** = vaše větev (`kontakty/...`)
4. Vyplňte:
   - **Title**: např. `Kontakt: Jan Novak`
   - **Description**: 1–2 věty, co jste přidali
5. Klikněte **Create Pull Request**.

### Varianta B: vytvoření PR na GitHub webu (když se v IDE ztratíte)
1. Otevřete svůj fork na GitHubu.
2. Po push GitHub často nabídne tlačítko **Compare & pull request** – klikněte na něj.
3. Zkontrolujte stejné nastavení (base/head repozitář + větve) a vytvořte PR.

---

## 10) Odevzdání
Odevzdáváte **odkaz na Pull Request**, který jste vytvořili do původního (učitelova) repozitáře.

---

## Rychlý checklist (před odevzdáním)
- [ ] mám GitHub účet
- [ ] mám fork učitelova repozitáře
- [ ] naklonoval jsem svůj fork do PC
- [ ] pracuji ve své větvi (ne v `main`)
- [ ] provedl jsem změny podle zadání (přidání kontaktu)
- [ ] mám commit
- [ ] mám push
- [ ] mám vytvořený Pull Request do učitelova repozitáře
- [ ] odevzdávám odkaz na PR
