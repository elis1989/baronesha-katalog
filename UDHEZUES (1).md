# 📘 Baronesha Catalog — Udhëzues

## Çfarë ka të re në këtë version

- ✨ **Logo dhe ngjyrat e Baroneshës** (ar + zi, dizajn luksoz)
- 🔒 **Toggle për çmimet** — ti vendos nëse klientët shohin çmimet apo jo
- 🎨 Tipografi serife (Cormorant Garamond) për një ndjenjë premium

---

## 🔒 Si funksionon toggle-ja e çmimeve

Te admin-i (`epic_catalog_editor.html`), lart djathtas, ke një **switch** te butoni "Çmimet ON/OFF":

| Statusi | Çfarë sheh ti (admin) | Çfarë shohin klientët |
|---------|----------------------|----------------------|
| **ON** (ar) | Çmimet plotësisht të redaktueshme | Çmimet shfaqen normalisht |
| **OFF** (gri) | Çmimet plotësisht të redaktueshme | "Kërkoni çmimin · Kontaktoni" |

Kliko mbi switch-in për të ndryshuar.

> 💡 Ti **gjithmonë** i sheh çmimet në admin, edhe kur toggle është OFF. Vetëm klientët në katalogun publik nuk i shohin.

⚠️ **E rëndësishme**: Statusi i toggle-jës ruhet në skedarin `catalog.json` kur kliko **Export JSON**. Pra:
1. Vendos toggle ON ose OFF në admin
2. Kliko **⬇ Export JSON**
3. Ngarko skedarin në GitHub
4. Klientët shohin gjendjen e re

---

## ✏️ Hapi 1 — Krijo repository (vetëm një herë)

1. Hyr në **github.com**, kliko **+** → **New repository**
2. Emri: `baronesha-katalog`
3. Zgjidh **Public**
4. **Create repository**

## 📤 Hapi 2 — Ngarko skedarët (vetëm një herë)

Tërhiq dhe lësho këto 4 skedarë në repository:

| Skedari | Kush e sheh |
|---------|-------------|
| `index.html` | Klientët |
| `catalog.json` | Klientët |
| `epic_images.js` | Klientët |
| `epic_catalog_editor.html` | Vetëm ti |

Pastaj **Commit changes**.

## 🌐 Hapi 3 — Aktivizo GitHub Pages (vetëm një herë)

1. **Settings** → **Pages**
2. **Branch**: `main` → **Save**
3. Prit ~1 minutë → merr linkun:
   - Klientët: `https://USERNAME.github.io/baronesha-katalog/`
   - Admin (vetëm ti): `https://USERNAME.github.io/baronesha-katalog/epic_catalog_editor.html`

---

## 🔄 Workflow-i i përditshëm

**A. Modifikon (lokalisht ose online)**
1. Hap `epic_catalog_editor.html`
2. Ndrysho çmime, foto, ose vendos toggle çmimesh ON/OFF
3. Kliko **⬇ Export JSON** lart djathtas

**B. Ngarkon në GitHub**
1. Riemërto skedarin e shkarkuar nga `catalog.json` (zakonisht është emri standard)
2. Shko në repository → kliko mbi `catalog.json` ekzistues → ngarkoje sërish
3. **Commit changes**

**C. Klientët shohin ndryshimet**
- Brenda 1 minute pasi bën commit, faqja online është përditësuar.

---

## 📋 Skedarët në këtë paketë

| Skedari | Përdorimi |
|---------|-----------|
| `UDHEZUES.md` | Ky udhëzues |
| `index.html` | **Faqja për klientët** (vetëm shikim, logo Baronesha) |
| `catalog.json` | Të dhënat (përmban edhe statusin ON/OFF të çmimeve) |
| `epic_images.js` | Fotot e produkteve |
| `epic_catalog_editor.html` | **Editori yt privat** (me toggle çmimesh) |

---

## ❓ Pyetje të zakonshme

**A do shohin klientët çmimet edhe nëse e fsheh në admin?**
Jo. Kur toggle është OFF dhe ti bën Export JSON + Upload në GitHub, çmimet janë të padukshme për klientët. Në vend të çmimit shfaqet "Kërkoni çmimin · Kontaktoni".

**Çfarë ndodh nëse harroj të bëj Export JSON pas ndryshimit?**
Ndryshimet ruhen vetëm në browser-in tënd. Klientët shohin versionin e fundit që ke ngarkuar në GitHub. Pra: **kurdoherë që ndryshon diçka rëndësishme → Export → Upload**.

**A mund ta përdor toggle-jën edhe për një produkt të vetëm?**
Versioni aktual e bën globalisht (të gjitha ose asnjë). Nëse do toggle për produkt të veçantë, më thuaj dhe e shtoj.
