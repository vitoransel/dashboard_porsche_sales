# Porsche Sales Sanitization Schema

## 1. Canonical input columns

| Column | Required | Description | Example raw values |
|---|---|---|---|
| `customer_name` | yes | Customer's full name | `John Smith`, `SOPHIA Miller`, `Daniel-Jones` |
| `salesperson` | yes | Salesperson's full name | `Kevin`, `AMANDA Scott`, `PETER Ford` |

## 2. Sanitized output columns

| Source | Output | Format |
|---|---|---|
| `customer_name` | `CustomerNameSanitized` | Title Case full name |
| `salesperson` | `SalespersonSanitized` | Title Case full name |

## 3. Sanitization rules

### Customer name

Normalize customer names to Title Case.

Apply the following rules:

- Capitalize the first letter of each name.
- Convert unnecessary uppercase letters to lowercase.
- Replace hyphens with spaces in compound names.
- Preserve apostrophes and other valid name characters.
- Do not change the spelling or invent missing information.

**Examples:**

| Original | Sanitized |
|---|---|
| `SOPHIA Miller` | `Sophia Miller` |
| `MARY Johnson` | `Mary Johnson` |
| `Daniel-Jones` | `Daniel Jones` |
| `Michael Adams` | `Michael Adams` |
| `OLIVIA BROWN` | `Olivia Brown` |
| `ava martinez` | `Ava Martinez` |

### Salesperson

Normalize salesperson names using the same formatting rules applied to customer names.

Apply the following rules:

- Capitalize the first letter of each name.
- Convert unnecessary uppercase letters to lowercase.
- Replace hyphens with spaces in compound names.
- Preserve apostrophes and other valid name characters.
- Do not change the spelling or invent missing information.

**Examples:**

| Original | Sanitized |
|---|---|
| `kevin` | `Kevin` |
| `AMANDA Scott` | `Amanda Scott` |
| `jessica` | `Jessica` |
| `LISA ray` | `Lisa Ray` |
| `samuel price` | `Samuel Price` |
| `PETER Ford` | `Peter Ford` |
| `ERIC woods` | `Eric Woods` |
| `natalie` | `Natalie` |

## 4. Quality checks

After normalization, verify:

- No original columns were removed or overwritten.
- Sanitized columns appear immediately after their respective source columns.
- All customer names follow a consistent Title Case format.
- All salesperson names follow a consistent Title Case format.
- Hyphens have been replaced with spaces.
- Original names remain available for comparison.

## 5. Invalid handling

Use `INVALID` in the corresponding sanitized column when a name is missing, empty, or cannot be normalized safely.

- Never invent customer or salesperson names.
- Keep the original names available for comparison.
- Do not overwrite the source columns during sanitization.
- Preserve the original data structure whenever possible.
