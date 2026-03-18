## User

اريدك ان تأتني بهيكل هذا الملف [@quran.json](file:///Users/hassan/001.Development/006.quran/quran.json)

## Assistant

<thinking>
The user wants me to describe the structure of the `quran.json` file based on the file outline provided. From the outline, I can see the structure clearly:

The file is an array of objects, where each object represents a Surah (chapter) of the Quran. Each Surah object has the following fields:
- `id` - the surah number
- `name` - the surah name (in Arabic likely)
- `transliteration` - the transliteration of the surah name
- `type` - the type (Meccan or Medinan)
- `total_verses` - total number of verses in the surah


- `verses` - an array of verse objects containing the verse id and text

So it's a comprehensive Quran dataset with all 114 surahs and their complete verse content organized hierarchically.
</thinking>

## هيكل ملف `quran.json`

الملف عبارة عن **مصفوفة (Array)** تحتوي على **114 عنصر** (كل عنصر يمثل سورة من سور القرآن الكريم).

كل سورة لها الهيكل التالي:

```/dev/null/schema.json#L1-20
[
  {
    "id": number,              // رقم السورة
    "name": string,            // اسم السورة بالعربية
    "transliteration": string, // النطق بالحروف اللاتينية
    "type": string,            // نوع السورة: "Meccan" أو "Medinan"
    "total_verses": number,    // عدد الآيات في السورة
    "verses": [                // مصفوفة الآيات
      {
        "id": number,          // رقم الآية
        "text": string         // نص الآية
      },
      ...
    ]
  },
  ...
]
```

### ملخص الهيكل:

| المستوى | الحقل | النوع | الوصف |
|---------|-------|-------|-------|
| السورة | `id` | `number` | رقم السورة (1-114) |
| السورة | `name` | `string` | اسم السورة |
| السورة | `transliteration` | `string` | النطق اللاتيني |
| السورة | `type` | `string` | مكية أو مدنية |
| السورة | `total_verses` | `number` | عدد الآيات |
| السورة | `verses` | `array` | مصفوفة الآيات |
| الآية | `id` | `number` | رقم الآية |
| الآية | `text` | `string` | نص الآية |

