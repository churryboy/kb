# KB Star Banking — Brand Identity & Digital Language

> **Official Documentation v1.0.2**

A comprehensive guide to KB Star Banking's visual language, interaction principles, and UI components library.

---

## 1. Color Palette

| Swatch | Name | Hex | Role |
|--------|------|-----|------|
| 🟡 | **KB Yellow** | `#FFCC00` | Primary Brand Color |
| ⬛ | **Charcoal** | `#2D2D2D` | Secondary / Text Primary |
| 🩶 | **Slate Gray** | `#64748B` | Neutral UI Elements |
| ⬜ | **Soft Gray** | `#F1F5F9` | Backgrounds & Dividers |

### Tailwind Config Colors

```js
colors: {
  "primary": "#ffcc00",
  "charcoal": "#2d2d2d",
  "background-light": "#f8f8f5",
  "background-dark": "#231f0f",
}
```

---

## 2. Typography

**Font Family:** Manrope (Google Fonts)

```js
fontFamily: {
  "display": ["Manrope", "sans-serif"]
}
```

| Level | Weight | Size | Example |
|-------|--------|------|---------|
| **Heading 1** | ExtraBold (800) | 48px / `text-5xl` | The quick brown fox jumps |
| **Heading 2** | Bold (700) | 30px / `text-3xl` | The quick brown fox jumps over the lazy dog |
| **Body Large** | Regular (400) | 18px / `text-lg` | KB Star Banking provides a seamless and secure financial experience. |
| **Body Base** | Regular (400) | 16px / `text-base` | A comprehensive banking application that allows users to manage their accounts. |

---

## 3. Border Radius

```js
borderRadius: {
  DEFAULT: "0.5rem",
  lg: "1rem",
  xl: "1.5rem",
  full: "9999px",
}
```

---

## 4. UI Components

### 4-1. Button Actions

#### Primary Button

```html
<button class="bg-primary text-charcoal px-8 py-3 rounded-xl font-bold hover:brightness-105 active:scale-95 transition-all">
  Primary Action
</button>
```

- 배경: `bg-primary` (`#FFCC00`)
- 텍스트: `text-charcoal` (`#2D2D2D`)
- Radius: `rounded-xl` (1.5rem)
- Hover: `brightness-105`
- Active: `scale-95`

#### Secondary Button

```html
<button class="bg-charcoal text-white px-8 py-3 rounded-xl font-bold hover:bg-slate-700 active:scale-95 transition-all">
  Secondary Action
</button>
```

- 배경: `bg-charcoal` (`#2D2D2D`)
- 텍스트: `text-white`
- Hover: `bg-slate-700`

#### Ghost Button

```html
<button class="border-2 border-primary text-slate-900 dark:text-white px-8 py-3 rounded-xl font-bold hover:bg-primary/10 transition-all">
  Ghost Action
</button>
```

- Border: `border-2 border-primary`
- Hover: `bg-primary/10`

#### Disabled Button

```html
<button class="bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-400 px-8 py-3 rounded-xl font-bold cursor-not-allowed opacity-50">
  Disabled
</button>
```

- `cursor-not-allowed`, `opacity-50`

#### Icon Buttons (FAB)

```html
<!-- Primary FAB -->
<button class="size-12 rounded-full bg-primary flex items-center justify-center text-charcoal shadow-md">
  <span class="material-symbols-outlined">add</span>
</button>

<!-- Outlined FAB -->
<button class="size-12 rounded-full border-2 border-slate-200 dark:border-slate-700 flex items-center justify-center text-slate-600 dark:text-slate-400">
  <span class="material-symbols-outlined">favorite</span>
</button>
```

---

### 4-2. Cards & Containers

#### Info Card (Light)

