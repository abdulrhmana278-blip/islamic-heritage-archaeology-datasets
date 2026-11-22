# islamic-heritage-archaeology-datasets
---
license: cc-by-4.0
language:
  - ar
task_categories:
  - question-answering
  - text-generation
  - text-classification
  - token-classification
pretty_name: Islamic Heritage & Archaeology Dataset (2.4M Records)
tags:
  - islamic-heritage
  - archaeology
  - islamic-history
  - islamic-architecture
  - epigraphy
  - cultural-heritage
  - artifacts
  - nlp
size_categories:
  - 1M<n<10M
---

# مجموعة بيانات الآثار والتاريخ والتراث الإسلامي
### (Islamic Heritage & Archaeology Dataset)

## نظرة عامة (Overview)

تُقدّم هذه المجموعة بنية بيانات غنية ومُهيكلة بصيغة **JSONL** تضم **2,400,000 سجل** (بواقع **300,000 سجل** في كل ملف من **8 ملفات متخصصة**) وحجم إجمالي **1,623.86 MB**، لتغطية محاور الآثار الإسلامية، العمارة، النقوش الكتابية، المواقع التاريخية، الأسئلة المعرفية، المسارات التراثية، العصور التاريخية، والمواد والحرف التقليدية.

تم توليد هذه البيانات عبر محرك توليد برمجي متخصص يراعي المصطلحات الأثرية والمعمارية والتاريخية، ويوفّر حقولاً منظمة وقابلة للتوسع تجعل المجموعة مناسبة لتدريب وتقييم نماذج اللغة (**LLMs**)، وبناء المساعدين المعرفيين، وتطبيقات التراث الرقمي (**Digital Heritage**)، وأنظمة الفهرسة والبحث الأثري والثقافي.

---

## ملخص إحصاءات المجموعة (Dataset Statistics)

- **إجمالي السجلات:** `2,400,000` سجل
- **الحجم الإجمالي للملفات:** `1,623.86 MB`
- **عدد الملفات:** `8` ملفات (`JSONL`، ترميز `UTF-8`)
- **الترخيص:** `CC BY 4.0`

| # | الملف | المحور الأثري / التاريخي | عدد السجلات | الحجم |
| :---: | :--- | :--- | :---: | :---: |
| 1 | `islamic_heritage_artifacts.jsonl` | السجلات الأثرية (Artifacts) | 300,000 | 303.71 MB |
| 2 | `islamic_heritage_architectural_terms.jsonl` | المصطلحات المعمارية (Architectural Terms) | 300,000 | 130.69 MB |
| 3 | `islamic_heritage_epigraphy.jsonl` | النقوش الكتابية (Epigraphy) | 300,000 | 154.16 MB |
| 4 | `islamic_heritage_sites.jsonl` | المواقع التاريخية (Historical Sites) | 300,000 | 187.88 MB |
| 5 | `islamic_heritage_qa.jsonl` | الأسئلة المعرفية (Heritage QA) | 300,000 | 178.11 MB |
| 6 | `islamic_heritage_itineraries.jsonl` | خطط الرحلات التراثية (Heritage Itineraries) | 300,000 | 303.95 MB |
| 7 | `islamic_heritage_eras.jsonl` | معلومات العصور (Historical Eras) | 300,000 | 227.94 MB |
| 8 | `islamic_heritage_materials.jsonl` | المواد التقليدية (Traditional Materials) | 300,000 | 137.47 MB |

---

## توافر البيانات (Data Availability)

المجموعة متاحة مجاناً على المنصتين التاليتين:

