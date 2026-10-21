# Python hujjatlarining o'zbekcha tarjimasi

*[English summary below](#english-summary)*

Bu repo [Python rasmiy hujjatlari](https://docs.python.org/)ni o'zbek tiliga tarjima
qilish loyihasi. Tarjima [PEP 545](https://peps.python.org/pep-0545/) asosida olib boriladi.

> **Holat:** loyiha endigina boshlandi. Tarjima hali rasmiy emas va docs.python.org saytida chiqmaydi.

## Asosiy qoidalar

- **Yozuv:** lotin alifbosi.
- **Atamalar:** [TERMINOLOGY.md](TERMINOLOGY.md) faylidagi ro'yxatga amal qiling. Yangi atama
  kerak bo'lsa, avval o'sha faylga qo'shishni taklif qiling.
- **Tarjima qilinmaydi:** kod, kalit so'zlar (`for`, `None`, `True`), funksiya, klass va modul
  nomlari, reST belgilari (`:func:`, `:ref:`, ` ``...`` `, `|version|`).
- **Sifat:** asl matnga yaqin turing. Maqsad inglizcha hujjat darajasidagi sifat.
- **Mashina tarjimasi va AI:** faqat odam diqqat bilan tekshirgandan keyin ishlatish mumkin.

## Birinchi navbatdagi fayllar

Tarjima docs.python.org saytidagi til tanlash menyusiga kirishi uchun quyidagilar
to'liq tarjima qilingan bo'lishi kerak:

- [ ] `bugs.po`
- [ ] `tutorial/` papkasidagi barcha fayllar
- [ ] `builtins/functions.po`

## Qanday hissa qo'shish mumkin

1. Reponi fork qiling va `3.15` branchida ishlang.
2. Tarjima qilmoqchi bo'lgan faylingizni issue ochib band qiling, shunda bir faylni
   ikki kishi tarjima qilmaydi.
3. `.po` faylni [Poedit](https://poedit.net/) yoki istalgan matn muharririda tarjima qiling.
4. Tekshiring: `make sphinx-lint`
5. Pull request oching.

Ismingizni [TRANSLATORS](TRANSLATORS) fayliga qo'shishingiz mumkin.

## Lokal build

```sh
python3 -m venv .venv
source .venv/bin/activate
make            # birinchi marta CPythonni venv/cpython papkasiga klonlaydi
pip install -r venv/cpython/Doc/requirements.txt
make            # HTML venv/cpython/Doc/build/html ichida hosil bo'ladi
```

macOSda Makefile GNU `cp` buyrug'ini talab qiladi: `brew install coreutils`.

Boshqa buyruqlar: `make todo` (qolgan ishlar, `pip install potodo` kerak),
`make wrap` (qatorlarni qayta bo'lish, `pip install powrap` kerak).

## Aloqa

- [Python Docs Discord](https://discord.gg/h3qDwgyzga), `#translations` kanali
- [Discourse: Translations](https://discuss.python.org/c/documentation/translations/39)
- [Devguide: Translating](https://devguide.python.org/documentation/translations/translating/)

Koordinator: Asliddin

## English summary

This is the Uzbek (`uz`, Latin script) translation of the Python documentation,
following [PEP 545](https://peps.python.org/pep-0545/). The project has just started.
The first goal is to fully translate `bugs.po`, `tutorial/` and `builtins/functions.po`
so the translation can be added to the docs.python.org language switcher.

## Documentation Contribution Agreement

Python's documentation is maintained using a global network of volunteers. By posting this project on Transifex, Github, and other public places, and inviting you to participate, we are proposing an agreement that you will provide your improvements to Python's documentation or the translation of Python's documentation for the PSF's use under the CC0 license (available at https://creativecommons.org/publicdomain/zero/1.0/legalcode). In return, you may publicly claim credit for the portion of the translation you contributed and if your translation is accepted by the PSF, you may (but are not required to) submit a patch including an appropriate annotation in the TRANSLATORS file. Although nothing in this Documentation Contribution Agreement obligates the PSF to incorporate your textual contribution, your participation in the Python community is welcomed and appreciated.

You signify acceptance of this agreement by submitting your work to the PSF for inclusion in the documentation.