```html
<div class="bg-white dark:bg-slate-900 p-6 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm hover:shadow-md transition-shadow">
  <div class="flex items-start justify-between mb-4">
    <div class="size-12 rounded-xl bg-primary/20 flex items-center justify-center text-primary">
      <span class="material-symbols-outlined text-2xl">account_balance_wallet</span>
    </div>
    <span class="text-xs font-bold text-emerald-500 bg-emerald-500/10 px-2 py-1 rounded">ACTIVE</span>
  </div>
  <h4 class="font-bold text-lg text-slate-900 dark:text-white mb-1">Savings Account</h4>
  <p class="text-sm text-slate-500 mb-4">KB Star Premium Savings account for daily needs.</p>
  <div class="flex items-center justify-between pt-4 border-t border-slate-100 dark:border-slate-800">
    <span class="text-2xl font-black text-slate-900 dark:text-white">$12,450.00</span>
    <span class="material-symbols-outlined text-slate-400 cursor-pointer">arrow_forward_ios</span>
  </div>
</div>
```

**구성 요소:**

- Icon badge: `size-12 rounded-xl bg-primary/20`
- Status badge: `text-emerald-500 bg-emerald-500/10`
- Shadow: `shadow-sm` → hover 시 `shadow-md`
- Border: `border border-slate-200`
- Radius: `rounded-2xl`

#### Action Card (Dark)

```html
<div class="bg-charcoal p-6 rounded-2xl shadow-xl relative overflow-hidden group">
  <div class="absolute top-0 right-0 w-32 h-32 bg-primary opacity-10 rounded-full -mr-16 -mt-16 transition-transform group-hover:scale-110"></div>
  <h4 class="text-white font-bold text-lg mb-2">Instant Transfer</h4>
  <p class="text-slate-400 text-sm mb-4">Send money to any KB Star user instantly without fees.</p>
  <button class="text-primary font-bold text-sm flex items-center gap-2 group-hover:gap-3 transition-all">
    Get Started <span class="material-symbols-outlined text-sm">trending_flat</span>
  </button>
</div>
```

**구성 요소:**

- 배경: `bg-charcoal`
- Decorative circle: `bg-primary opacity-10`, hover 시 `scale-110`
- CTA link: `text-primary`, hover 시 `gap-3`으로 arrow 이동 효과

---

## 5. Logo Usage

### Light Surface

- 배경: `bg-white` 또는 `bg-background-light` (`#F8F8F5`)
- 로고 높이: `h-24`
- Shadow: `drop-shadow-sm`

### Dark Surface

- 배경: `bg-charcoal` (`#2D2D2D`)
- 로고 높이: `h-24`
- 필터: `brightness-110`

### Footer (Small)

- 높이: `h-6`
- 필터: `grayscale brightness-150`

---

## 6. Navigation (Header)

```html
<header class="flex items-center justify-between whitespace-nowrap border-b border-solid border-slate-200 dark:border-slate-800 px-6 lg:px-20 py-4 bg-white dark:bg-slate-900 sticky top-0 z-50">
  ...
</header>
```

**특성:**

- `sticky top-0 z-50`
- 하단 border: `border-b border-slate-200`
- 패딩: `px-6 lg:px-20 py-4`
- 활성 nav 링크: `text-primary font-bold border-b-2 border-primary pb-1`
- 비활성 nav 링크: `text-slate-600 font-semibold hover:text-primary`

### Search Input

```html
<div class="flex w-full flex-1 items-stretch rounded-lg h-full bg-slate-100 dark:bg-slate-800 border border-slate-200 dark:border-slate-700">
  <div class="text-slate-400 flex items-center justify-center pl-3">
    <span class="material-symbols-outlined text-xl">search</span>
  </div>
  <input class="w-full bg-transparent border-none focus:ring-0 text-sm px-3 text-slate-900 dark:text-white placeholder:text-slate-500" placeholder="Search system..." />
</div>
```

---

## 7. Footer

```html
<footer class="bg-slate-900 text-slate-400 py-12 px-6 lg:px-20 border-t border-slate-800">
  ...
</footer>
```

- 배경: `bg-slate-900`
- 텍스트: `text-slate-400`
- 링크 hover: `hover:text-primary`

---

## 8. Dark Mode Support

Tailwind `darkMode: "class"` 전략 사용.

```js
tailwind.config = {
  darkMode: "class",
  ...
}
```

