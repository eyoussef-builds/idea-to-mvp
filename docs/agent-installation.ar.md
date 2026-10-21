# التثبيت خطوة بخطوة على 15 مساعدًا

[English](agent-installation.md) · [الشرح الرئيسي](../README.ar.md)

اعتبر المهارة كتيّبًا صغيرًا يحتاج المساعد وضعه على رف يعرف مكانه. سننزّل الكتيّب، ونضعه على الرف المناسب، ثم نطلب من المساعد قراءته. لا تحتاج تعديل الكود.

## 1. نزّل المجلد مرة واحدة

1. افتح [صفحة المستودع](https://github.com/eyoussef-builds/idea-to-mvp).
2. اضغط الزر الأخضر **Code** ثم **Download ZIP**.
3. فك الضغط. افتح المجلد الناتج الذي يحتوي `README.md` ومجلد `skills`.
4. تأكد من وجود `skills/idea-to-mvp/SKILL.md`. انقل مجلد `idea-to-mvp` كاملًا بمراجعه وقوالبه وبرامجه، وليس ملف `SKILL.md` وحده.
5. اختر مساعدك من الأقسام التالية. ثبّت نسخة واحدة في مكان واحد؛ لا تحتاج كل المجلدات.

أو، إذا كان Git مثبتًا، افتح Terminal أو PowerShell داخل مجلد تنزيل مناسب ونفّذ:

```sh
git clone https://github.com/eyoussef-builds/idea-to-mvp.git
cd idea-to-mvp
```

المهارة هنا مجلد محلي وليست إضافة متجر مسجّلة. لا تحتاج تثبيت كل المساعدين؛ يكفي مساعد واحد مثبت ومسجّل الدخول.

## 2. كيف تنسخها؟

**دون أوامر:** لكل مساعد مكان مكتوب أدناه. `~` تعني مجلد حسابك الشخصي، وليست اسم شخص محدد. على macOS استخدم Finder ثم **Go → Go to Folder**. على Linux استخدم مدير الملفات وأظهر المجلدات المخفية عند الحاجة. على Windows افتح مجلد المستخدم ثم أنشئ المجلدات المكتوبة في مسار PowerShell. إذا لم يوجد المجلد المطلوب، أنشئ مجلداته داخل حسابك أولًا. انسخ مجلد المهارة كاملًا إليه. إذا وجدت نسخة قديمة، توقّف وقارنها قبل الاستبدال.

**باستخدام الأوامر:** افتح الطرفية داخل مجلد المستودع بعد فك الضغط. في قسم مساعدك ستجد سطرين: أحدهما لـmacOS/Linux والآخر لـPowerShell. اختر نظامك فقط، ثم شغّل كتلة النسخ المناسبة التالية في **نفس نافذة الطرفية**.

macOS / Linux، بعد ضبط `dest_parent` من قسم مساعدك:

```sh
if [ -e "$dest_parent/idea-to-mvp" ] || [ -L "$dest_parent/idea-to-mvp" ]; then
  echo "Already installed. Compare your existing copy before updating."
else
  mkdir -p "$dest_parent" && cp -R "skills/idea-to-mvp" "$dest_parent/"
fi
```

Windows PowerShell، بعد ضبط `$destParent` من قسم مساعدك:

```powershell
$skillDest = Join-Path $destParent 'idea-to-mvp'
if (Test-Path -LiteralPath $skillDest) { throw 'Already installed. Compare before updating.' }
New-Item -ItemType Directory -Force -Path $destParent | Out-Null
Copy-Item -LiteralPath 'skills/idea-to-mvp' -Destination $destParent -Recurse
```

إذا ظهر تنبيه «Already installed»، لم تتحدّث النسخة القديمة. احفظ تعديلاتك وقارن المجلدين أولًا. المجلد النهائي يجب أن يحتوي `idea-to-mvp/SKILL.md` مباشرة، وليس مجلدًا إضافيًا متداخلًا بنفس الاسم.

التعليمات راجعت وثائق المساعدين الرسمية بتاريخ 2026-10-21؛ ليست ادعاءً بتجربة المهارة عمليًا على كل مساعد. قد تختلف الإصدارات وسياسات المؤسسات. إعادة فتح الجلسة أو تحميل المهارات قد تكون مطلوبة.

**حدود التوافق:** التعليمات قابلة للنقل؛ الأدوات ليست متطابقة. البحث يحتاج تصفحًا، والبناء يحتاج أوامر وملفات، والنشر يحتاج صلاحيات. ثبّت تكامل Spec Kit الرسمي المناسب لمساعدك عندما تصل إلى مرحلة البناء؛ وجود المهارة وحده لا يثبّته.

## 1. OpenAI Codex

1. اختر المجلد الشخصي: `~/.agents/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.agents/skills"
```

```powershell
$destParent = Join-Path $HOME '.agents/skills'
```

3. في Codex CLI أو إضافة المحرر، اكتب `$idea-to-mvp` أو اخترها من `/skills`. في قائمة المهارات بتطبيق سطح المكتب اختر المهارة المثبّتة. البديل الخاص بمشروع: `.agents/skills/idea-to-mvp/`.

[الوثائق الرسمية](https://developers.openai.com/codex/skills/).

## 2. Claude Code

1. اختر المجلد الشخصي: `~/.claude/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.claude/skills"
```

```powershell
$destParent = Join-Path $HOME '.claude/skills'
```

3. اكتب `/idea-to-mvp` ثم طلبك. البديل الخاص بمشروع: `.claude/skills/idea-to-mvp/`. التثبيت المحلي لا يثبّتها تلقائيًا في Cowork أو الجلسات السحابية.

[الوثائق الرسمية](https://code.claude.com/docs/en/skills).

## 3. OpenClaw

1. من مجلد المستودع، نفّذ:

```sh
openclaw skills install ./skills/idea-to-mvp --as idea-to-mvp
openclaw skills list
openclaw skills check
```

2. راجع أي تنبيه ثقة دون تجاوزه تلقائيًا. تأكد أن التثبيت يستهدف مساحة عمل المساعد المطلوبة؛ اختر المساعد المهيأ عبر خيارات CLI الرسمية إذا كان لديك أكثر من واحد.
3. اطلب استخدام `idea-to-mvp` وتأكد من ظهورها. الـGateway البعيد يحتاج الملفات والأدوات في بيئته هو.

[الوثائق الرسمية](https://docs.openclaw.ai/cli/skills).

## 4. Hermes Agent

1. من الطرفية نفّذ:

```sh
hermes skills install eyoussef-builds/idea-to-mvp/skills/idea-to-mvp
```

2. راجع فحص المهارة المجتمعية واترك فحوص الأمان مفعّلة.
3. اطلب من Hermes عرض المهارات ثم استخدام `idea-to-mvp`. المجلد اليدوي الافتراضي `~/.hermes/skills/idea-to-mvp/`؛ قد يختلف مع ملف تعريف مخصص.

[الوثائق الرسمية](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills/).

## 5. Cursor

1. اختر المجلد الشخصي: `~/.cursor/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.cursor/skills"
```

```powershell
$destParent = Join-Path $HOME '.cursor/skills'
```

3. اكتب `/` في محادثة Agent واختر `idea-to-mvp`. البديل الخاص بمشروع: `.cursor/skills/idea-to-mvp/`. وصول المهارة الشخصية إلى عامل سحابي يحتاج مزامنة أو إعدادًا مدعومًا منفصلًا.

[الوثائق الرسمية](https://cursor.com/docs/skills).

## 6. Grok Bot

1. هذه **طريقة تكييف للتعليمات**، وليست ادعاءً بدعم استيراد `SKILL.md` الأصلي. افتح Bot وأرسل رابط هذا المستودع.
2. اطلب قراءة `skills/idea-to-mvp/SKILL.md` والمراجع المطلوبة، ثم حفظ طريقة العمل كمهارة خاصة باسم `idea-to-mvp`. احتفظ بالملفات المساعدة إذا كانت بيئة المساعد تدعمها.
3. افحص المهارة المحفوظة في إدارة الإضافات والمهارات الخاصة، وفعّلها للمساعد الحالي إن لزم ثم اخترها من `/` حيث يتوفر. إذا تعذرت قراءة المجلد، استخدم طريقة القراءة الصريحة في نهاية الدليل.

[الوثائق الرسمية](https://docs.x.ai/grok-bot/skills-routines-and-automations).

## 7. OpenCode

1. اختر المجلد الشخصي: `~/.config/opencode/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.config/opencode/skills"
```

```powershell
$destParent = Join-Path $HOME '.config/opencode/skills'
```

3. اطلب تحميل `idea-to-mvp` عبر أداة المهارات. البديل الخاص بمشروع: `.opencode/skills/idea-to-mvp/`. تأكد من ظهور الاسم وإمكانية قراءة المراجع.

[الوثائق الرسمية](https://opencode.ai/docs/skills/).

## 8. GitHub Copilot

1. اختر المجلد الشخصي: `~/.copilot/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.copilot/skills"
```

```powershell
$destParent = Join-Path $HOME '.copilot/skills'
```

3. استخدم وضع Agent محليًا في محرر مدعوم أو Copilot CLI واطلب `idea-to-mvp`. البديل الخاص بمشروع: `.github/skills/idea-to-mvp/`. يتأثر الاكتشاف بالإصدار وسياسة المؤسسة، ولا يقرأ المساعد السحابي ملفات جهازك تلقائيًا.

[الوثائق الرسمية](https://docs.github.com/en/copilot/concepts/customizations/agent-skills).

## 9. Gemini CLI

1. اختر المجلد الشخصي: `~/.gemini/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.gemini/skills"
```

```powershell
$destParent = Join-Path $HOME '.gemini/skills'
```

3. نفّذ `/skills list` داخل المساعد ثم اطلب استخدام `idea-to-mvp`. استخدم `/skills reload` عند الحاجة. البديل الخاص بمشروع: `.gemini/skills/idea-to-mvp/`. احتفظ بطلبات الموافقة المعتادة لتفعيل المهارة.

[الوثائق الرسمية](https://geminicli.com/docs/cli/skills/).

## 10. Windsurf / Cascade / Devin Desktop

1. اختر المجلد الشخصي: `~/.codeium/windsurf/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.codeium/windsurf/skills"
```

```powershell
$destParent = Join-Path $HOME '.codeium/windsurf/skills'
```

3. اطلب من Cascade تحميل `idea-to-mvp` وتأكد من ظهورها. الوثائق الحالية تنتقل إلى Devin Desktop؛ مجلد المشروع المفضل `.devin/skills/` مع استمرار `.windsurf/skills/` للتوافق. اختر المجلد المدعوم في إصدارك.

[الوثائق الرسمية](https://docs.windsurf.com/windsurf/cascade/skills).

## 11. Cline

1. اختر المجلد الشخصي: `~/.cline/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.cline/skills"
```

```powershell
$destParent = Join-Path $HOME '.cline/skills'
```

3. افتح Cline وتأكد من تفعيل المهارات في إصدارك ثم اطلب استخدام `idea-to-mvp`. البديل الخاص بمشروع: `.cline/skills/idea-to-mvp/`. استخدم وضعًا يتيح أدوات المهمة المطلوبة.

[الوثائق الرسمية](https://docs.cline.bot/customization/skills).

## 12. Roo Code

1. اختر المجلد الشخصي: `~/.roo/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.roo/skills"
```

```powershell
$destParent = Join-Path $HOME '.roo/skills'
```

3. اطلب من Roo تحميل `idea-to-mvp` بأداة المهارات. البديل الخاص بمشروع: `.roo/skills/idea-to-mvp/`. استخدم المجلد العام ما لم تكن تريد قصر المهارة على وضع معين.

[الوثائق الرسمية](https://roocodeinc.github.io/Roo-Code/advanced-usage/available-tools/skill/).

## 13. Aider

1. نستخدم **سياقًا للقراءة** بدل الادعاء بوجود تثبيت مهارات أصلي. من المستودع، نفّذ:

```sh
aider --read skills/idea-to-mvp/SKILL.md
```

2. أضف المراجع ذات الصلة بأمر `/read` مع مسار الملف داخل `skills/idea-to-mvp/references/`، وأضف البرامج المساعدة عند الحاجة.
3. اطلب اتباع المهارة، وأعطه فقط البيانات المسموح بها. قراءة النص لا تضيف أدوات محادثات أو متصفحًا أو خدمة صور أو صلاحية تنفيذ غير متاحة.

[الوثائق الرسمية](https://aider.chat/docs/usage/tips.html).

## 14. Amp

1. اختر المجلد الشخصي: `~/.agents/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.agents/skills"
```

```powershell
$destParent = Join-Path $HOME '.agents/skills'
```

3. اطلب من Amp عرض المهارات وتحميل `idea-to-mvp`. البديل الخاص بمشروع: `.agents/skills/idea-to-mvp/`. تأكد أن إعداداتك لم تعطّل اكتشاف المهارات العامة.

[الوثائق الرسمية](https://ampcode.com/docs/customize/skills).

## 15. Goose

1. اختر المجلد الشخصي: `~/.agents/skills/idea-to-mvp/`.
2. نفّذ سطر نظامك ثم كتلة النسخ في الخطوة 2 أعلاه:

```sh
dest_parent="$HOME/.agents/skills"
```

```powershell
$destParent = Join-Path $HOME '.agents/skills'
```

3. أبقِ إضافة Skills مفعّلة. افحص `goose skills list` ثم استخدم `/skills idea-to-mvp` داخل المحادثة. البديل الخاص بمشروع: `.agents/skills/idea-to-mvp/`. عمل الملفات والأوامر يحتاج إضافات أدوات مناسبة.

[الوثائق الرسمية](https://github.com/aaif-goose/goose/blob/main/documentation/docs/guides/context-engineering/using-skills.md).

## 3. تأكد أنها تعمل

1. افتح جلسة جديدة أو أعد تحميل المهارات إذا لم تظهر.
2. اسأل: «هل ترى مهارة `idea-to-mvp`؟ اقرأ تعليماتها وقل لي ماذا تحتاج قبل بدء العمل».
3. تحقق أنه يقرأ مجلد المهارة الكامل لا ملفًا آخر يحمل اسمًا مشابهًا.
4. استخدم طلب البداية في [الشرح الرئيسي](../README.ar.md). إذا كانت أداة لازمة غير متاحة، يجب أن يوضح ذلك، لا أن يختلق نتيجة ناجحة.

## لأي مساعد آخر: قراءة صريحة

افتح المستودع أو نزّله في مساحة يستطيع المساعد قراءتها، ثم قل:

```text
اقرأ skills/idea-to-mvp/SKILL.md واتبع طريقة العمل لهذه المهمة.
اقرأ المراجع المرتبطة عند الحاجة وافحص البرامج قبل تشغيلها.
احترم صلاحياتي الحالية ووضّح الأدوات والبيانات غير المتاحة.
```

إذا كان المساعد نصيًا فقط، أرفق ملف التعليمات والمراجع الضرورية إن كان يدعم المرفقات. هذا يتيح شرحًا أو تخطيطًا، ولا يمنحه وصولًا إلى ملفات جهازك. لا ترفع سجلًا خاصًا كاملًا لمجرد تعويض أداة ناقصة.

## حل المشكلات

| المشكلة | ما الذي تفعله؟ |
| --- | --- |
| لا تظهر المهارة | افحص المجلد المدعوم وحالة الأحرف في `SKILL.md` وعدم وجود مجلد إضافي متداخل، ثم أعد تحميل المهارات. |
| لا تعمل تلقائيًا | اذكر اسمها صراحة أو استخدم طريقة الاستدعاء الخاصة بالمساعد. |
| النسخة المثبّتة قديمة | قارن النسخة الجديدة بالقديمة، واحفظ التعديلات والملف الشخصي المحلي قبل التحديث. |
| توجد نسختان بنفس الاسم | اختر المكان المقصود وأزل النسخة المكررة بعد حفظ أي تعديلات. |
| المساعد السحابي لا يرى ملفاتك | استخدم بيئة محلية أو مصدرًا مسموحًا به متاحًا فعلًا؛ لا تفترض مزامنة تلقائية. |
| سياسة المؤسسة تمنع المهارات | راجع سياسة المؤسسة والطريقة المدعومة مع المسؤول؛ لا تتجاوز القيود. |
| تريد حذفها | احذف مجلد `idea-to-mvp` المثبّت فقط أو استخدم أداة الإزالة الخاصة بالمساعد، واترك ملفات مشاريعك كما هي. |

---

إعداد [eyoussef-builds](https://github.com/eyoussef-builds) · [hello@eyoussef.me](mailto:hello@eyoussef.me) · [eyoussef.me](https://eyoussef.me)
