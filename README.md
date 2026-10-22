# Navbahor Group — Xodimlar almashinuvi (Attrition) tahlili

![Dashboard](dashboard.jpg)

Kompaniyada xodimlar nega va qayerda ko'proq ketayotganini aniqlash uchun HR ma'lumotlarini tozalab, tahlil qildim va Excelda interaktiv dashboard yasadim.

> **Eslatma:** ma'lumotlar sun'iy yaratilgan (sintetik dataset), haqiqiy kompaniyaga tegishli emas. Loyiha o'quv va portfolio maqsadida qilingan.

## Maqsad

Quyidagi savollarga javob topish:

- Kompaniyada ketish foizi (attrition) qancha?
- Qaysi bo'limda xodimlar ko'proq ketadi?
- Yangi xodimlar ko'proq ketadimi?
- Xodimlar asosan nega ketadi?
- Ketganlarning oyligi qolganlarnikidan farq qiladimi?

## Ma'lumot haqida

| Ko'rsatkich | Qiymat |
|---|---|
| Xodimlar soni | 800 (tozalashdan keyin) |
| Bo'limlar | 7 ta (Sotuv, Marketing, IT, Moliya, HR, Logistika, Mijozlar xizmati) |
| Holat sanasi | 2026 yil 30-sentabr |
| Ustunlar | Bo'lim, lavozim, daraja, oylik, baholar, ish formati, ketgan/ketmagan, ketish sababi va boshqalar |
| Valyuta | So'm (UZS) |

## Qilingan ishlar

1. **Ma'lumotni tozalash (Power Query)**
   - Takroriy qatorlarni o'chirdim (810 → 800).
   - Bo'lim va jins nomlarini standartlashtirdim.
   - Oyliklardagi 3 ta g'ayritabiiy qiymatni (ortiqcha nol xatosi, 43–89 mln so'm) darajaga mos holda 10 ga bo'lib tuzatdim.
   - Samaradorlik bahosidagi bo'sh qiymatlarni (~2%) o'zgartirmadim: o'rtacha hisoblashda ular hisobga olinmaydi.
2. **Yangi ustunlar (formulalar)**
   - Yosh (`DATEDIF`), Staj (ketgan xodimlar uchun ketgan sanagacha), Yosh va Staj guruhlari (`IF`), Bo'lim rahbari (`XLOOKUP`), Ketdi (1/0).
3. **Pivot Table va PivotChart**
   - Ketish foizi: `Ketdi` ustunining o'rtachasi orqali, bo'lim, staj, sabab va oylik bo'yicha.
4. **Interaktiv dashboard**
   - KPI kartalar: jami xodim, ketganlar soni, ketish foizi, o'rtacha oylik.
   - 4 ta diagramma va 2 ta Slicer (Bo'lim, Ish formati).
5. **Xulosa va tavsiyalar**

## Ishlatilgan vositalar

- Microsoft Excel
- Power Query (ma'lumotni tozalash)
- Pivot Table, PivotChart, Slicer
- `DATEDIF`, `IF`, `XLOOKUP`, `COUNTIF`, `AVERAGE`

## Asosiy topilmalar

- Umumiy **ketish foizi 17,9%** (800 xodimdan 143 tasi ketgan).
- **Mijozlar xizmatida** ketish eng yuqori: 23,2%, kompaniya o'rtachasidan taxminan 5 punkt ko'p. HR (9,1%) va Marketingda (10,8%) eng past.
- **Yangi xodimlar** ko'proq ketadi: birinchi yilda 25%, 3 yildan ko'p ishlaganlarda 14%.
- **Asosiy sabablar:** karyera o'sishi yo'qligi (30), rahbar bilan muammo (29) va past maosh (27). Ular jami ketishlarning taxminan 60% ini tashkil qiladi.
- Ketganlarning o'rtacha oyligi qolganlarnikidan past. Bu bog'liqlikni ko'rsatadi, lekin sabab ekanini isbotlamaydi: maosh ketganlarning atigi 27 tasi uchun asosiy sabab.

## Tavsiyalar

1. **Mijozlar xizmatida** maosh, ish yuklamasi va karyera yo'lini ko'rib chiqish.
2. **Birinchi yil uchun** adaptatsiya dasturi va mentor tizimini joriy qilish.
3. **Rahbarlar uchun** trening va xodimlar bilan muntazam birma-bir uchrashuvlar o'tkazish.
4. **Past oylikli xodimlarning** maoshini bozor darajasi bilan solishtirish.

## Repository tuzilishi

```
hr-attrition-analysis/
├── README.md
├── NavbahorGroup_HR_Dashboard.xlsx
└── dashboard.jpg
```

### Excel fayl varaqlari

| Varaq | Mazmuni |
|---|---|
| `Dashboard` | Interaktiv dashboard |
| `Pivots` | Dashboard uchun Pivot jadvallar |
| `HR_Clean` | Tozalangan ma'lumot (Power Query natijasi) |
| `HR_Raw` | Xom ma'lumot |
| `Bolimlar` | Bo'lim rahbarlari ma'lumotnomasi |
| `Data_Dictionary` | Ustunlar izohi |

## Faylni ochish bo'yicha eslatma

Dashboard to'liq ishlashi uchun faylni **Microsoft Excel**da oching (Slicer va PivotChart boshqa dasturlarda to'g'ri ishlamasligi mumkin).

## Cheklovlar

- Ma'lumotlar sintetik, shuning uchun topilmalar real kompaniyaga umumlashtirilmaydi.
- Kichik guruhlarda (masalan, bitta bo'lim va bitta ish formati birga tanlanganda) foizlar tasodifiy o'zgarishi mumkin.

## Keyingi qadamlar

- Ma'lumotni SQL ga yuklab, so'rovlar bilan tahlil qilish.
- Dashboardni Power BI da qayta yasash.
- Python (pandas) bilan ketishni bashorat qiluvchi oddiy model qurish.

## Muallif

**[Ismingiz Familiyangiz]**
LinkedIn: [havola]
Email: [pochta]