- `<html class="light">` → 라이트 모드
- `<html class="dark">` → 다크 모드
- 모든 컴포넌트에 `dark:` variant 적용 필수

| Token | Light | Dark |
|-------|-------|------|
| Page BG | `bg-background-light` (`#F8F8F5`) | `bg-background-dark` (`#231F0F`) |
| Surface | `bg-white` | `bg-slate-900` |
| Border | `border-slate-200` | `border-slate-800` |
| Text Primary | `text-slate-900` | `text-white` |
| Text Secondary | `text-slate-600` | `text-slate-400` |

---

## 9. Icon System

**Google Material Symbols Outlined**

```html
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&display=swap" rel="stylesheet" />
```

사용 예시:

```html
<span class="material-symbols-outlined">account_balance_wallet</span>
<span class="material-symbols-outlined">search</span>
<span class="material-symbols-outlined">notifications</span>
<span class="material-symbols-outlined">add</span>
<span class="material-symbols-outlined">favorite</span>
<span class="material-symbols-outlined">arrow_forward_ios</span>
<span class="material-symbols-outlined">trending_flat</span>
<span class="material-symbols-outlined">download</span>
<span class="material-symbols-outlined">verified</span>
```

---

## 10. Layout

- 최대 너비: `max-w-[1200px] mx-auto`
- 콘텐츠 패딩: `px-6 lg:px-10 py-10`
- 섹션 간격: `mb-20`
- 그리드: `grid-cols-1 sm:grid-cols-2 lg:grid-cols-4` (컬러), `grid-cols-1 md:grid-cols-2` (컴포넌트)

---

## 11. Iconography System

### 11-1. Design Principles

KB Star Banking의 아이콘 시스템은 친근함, 접근성, 브랜드 일관성을 강조하는 시각적 심볼 컬렉션입니다.

#### Core Principles

| Principle | Description |
|-----------|-------------|
| **Soft Line Art** | 얇고 우아한 라인 스타일로 무거운 채움을 피해 숨쉬는 듯한 모던 인터페이스 구현 |
| **Rounded Terminals** | 모든 경로와 스트로크가 둥근 끝으로 마무리되어 KB Star Banking의 친근하고 접근하기 쉬운 특성 반영 |
| **Consistent 2px Stroke** | 표준 2px 스트로크 두께로 다양한 화면 해상도와 크기에서 시각적 균형과 가독성 보장 |

### 11-2. Navigation Icons (Bottom Navigation Style)

```html
<!-- Bottom Navigation Container -->
<div class="flex gap-8 md:gap-16 items-end">
  <!-- Inactive Tab -->
  <div class="flex flex-col items-center gap-3">
    <span class="material-symbols-outlined text-3xl text-slate-400">shopping_bag</span>
    <span class="text-sm font-medium text-slate-500">상품</span>
  </div>
  
  <!-- Active Tab (Center FAB Style) -->
  <div class="flex flex-col items-center gap-3">
    <div class="size-16 rounded-full bg-primary flex items-center justify-center shadow-lg shadow-primary/20 transform -translate-y-4">
      <span class="material-symbols-outlined text-4xl text-charcoal">account_balance_wallet</span>
    </div>
    <span class="text-sm font-bold text-slate-900 dark:text-slate-100">지갑</span>
  </div>
  
  <!-- Other Tabs -->
  <div class="flex flex-col items-center gap-3">
    <span class="material-symbols-outlined text-3xl text-slate-400">featured_seasonal_and_gifts</span>
    <span class="text-sm font-medium text-slate-500">혜택</span>
  </div>
</div>
```

**네비게이션 아이콘 특징:**

- **비활성 상태**: `text-slate-400` 아이콘 + `text-slate-500` 라벨
- **활성 상태**: `bg-primary` 원형 배경 + `text-charcoal` 아이콘 + 상향 이동 효과
- **FAB 스타일**: 중앙 활성 탭은 `size-16` 원형 버튼으로 강조
- **그림자**: `shadow-lg shadow-primary/20`으로 부드러운 입체감

### 11-3. Functional Icons

