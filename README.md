<div align="center">

<br/>

<img alt="arabic-ui-kit" src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=42&duration=2400&pause=900&color=A78BFA&center=true&vCenter=true&width=900&height=80&lines=arabic-ui-kit"/>

**The first UI library designed FOR Arabic. Not translated.**
_RTL-first · Beautiful Arabic typography · Accessible · Tailwind + React + Flutter._

<br/>

```bash
npm i @kasimmj/arabic-ui-kit
# or
flutter pub add arabic_ui_kit
```

### 🖥️ Browse the live component playground

[<img src="https://img.shields.io/badge/Open%20Playground-A78BFA?style=for-the-badge&logoColor=white" height="40"/>](https://arabic-ui-kit.kasimmj.com)

<br/>

<p>
<img src="https://img.shields.io/badge/RTL-006C35?style=for-the-badge"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white"/>
<img src="https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white"/>
<img src="https://img.shields.io/badge/MIT-000000?style=for-the-badge"/>
</p>

<p>
<img src="https://img.shields.io/github/stars/kasimmj/arabic-ui-kit?style=social"/>
<img src="https://img.shields.io/github/forks/kasimmj/arabic-ui-kit?style=social"/>
</p>

</div>

---

## 🌍 ليش هذي المكتبة موجودة؟

Material UI, Tailwind UI, shadcn/ui — كلهن ممتازين، **لكنهن مكتوبين للإنجليزية**. لما تستخدمهن بالعربي:

- 📏 الـ spacing مكسور (padding-left بدل padding-inline-start)
- 🔤 الـ fonts مو متوازنة (تستخدم Inter للأرقام والعربي يبان قبيح)
- 📐 الـ icons في الجهة الخطأ
- 🔠 الأرقام تطلع بالشكل الإنجليزي حتى لو السياق عربي
- 📅 الـ date pickers تستخدم الميلادي ما يدعمن الهجري
- ❌ بدون دعم لـ proper hyphenation للنصوص العربية

`arabic-ui-kit` مصمم **من الأساس** للعربية. لا تعديلات بعد التطوير. لا CSS override. لا تكهنات.

---

## ✨ 80+ Components, all RTL-first

### الأساسية:
**Button** · **Input** · **Textarea** · **Checkbox** · **Radio** · **Switch** · **Select** · **Combobox** · **Slider**

### النماذج:
**Form** · **FormField** · **DatePicker (Hijri + Gregorian)** · **TimePicker** · **NumberInput (Arabic numerals support)** · **PhoneInput (+964 default)** · **FileUpload**

### التخطيط:
**Container** · **Stack** · **Grid** · **Sidebar** · **NavBar** · **TabBar** · **Footer** · **Drawer** · **Modal** · **Sheet**

### التنقل:
**Tabs** · **Pagination** · **Breadcrumb** · **Stepper** · **CommandPalette (with Arabic shortcuts)**

### العرض:
**Card** · **Avatar** · **Badge** · **Tag** · **Tooltip** · **Popover** · **Toast** · **Alert** · **Banner** · **Skeleton**

### العربية-فقط:
**HijriCalendar** · **PrayerTimesWidget** · **QuranReader (with Tajweed)** · **ArabicNumberFormatter** · **AdhanCountdown** · **DiacriticsToggle**

### المتقدمة:
**DataTable (RTL columns)** · **Charts (Recharts with RTL)** · **RichTextEditor (Arabic-aware)** · **CodeEditor (Monaco RTL)** · **Map (with Arabic cities)**

---

## 🎨 Visual Playground

The live playground (`arabic-ui-kit.kasimmj.com`) lets you:

```
╭─────────────────────────────────────────────────────────────────╮
│  🌐 arabic-ui-kit Playground                          [العربية ▾]│
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   Components                Preview                              │
│   ────────────              ────────────────────────────────    │
│   ▸ Buttons                 ┌─────────────────────────────┐    │
│   ▾ Forms                   │                              │    │
│     • Input                 │     ╭──────────╮             │    │
│     • DatePicker  ← active  │     │  حفظ  ➜  │            │    │
│     • PhoneInput            │     ╰──────────╯             │    │
│     • Select                │                              │    │
│   ▸ Layout                  │     [التاريخ      📅 ▾]     │    │
│   ▸ Navigation              │                              │    │
│   ▸ Display                 │     ┌──────────┐             │    │
│   ▸ Arabic-only             │     │ هجري ●   │             │    │
│                             │     │ ميلادي ○  │             │    │
│   Theme: ⚫ Dark  ○ Light    │     └──────────┘             │    │
│   Locale: 🇮🇶 Iraq           │                              │    │
│   Font: Cairo  ▾            └──────────────────────────────┘    │
│                                                                 │
│   📋 Copy code:                                                  │
│   ┌───────────────────────────────────────────────────────┐    │
│   │ <DatePicker calendar="hijri" defaultValue={...} />    │    │
│   └───────────────────────────────────────────────────────┘    │
│                                                                 │
╰─────────────────────────────────────────────────────────────────╯
```

Features:
- 🎨 **Live editing** — change props, see results instantly
- 🌗 **Theme switcher** — dark/light side-by-side
- 🌍 **Locale switcher** — see RTL/LTR + different Arabic dialects
- 🔤 **Font switcher** — Cairo, Tajawal, IBM Plex Arabic, Almarai
- 📋 **Copy-paste code** for each variation
- 📱 **Mobile preview** — responsive testing

---

## ⚡ Quick example

```tsx
import { Button, DatePicker, PhoneInput, ArabicNumberFormatter } from "@kasimmj/arabic-ui-kit";

function ContactForm() {
  return (
    <Stack dir="rtl" gap={4}>
      <PhoneInput
        defaultCountry="IQ"           // +964
        placeholder="رقم هاتفك"
      />

      <DatePicker
        calendar="hijri"               // or "gregorian"
        locale="ar"
        placeholder="اختر تاريخ المراجعة"
      />

      <Button variant="primary" size="lg">
        إرسال الطلب
      </Button>

      <ArabicNumberFormatter
        value={1234567.89}
        useArabicNumerals
      />
      {/* Renders: ١٬٢٣٤٬٥٦٧٫٨٩ */}
    </Stack>
  );
}
```

---

## 🎨 Theming

Every color, font, spacing, and radius is a token. Change one variable → entire app updates.

```ts
import { ThemeProvider } from "@kasimmj/arabic-ui-kit";

<ThemeProvider
  theme={{
    colors: {
      primary: "#8A2BE2",
      surface: "#0D1117",
    },
    fonts: {
      arabic: "Cairo, sans-serif",
      latin: "Inter, sans-serif",
    },
    radius: "md",          // sm | md | lg | full
    direction: "rtl",      // rtl | ltr | auto
    locale: "ar-IQ",
  }}
>
  <App />
</ThemeProvider>
```

Pre-built themes:
- 🌚 **Midnight** — dark + violet (default)
- 🌅 **Desert** — warm + bronze
- 🕌 **Classic** — traditional Islamic aesthetic
- 💼 **Corporate** — clean + minimal
- 🎨 **Vibrant** — bold + colorful

---

## ♿ Accessibility

- ✅ WCAG 2.1 AA compliant
- ✅ Full keyboard navigation (with Arabic shortcut layouts)
- ✅ Screen reader tested (NVDA + JAWS + VoiceOver)
- ✅ Color contrast 4.5:1 minimum on text
- ✅ Reduced motion respected
- ✅ Focus rings visible on all interactive elements

---

## 📱 Platforms

| Platform | Status | Package |
|----------|--------|---------|
| React (Next.js, Vite, CRA) | ✅ Stable | `@kasimmj/arabic-ui-kit` |
| Flutter | ✅ Stable | `arabic_ui_kit` |
| Vue 3 | 🚧 Beta | `@kasimmj/arabic-ui-kit-vue` |
| Svelte | 🚧 Beta | `@kasimmj/arabic-ui-kit-svelte` |
| Web Components | 📋 Planned | — |

---

## 🇮🇶 Iraqi-specific features

- 🏙️ **City picker** — All Iraqi cities + districts pre-populated
- 📞 **Phone validation** — Iraqi mobile prefixes (07X) + landlines
- 📅 **Hijri calendar** — Islamic date support with proper conversions
- 🕌 **Prayer times widget** — based on lat/long, multiple calculation methods
- 📜 **Diacritics toggle** — Show/hide tashkeel on Quranic text
- 💰 **IQD formatter** — proper Iraqi Dinar formatting (1,234,567 IQD)

---

## 🚀 Roadmap

- [x] 80+ React components
- [x] 80+ Flutter components (parity)
- [x] Visual playground
- [x] 5 themes
- [ ] Figma library + variables
- [ ] Sketch library
- [ ] Vue 3 + Svelte parity
- [ ] Voice navigation (Arabic STT)
- [ ] Animation system (Framer Motion preset)

---

## 📜 License

MIT.

---

<div align="center">

**Star ⭐ to support Arabic developer experience.**

</div>
