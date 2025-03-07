---
lang: he-IL
layout: wiki
section: twilightmenu
category: customization
title: DSi / 3DS Skins - Custom SFX
description: כיצד להשתמש במוזיקת רקע מותאמת אישית ואפקטי סאונד בסקינים של DSi ו3DS עבור TWiLight Menu++
---

TWiLightMenu תומך בקבצי שמע מותאמים אישית בערכות הנושא. מקמו את קבצי השמע שלכם בתת התיקיה `sound` שבתיקיה ערכת הנושא שלכם, למשל עבור ערכת הנושא `white`, תמקמו את הקבצים ב`themes/white/sound/sfx.bin` וב`themes/sound/bgm.pcm.raw` בהתאמה. שתי הקבצים הם אופציונליים, אם אחד מהם חסר יהיה שימוש במוזיקת ברירת המחדל. לאחר מכן תשנו את הגדרת המוזיקה בהגדרות ל"Theme".

הוראות אלו מניחות שיש לכם את devkitPro מותקן עם mmutil. ניתן להשיג את devkitPro ב[אתר האינטרנט של devkitPro ](https://devkitpro.org/wiki/Getting_Started).

## בנק אפקטי צליל
בנק אפקטי הצליל מכיל אפקטי צליל שונים, לדוגמה צליל בחירת אייקון ועוד.

| קובץ        | תיאור                                                                      |
| ----------- | -------------------------------------------------------------------------- |
| startup.wav | מושמע בהפעלה. ראו את הפרק [צליל הפעלה](#startup-sound) למידע נוסף          |
| back.wav    | חזור                                                                       |
| launch.wav  | מושמע בהפעלה משחק                                                          |
| select.wav  | מושמע בהזזת סמן הבחירה                                                     |
| wrong.wav   | מושמע בהגעה לקצה העמוד                                                     |
| switch.wav  | מושמע בהעברת עמודים                                                        |
| stop.wav    | מושמע בערכת הנושא DSi כאשר סמן הבחירה מפסיק לזוז                           |
| bgm.pcm.raw | לא חלק מבנק הצלילים. ראו את הפרק [מוזיקת רקע בתפריט](#menu-bgm) למידע נוסף |

לאחר מכן תוכלו להריץ את `make` ליצירת בנק אפקטי הצליל. כל הקבצים המפורטים מעלה, מבלבד *bgm.pcm.raw* הכרחיים, אך ניתן להשתיקם.

קובץ *sfx.bin* הנוצר **חייב להיות מתחת ל512000B = 512 kB**. קובץ גדול יותר יגרום לקריסות או לחלק מהקבצים לא לנגן בצורה מלאה.

### צליל הפעלה
בעוד ששאר אפקטי הצליל יעבדו עם כל קובץ WAV, צליל ההפעלה חייב להיות בפורמט מסויים בשביל לעבוד כנדרש, אחרת יהיה פער בין סיום צליל ההפעלה לתחילת מוזיקת הרקע.

קובץ הstartup.wav חייב להיות **16-bit 16 kHz**. לדוגמה, ניתן להשתמש ב[Audacity](https://www.audacityteam.org/download/) להמרת הקובץ לפורמט הזה. כשהקובץ טעון בAudacity שנו את ה**Project Rate (Hz)** ל**16000**, לחצו על **Shift+M** ושנו את ה**Format** ל**16-bit PCM**.

אם הקובץ שלכם בסטריאו, לכו ל **Tracks > Mix > Mix Stereo down to Mono**.

חייב להגדיר את `PlayStartupJingle=1` ב `theme.ini` בשביל שצליל ההפעלה ינוגן.


## מוזיקת רקע בתפריט

מוזיקת רקע בתפריט צריכה להיות קובץ raw PCM עם ההגדרות **16-bit 16 kHz Mono**. לדוגמה, ניתן להשתמש ב[Audacity](https://www.audacityteam.org/download/) להמרת הקובץ לפורמט הזה. כשהקובץ טעון בAudacity שנו את ה**Project Rate (Hz)** ל**16000**, לחצו על **Shift+M** ושנו את ה**Format** ל**16-bit PCM**.

אם הקובץ שלכם בסטריאו, לכו ל **Tracks > Mix > Mix Stereo down to Mono**.

לייצוא בפורמט הנכון, בצעו:
1. בחרו ב `File` > `Export` > `Export Audio...`
1. הגדירו את `File Type` ל`Other uncompressed files`
1. הגדירו את `Header` ל`RAW (header-less)`
1. הגדירו את `Encoding` ל`Signed 16-bit PCM`
1. קבעו את שם המוצא ל`bgm.pcm.raw` ולחצו על `Save`
1. לחצו על `OK` לעריכת הmetadata

עכשיו יש לכם קובץ `bgm.pcm.raw` שניתן להעתיק לתת התיקייה *sound* בתיקיית ערכת הנושא שלכם.

בניגוד לsfx.bin, גודלו של *bgm.pcm.raw* יכול להיות בכל גודל.