일반적인 기능 아이콘들의 그리드 시스템:

```html
<div class="grid grid-cols-4 gap-4">
  <div class="aspect-square bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-800 rounded-xl flex flex-col items-center justify-center gap-2">
    <span class="material-symbols-outlined text-2xl">notifications</span>
    <span class="text-[10px] text-slate-400">Notification</span>
  </div>
  <div class="aspect-square bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-800 rounded-xl flex flex-col items-center justify-center gap-2">
    <span class="material-symbols-outlined text-2xl">search</span>
    <span class="text-[10px] text-slate-400">Search</span>
  </div>
  <!-- More icons... -->
</div>
```

### 11-4. Icon Sizing & Grid System

| Size | Usage | CSS Class | Pixel Size |
|------|-------|-----------|------------|
| **Standard Action** | 일반 버튼, 인라인 아이콘 | `text-2xl` | 24 x 24px |
| **Display Icon** | 카드 헤더, 주요 액션 | `text-4xl` | 32 x 32px |
| **Navigation** | 하단 네비게이션 | `text-3xl` | 28 x 28px |
| **FAB Center** | 중앙 플로팅 버튼 | `text-4xl` | 32 x 32px |

#### Grid Guidelines

```css
/* 24x24 Grid */
.icon-grid-24 {
  background-image: linear-gradient(#000 1px, transparent 1px), 
                    linear-gradient(90deg, #000 1px, transparent 1px);
  background-size: 8px 8px;
}

/* 32x32 Grid */
.icon-grid-32 {
  background-image: linear-gradient(#000 1px, transparent 1px), 
                    linear-gradient(90deg, #000 1px, transparent 1px);
  background-size: 12px 12px;
}
```

### 11-5. Color Usage in Icons

#### Charcoal (#2D2D2D)
기본 상호작용 상태, 라벨, 보조 액션에 사용하여 밝은 배경에서 높은 가독성 보장.

```html
<!-- Charcoal Icons -->
<span class="material-symbols-outlined text-charcoal text-4xl">savings</span>
<span class="material-symbols-outlined text-charcoal text-4xl">credit_card</span>
<span class="material-symbols-outlined text-charcoal text-4xl">swap_horiz</span>
```

#### KB Yellow (#FFCC00)
브랜드 강조, 네비게이션 활성 상태, 핵심 뱅킹 가치를 나타내는 주요 CTA 심볼에 사용.

```html
<!-- Primary Brand Icons -->
<span class="material-symbols-outlined text-primary text-4xl">stars</span>
<span class="material-symbols-outlined text-primary text-4xl">qr_code_2</span>
<span class="material-symbols-outlined text-primary text-4xl">emoji_events</span>
```

#### Slate Gray (Inactive States)
비활성 상태, 보조 정보, 플레이스홀더에 사용.

```html
<!-- Inactive/Secondary Icons -->
<span class="material-symbols-outlined text-slate-400 text-3xl">shopping_bag</span>
<span class="material-symbols-outlined text-slate-500 text-2xl">settings</span>
```

### 11-6. Material Symbols Configuration

```css
.material-symbols-outlined {
  font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
}

/* 더 굵은 스트로크가 필요한 경우 */
.icon-stroke-2 {
  font-variation-settings: 'wght' 400;
}
```

### 11-7. Common Icon Mappings

| Function | Icon | Usage Context |
|----------|------|---------------|
| `account_balance_wallet` | 지갑/계좌 | 메인 네비게이션, 계좌 관련 |
| `shopping_bag` | 상품 | 상품 카테고리, 쇼핑 |
| `query_stats` | 자산 | 자산 관리, 통계 |
| `featured_seasonal_and_gifts` | 혜택 | 프로모션, 리워드 |
| `description` | 테마/내역 | 문서, 거래내역 |
| `notifications` | 알림 | 푸시, 메시지 |
| `search` | 검색 | 검색 기능 |
| `settings` | 설정 | 환경설정 |
| `menu` | 메뉴 | 햄버거 메뉴 |

---

*© 2024 KB Star Banking. All rights reserved.*
