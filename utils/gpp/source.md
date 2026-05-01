

#mode standard cpp
/* ======================
        Quran Related
   ======================*/
#mode standard tex

\define{\qref{surahName}{surahNumber}{ayahNumber}}{(\surahName, Q\surahNumber:\ayahNumber)}
\define{\qrefl{surahName}{surahNumber}{ayahNumber}}{(al-\surahName, Q\surahNumber:\ayahNumber)}

\define{\quran{arabic}{translation}{reference}}{
::: {custom-style="Quran Arabic" dir="rtl"}
\arabic
:::

::: {custom-style="Quran Translation"}
«\translation@»
:::

::: {custom-style="Quran Reference"}
\reference
:::
}

\mode{standard}{cpp}
/* ======================
        Ḥadīth Related
   ======================*/
#mode standard tex

\define{\hadith{arabic}{english}}{
::: {custom-style="Hadith Arabic" dir="rtl"}
\arabic
:::

::: {custom-style="Hadith English"}
\english
:::
}

\mode{standard}{cpp}
/* ======================
        Translation related
   ======================*/
#mode standard tex

\define{\trans{arabic}{english}}{

\ifndef{FINAL}
::: {custom-style="Arabic Source" dir="rtl"}
\arabic
:::

::: {custom-style="English Target"}
\english
:::
\else
\english
\endif
}

\define{\note{text}}{\ifdef{NOTE}[TRANS: \text]{custom-style="Highlight C1"}\else%DEL\endif}

\define{\c1{text}}{[\text]{custom-style="Highlight C1"}}
\define{\c2{text}}{[\text]{custom-style="Highlight C2"}}
\define{\c3{text}}{[\text]{custom-style="Highlight C3"}}
\define{\c4{text}}{[\text]{custom-style="Highlight C4"}}
\define{\warn{text}}{[\text]{custom-style="Highlight Warn"}}

\mode{standard}{cpp}
/* ======================
        Miscellaneous
   ======================*/
#mode standard tex

\define{\bodyArabic{arabic}}{
::: {custom-style="Body Text Arabic" dir="rtl"}
\arabic
:::
}

\define{\year{year}}{\year[h]{.smallcaps}}
\define{\dyear{year}}{d.\year[h]{.smallcaps}}
\define{\yearrange{beginyear}{endyear}}{\beginyear--\endyear[h]{.smallcaps}}

\define{\ITA{arabic}}{[\arabic]{dir="rtl" custom-style="In-text Arabic"}}
\defin{\IFA{arabic}}{[\arabic]{dir="rtl" custom-style="In-footnote Arabic"}}

\define{\SC{text}}{[\text]{.smallcaps}}

\mode{standard}{cpp}

#ifndef INT
#define ALI ʿAlī
#else
#define ALI ʿAlīyyu
#endif

/* ======================
        OpenXML
   ====================== */

#mode standard tex

\define{\pagebreak}{
```@{=openxml@}
<w:p>
    <w:r>
        <w:br w:type="page"/>
    </w:r>
</w:p>
```
}

\mode{standard}{cpp}

/* ======================
        Honorifics
   ======================*/

#define SWT ([سبحانه وتعالى]{lang=ar})
#define PBUH ([صلى الله عليه وسلم]{lang=ar})
#define P_HIM ([رضي الله عنه]{lang=ar})
#define P_HER ([رضي الله عنها]{lang=ar})
#define P_TWO ([رضي الله عنهما]{lang=ar})
#define P_THM ([رضي الله عنهم]{lang=ar})
#define M_HIM ([رحمه الله تعالى]{lang=ar})

#define HPBUH ([صلى الله عليه وسلم]{custom-style="kHeader Honorifics"})
#define HS_HIM ([عليه السلام]{custom-style="kHeader Honorifics"})

#define HSS_HIM ([عليه الصلاة والسلام]{custom-style="kHeader Honorifics"})
#define HSS_TWO ([عليهما الصلاة والسلام]{custom-style="kHeader Honorifics"})

#define BSWT ([سبحانه وتعالى]{custom-style="kBody Honorifics"})
#define BAWJ ([عزَّ وجلَّ]{custom-style="kBody Honorifics"})
#define BBSWT [[سبحانه وتعالى]{custom-style="kBody Honorifics"}]
#define BPBUH ([صلى الله عليه وسلم]{custom-style="kBody Honorifics"})
#define BBPBUH [[صلى الله عليه وسلم]{custom-style="kBody Honorifics"}]
#define BP_HIM ([رضي الله عنه]{custom-style="kBody Honorifics"})
#define BP_HER ([رضي الله عنها]{custom-style="kBody Honorifics"})
#define BP_TWO ([رضي الله عنهما]{custom-style="kBody Honorifics"})
#define BP_THM ([رضي الله عنهم]{custom-style="kBody Honorifics"})
#define BM_HIM ([رحمه الله تعالى]{custom-style="kBody Honorifics"})
#define BM_TWO ([رحمهما الله تعالى]{custom-style="kBody Honorifics"})
#define BM_THM ([رحمهم الله تعالى]{custom-style="kBody Honorifics"})
#define BS_HIM ([عليه السلام]{custom-style="kBody Honorifics"})
#define BSS_THM ([عليهم الصلاة والسلام]{custom-style="kBody Honorifics"})
#define BSS_HIM ([عليه الصلاة والسلام]{custom-style="kBody Honorifics"})
#define BH_HIM ([حفظه الله تعالى]{custom-style="kBody Honorifics"})

#define FSWT ([سبحانه وتعالى]{custom-style="kFootnotes Honorifics"})
#define FAWJ ([عزَّ وجلَّ]{custom-style="kFootnotes Honorifics"})
#define FPBUH ([صلى الله عليه وسلم]{custom-style="kFootnotes Honorifics"})
#define FM_HIM ([رحمه الله تعالى]{custom-style="kFootnotes Honorifics"})

#define pyTimeHijri #exec python ./utils/python/_pyTimeHijri.py
#define printDate #date (%a) %d %b %Y %I:%M%p

/* ==========================
        DOCUMENT METADATA
   ==========================*/
#mode standard cpp
#mode user "\\" "" "{" "}{" "}" "{" "}" "#" ""
#mode string iii "\"" "\"" "\\"
#mode string iii "'" "'" "\\"
#mode comment "%\n" ""
