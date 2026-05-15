# 📘 Udhëzues: Si ta hedh katalogun online (GitHub Pages)

## Çfarë do bësh
- Ngarkon skedarët në GitHub (5 minuta një herë)
- Aktivizon GitHub Pages (1 minutë një herë)
- Merr një link që e dërgon te klientët
- Sa herë që ndryshon çmimet, ngarkon vetëm `catalog.json` (30 sekonda)

---

## ✏️ Hapi 1 — Krijo repository-n (vetëm një herë)

1. Hyr në **github.com** dhe logohu.
2. Lart djathtas, kliko **+** → **New repository**
3. Te **Repository name** shkruaj: `baronesha-katalog` (ose çfarë do)
4. Zgjidh **Public** ⚠️ (e rëndësishme, falas vetëm publike)
5. **MOS** zgjidh asnjë opsion tjetër (pa README, pa .gitignore)
6. Kliko **Create repository**

---

## 📤 Hapi 2 — Ngarko skedarët (drag & drop)

1. Në faqen e repository-t të porsa-krijuar, kliko linkun **"uploading an existing file"** (në mes të faqes)
2. Tërhiq dhe lësho këto 4 skedarë në kuti (ose kliko "choose your files"):
   - `index.html` (faqja për klientët)
   - `catalog.json` (të dhënat — çmime, emra)
   - `epic_images.js` (fotot e produkteve)
   - `epic_catalog_editor.html` (editori yt privat — opsional, vetëm nëse do ta përdorësh online edhe ti)
3. Pasi të ngarkohen të katra, poshtë faqes kliko **Commit changes**

---

## 🌐 Hapi 3 — Aktivizo GitHub Pages (vetëm një herë)

1. Në repository, lart kliko **Settings**
2. Në menu majtas, kliko **Pages**
3. Te **"Branch"** zgjidh **`main`** (nga dropdown-i që thotë "None")
4. Lëre **`/ (root)`** për folder
5. Kliko **Save**
6. Prit ~1 minutë. Sipër do shfaqet kutia e gjelbër: **"Your site is live at https://USERNAME.github.io/baronesha-katalog/"**

🎉 **Ky është linku që u jep klientëve!**

> ⚠️ Linku admin (editori yt) është:
> `https://USERNAME.github.io/baronesha-katalog/epic_catalog_editor.html`
>
> Mos ua jep klientëve. Mbaje vetëm për ty.

---

## 🔄 Hapi 4 — Workflow-i i përditshëm (kur ndryshon çmimet)

Sa herë që ndryshon diçka:

### A. Modifikon lokalisht
1. Hap `epic_catalog_editor.html` në kompjuter (siç bën tani)
2. Ndrysho çmimet/produktet/fotot
3. Kliko **⬇ Export JSON** lart djathtas
4. Të shkarkohet skedari `epic_catalog_week20.json`

### B. Ngarkon në GitHub
1. Riemërto skedarin e shkarkuar nga **`epic_catalog_week20.json`** → **`catalog.json`**
2. Shko në repository-n tënd në GitHub
3. Kliko mbi skedarin ekzistues **`catalog.json`** (në listën e skedarëve)
4. Kliko ikonën e laptopit në krye (✏️ ose "Edit"), pastaj **Upload files** ose tërhiqe direkt
5. Konfirmo me **Commit changes**

### C. Klientët shohin ndryshimet
- Brenda ~1 minute, faqja online është përditësuar.
- Klientët mund të rifreskojnë faqen për të parë çmimet e reja.

---

## 💡 Këshilla

- **Backup automatik**: Çdo ndryshim në GitHub ruhet me historik. Mund të kthehesh mbrapa në çdo version të mëparshëm.
- **Përdorim nga telefoni**: Edhe nga celular mund ta hapësh `epic_catalog_editor.html` direkt nga GitHub Pages (linku admin), por më e lehtë është nga kompjuteri.
- **Linku më i bukur**: Nëse do një emër më profesional (p.sh. `katalog.baronesha.com`), GitHub Pages mbështet domain personal. Mund të blesh një domain (10€/vit) dhe ta lidhësh.
- **Fotot e mëdha**: Skedari `epic_images.js` është ~1.5 MB. Klientët e shkarkojnë një herë; pastaj e mban browser-i në cache.

---

## ❓ Probleme të mundshme

**Klientët shohin versionin e vjetër** → Thuaju të bëjnë "Hard refresh" (Ctrl+Shift+R në Windows, Cmd+Shift+R në Mac).

**Faqja shfaq "Gabim në ngarkim"** → Sigurohu që `catalog.json` është në të njëjtin folder me `index.html` në GitHub.

**Fotot nuk shfaqen** → Sigurohu që `epic_images.js` është ngarkuar gjithashtu.

---

## 📞 Skedarët që duhet të ngarkosh

| Skedari | Kush e sheh | Çfarë bën |
|---------|-------------|-----------|
| `index.html` | Klientët | Faqja kryesore (vetëm shikim) |
| `catalog.json` | Klientët | Të dhënat (çmime, produkte) |
| `epic_images.js` | Klientët | Fotot e produkteve |
| `epic_catalog_editor.html` | Vetëm ti | Editori për të ndryshuar |
