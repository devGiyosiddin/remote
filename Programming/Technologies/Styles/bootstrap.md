## 📐 Таблица брейкпоинтов Bootstrap 5

#breakpoints #bootstrap

| Брейкпоинт  | Префикс                           | Размер экрана от |
| ----------- | --------------------------------- | ---------------- |
| Extra small | `xs` (по умолчанию, без префикса) | 0px              |
| Small       | `sm:`                             | ≥ 576px          |
| Medium      | `md:`                             | ≥ 768px          |
| Large       | `lg:`                             | ≥ 992px          |
| Extra large | `xl:`                             | ≥ 1200px         |
| XXL         | `xxl:`                            | ≥ 1400px         |
### 🧠 Важное различие:

**Tailwind** — работает **mobile-first**, т.е.:

- `block` → по умолчанию (`min-width: 0`)
    
- `md:hidden` → при `min-width: 768px` → `display: none`
    

**Bootstrap** — работает **desktop-first (грубо говоря)**, и **классы вроде `d-none`, `d-md-block`** **не отменяют предыдущее значение**, если ты явно его не указал.