| المنصة | الرابط |
| :--- | :--- |
| 🤗 **Hugging Face** | [Abdulrhman472001/islamic-heritage-archaeology-dataset](https://huggingface.co/datasets/Abdulrhman472001/islamic-heritage-archaeology-dataset) |
| 📊 **Kaggle** | [abdulrhmanamr47/islamic-heritage-archaeology-dataset](https://www.kaggle.com/datasets/abdulrhmanamr47/islamic-heritage-archaeology-dataset) |

- **Hugging Face:** https://huggingface.co/datasets/Abdulrhman472001/islamic-heritage-archaeology-dataset
- **Kaggle:** https://www.kaggle.com/datasets/abdulrhmanamr47/islamic-heritage-archaeology-dataset

---

## القيمة العلمية والتقنية للبيانات (Why This Dataset Matters)

1. **ترابط التخصص الأثري بالتاريخ والعمارة والفنون:** تربط المجموعة بين القطعة الأثرية (`artifacts`) من حيث المادة والتقنية والأبعاد والنقش والخط والحالة، وبين العصر التاريخي (`eras`)، والموقع (`sites`)، والمصطلح المعماري (`architectural_terms`)، مما يوفّر سياقاً معرفياً متكاملاً.
2. **معالجة النقوش والكتابات التاريخية:** يضم ملف `islamic_heritage_epigraphy.jsonl` سجلات تربط نوع النقش (`ديني`، `تمجيدي`، `تاريخي`) والخط والعصر بالنص وقراءته الحديثة (`modern_transcription`) والملاحظات التاريخية، وهو ما يخدم تطبيقات قراءة وتحليل النقوش والتراث الكتابي.
3. **تغطية السياحة الثقافية والمسارات التراثية:** يقدّم ملف `islamic_heritage_itineraries.jsonl` خططاً يومية منظمة (`daily_plan`) وأبرز المعالم والاهتمامات (`highlights`) للرحلات التراثية، مما يدعم تطبيقات الإرشاد السياحي والتخطيط الثقافي.
4. **بنية JSONL نظيفة وقابلة للتكامل:** تأتي جميع الملفات بصيغة `JSONL` بترميز `UTF-8` مع مفاتيح واضحة وحقول هيكلة دقيقة تسهل استخدامها في التدريب، الضبط الدقيق (**Fine-Tuning**)، والتقييم (**Benchmarking**).

---

## هيكل الملفات الثمانية وتفاصيلها (Dataset Structure)

### 1. السجلات الأثرية (`islamic_heritage_artifacts.jsonl`)

- **الهدف:** وصف القطع الأثرية والتحف والمخطوطات الإسلامية من حيث العصر، الفئة، المادة، التقنية، الأبعاد، النقش الكتابي، الحالة، والوصف التفصيلي.
- **الحقول الأساسية:** `id`, `type`, `artifact_id`, `artifact_name`, `category`, `era`, `era_period`, `origin_region`, `material`, `technique`, `dimensions`, `inscription_type`, `inscription_script`, `inscription_text`, `description`, `condition`, `tags`, `current_location`.

### 2. المصطلحات المعمارية (`islamic_heritage_architectural_terms.jsonl`)

- **الهدف:** توثيق المصطلحات المعمارية الإسلامية وتعريفها ووظيفتها ومواضعها والعصور التي برزت فيها.
- **الحقول الأساسية:** `id`, `type`, `term`, `definition`, `function`, `locations`, `eras`, `tags` (مع دعم `types` عند توفرها).

### 3. النقوش الكتابية (`islamic_heritage_epigraphy.jsonl`)

- **الهدف:** تقديم أزواج نقوش كتابية حسب النوع والخط والعصر مع النص، المقابل الكتابي الحديث، والملاحظات التاريخية.
- **الحقول الأساسية:** `id`, `type`, `inscription_type`, `script`, `era`, `simulated_inscription`, `modern_transcription`, `historical_notes`, `tags`.

### 4. المواقع التاريخية (`islamic_heritage_sites.jsonl`)

- **الهدف:** وصف المعالم والمواقع الأثرية والتاريخية من حيث النوع، المدينة، العصر، الفترة الزمنية، السمات المعمارية، والوصف العام.
- **الحقول الأساسية:** `id`, `type`, `site_name`, `site_type`, `city`, `era`, `era_period`, `description`, `features`, `tags`.

### 5. الأسئلة المعرفية (`islamic_heritage_qa.jsonl`)

- **الهدف:** توفير أسئلة وإجابات معرفية حول العمارة والفنون والحرف والتاريخ الإسلامي لدعم مهام الإجابة عن الأسئلة وبناء المساعدين المتخصصين.
- **الحقول الأساسية:** `id`, `type`, `question`, `answer`, `category`, `tags`.

### 6. خطط الرحلات التراثية (`islamic_heritage_itineraries.jsonl`)

- **الهدف:** بناء جداول وبرنامج زيارات يومي للوجهات التراثية مع إبراز المحاور الثقافية والفنية والمعمارية.
- **الحقول الأساسية:** `id`, `type`, `destination`, `duration_days`, `theme`, `daily_plan`, `highlights`, `tags`.

### 7. معلومات العصور (`islamic_heritage_eras.jsonl`)

- **الهدف:** تلخيص العصور التاريخية الإسلامية من حيث الفترة الزمنية، العاصمة، الخصائص، الإنجازات، الأقاليم، والملخص العام.
- **الحقول الأساسية:** `id`, `type`, `era_name`, `period`, `capital`, `characteristics`, `achievements`, `regions`, `summary`.

### 8. المواد التقليدية (`islamic_heritage_materials.jsonl`)

- **الهدف:** تعريف الخامات والمواد التقليدية المستخدمة في الفنون والحرف الإسلامية وتقنيات تشكيلها والعصور المرتبطة بها والمنتجات الشائعة.
- **الحقول الأساسية:** `id`, `type`, `material_name`, `description`, `techniques`, `eras_used`, `typical_objects`, `tags`.

---

## أمثلة من السجلات (Data Samples)

**مثال من السجلات الأثرية (Artifacts):**

```json
{
  "id": 1,
  "type": "artifact_record",
  "artifact_id": "ART-45821",
  "artifact_name": "إبريق النحاس الأصفر",
  "category": "أواني_منزلية",
  "era": "العصر المملوكي",
  "era_period": "1250-1517م",
  "origin_region": "مصر",
  "material": "النحاس الأصفر",
  "technique": "التعشيق بالفضة",
  "dimensions": "الارتفاع: 25 سم، القطر: 15 سم",
  "inscription_type": "ديني",
  "inscription_script": "الثلث",
  "inscription_text": "بسم الله الرحمن الرحيم",
  "description": "إبريق من النحاس الأصفر، يعود إلى العصر المملوكي. يتميز بـ التعشيق بالفضة دقيق. يحمل نقشاً ديني بالخط الثلث. الزخرفة تتكون من أنماط هندسية. الحالة العامة: جيدة جداً.",
  "condition": "جيدة جداً",
  "tags": ["العصر المملوكي", "النحاس الأصفر", "أواني_منزلية", "الثلث", "فن_إسلامي"],
  "current_location": "متحف افتراضي للتراث الإسلامي"
}
```

**مثال من النقوش الكتابية (Epigraphy):**

```json
{
  "id": 2,
  "type": "epigraphy_pair",
  "inscription_type": "تمجيدي",
  "script": "الثلث",
  "era": "العصر المملوكي",
  "simulated_inscription": "العز لمولانا السلطان قايتباي",
  "modern_transcription": "العِزُّ لمولانا السلطان قايتباي",
  "historical_notes": "صيغة تمجيد شائعة في العصر المملوكي",
  "tags": ["نقوش", "خط_عربي", "فن_إسلامي", "تمجيدي"]
}
```

**مثال من خطط الرحلات التراثية (Itineraries):**

```json
{
  "id": 1,
  "type": "heritage_itinerary",
  "destination": "القاهرة",
  "duration_days": 5,
  "theme": "رحلة تراثية إسلامية",
  "daily_plan": [
    "اليوم 1: زيارة المساجد التاريخية في القاهرة صباحاً، وجولة في الأسواق القديمة مساءً.",
    "اليوم 2: زيارة المتاحف الإسلامية صباحاً، واستكشاف القصور الأثرية مساءً.",
    "اليوم 3: التعرف على فن الخط العربي صباحاً، وزيارة المدارس التاريخية مساءً.",
    "اليوم 4: مشاهدة ورش الحرف التقليدية صباحاً، وجولة في الأحياء القديمة مساءً.",
    "اليوم 5: زيارة الحمامات التاريخية صباحاً، واستكشاف القلاع والأسوار مساءً."
  ],
  "highlights": ["آثار العصر المملوكي", "فنون الخط والزخرفة", "العمارة الإسلامية", "الحرف التقليدية"],
  "tags": ["القاهرة", "سياحة_تراثية", "فن_إسلامي"]
}
```

---

## استخدامات مقترحة (Use Cases)

- **تدريب النماذج اللغوية المتخصصة (SFT & Domain LLMs):** بناء نماذج تفهم المصطلحات الأثرية والتاريخ الإسلامي والعمارة وتجيب بدقة عن الأسئلة التخصصية.
- **التراث الرقمي والمتاحف الافتراضية (Digital Heritage & Museology):** تنظيم البيانات الوصفية للقطع الأثرية والمواقع ودعم أنظمة البحث والاستكشاف الثقافي.
- **دراسة النقوش والخطوط التاريخية (Epigraphy & Historical Studies):** تدريب النماذج على ربط النصوص التاريخية والخطوط والعصور والقراءات الحديثة.
- **تطبيقات السياحة الثقافية (Cultural Tourism & Travel Assistants):** توليد مسارات وخطط زيارات تراثية منظمة للمدن والمواقع التاريخية.

---

## الترخيص (License)

هذه البيانات متاحة للعموم بموجب ترخيص المشاع الإبداعي نَسب المُصنَّف 4.0 دولي (CC BY 4.0). يُسمح بالمشاركة والتعديل والاستخدام التجاري والبحثي بشرط الإشارة إلى المصدر الأصلي.

---

## الاستشهاد (Citation)

إذا استخدمت هذه البيانات في أبحاثك أو نماذجك، يرجى الاستشهاد بها على النحو التالي:

```bibtex
@dataset{islamic_heritage_archaeology_2026,
  author       = {Abd El Rahman Amr},
  title        = {Islamic Heritage & Archaeology Dataset},
  year         = {2026},
  publisher    = {Hugging Face / Kaggle},
  license      = {CC-BY-4.0}
}
```

---

## تحميل البيانات وقراءتها عبر Python

> **ملاحظة:** الحجم الإجمالي يتجاوز **1.6 GB**؛ يُنصح بتحميل الملفات التي تحتاجها فقط، أو استخدام وضع البث (`streaming=True`) عند العمل عبر `datasets`.

### 1. التحميل من Hugging Face

تنزيل المجموعة كاملة إلى مجلد محلي عبر `huggingface_hub`:

```python
from pathlib import Path
from huggingface_hub import snapshot_download

local_dir = snapshot_download(
    repo_id="Abdulrhman472001/islamic-heritage-archaeology-dataset",
    repo_type="dataset",
    local_dir="./data_hf",
)
print("تم التنزيل إلى:", Path(local_dir).resolve())
```

أو تنزيل ملفات محددة فقط:

```python
from huggingface_hub import snapshot_download

snapshot_download(
    repo_id="Abdulrhman472001/islamic-heritage-archaeology-dataset",
    repo_type="dataset",
    local_dir="./data_hf",
    allow_patterns=["*islamic_heritage_qa.jsonl", "*islamic_heritage_epigraphy.jsonl"],
)
```

أو التحميل المباشر عبر مكتبة `datasets` (لكل ملف حقول مختلفة، لذا يُحمَّل كل ملف على حدة):

```python
from datasets import load_dataset

REPO = "Abdulrhman472001/islamic-heritage-archaeology-dataset"

qa        = load_dataset(REPO, data_files="**/islamic_heritage_qa.jsonl", split="train")
epigraphy = load_dataset(REPO, data_files="**/islamic_heritage_epigraphy.jsonl", split="train")

print(qa)
print(qa[0])

# وضع البث للملفات الكبيرة دون تنزيلها كاملة
artifacts = load_dataset(
    REPO,
    data_files="**/islamic_heritage_artifacts.jsonl",
    split="train",
    streaming=True,
)
print(next(iter(artifacts)))
```

### 2. التحميل من Kaggle

عبر مكتبة `kagglehub`:

```python
import kagglehub

dataset_path = kagglehub.dataset_download(
    "abdulrhmanamr47/islamic-heritage-archaeology-dataset"
)
print("مسار البيانات على الجهاز:", dataset_path)
```

أو عبر سطر الأوامر (Kaggle CLI):

```bash
kaggle datasets download -d abdulrhmanamr47/islamic-heritage-archaeology-dataset -p ./data_kaggle --unzip
```

### 3. قراءة ومعاينة أي ملف `.jsonl` محلياً

```python
import json
from pathlib import Path

# يبحث عن الملف داخل المجلد مهما كان مساره الفرعي
file_path = next(Path("./data_hf").rglob("islamic_heritage_qa.jsonl"))

records = []
with file_path.open("r", encoding="utf-8") as f:
    for i, line in enumerate(f):
        if line.strip():
            records.append(json.loads(line))
        if i >= 999:  # اقرأ أول 1000 سجل فقط للمعاينة السريعة
            break

print("عدد السجلات المقروءة:", len(records))
print("أول سجل:", records[0])
```

### 4. القراءة عبر pandas وتوزيع العصور

```python
import pandas as pd
from pathlib import Path

path = next(Path("./data_hf").rglob("islamic_heritage_artifacts.jsonl"))

# قراءة أول 10,000 سجل على دفعات لتوفير الذاكرة
chunks = pd.read_json(path, lines=True, chunksize=10_000)
df = next(chunks)

print(df[["artifact_name", "era", "material", "condition"]].head())
print(df["era"].value_counts())
print(df["material"].value_counts().head(10))
```

### 5. تصفية السجلات حسب العصر دون تحميل الملف كاملاً

```python
import json
from pathlib import Path

path = next(Path("./data_hf").rglob("islamic_heritage_sites.jsonl"))
out = Path("sites_mamluk.jsonl")

count = 0
with path.open("r", encoding="utf-8") as src, out.open("w", encoding="utf-8") as dst:
    for line in src:
        r = json.loads(line)
        if r.get("era") == "العصر المملوكي":
            dst.write(json.dumps(r, ensure_ascii=False) + "\n")
            count += 1

print(f"تم حفظ {count:,} سجل في {out.resolve()}")
```

### 6. تحويل الأسئلة والأجوبة إلى صيغة محادثة (SFT)

```python
import json
from pathlib import Path

path = next(Path("./data_hf").rglob("islamic_heritage_qa.jsonl"))
out = Path("sft_heritage_qa.jsonl")

with path.open("r", encoding="utf-8") as src, out.open("w", encoding="utf-8") as dst:
    for i, line in enumerate(src):
        if i >= 1000:  # عيّنة تجريبية
            break
        r = json.loads(line)
        sample = {
            "messages": [
                {"role": "user", "content": r["question"]},
                {"role": "assistant", "content": r["answer"]},
            ]
        }
        dst.write(json.dumps(sample, ensure_ascii=False) + "\n")

print("تم الحفظ في:", out.resolve())
```
