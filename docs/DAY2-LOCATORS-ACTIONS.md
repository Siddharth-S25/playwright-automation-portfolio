# Day 2: Locators, Actions & Waits

## 📍 5 Locator Types

### 1. CSS Selector
```javascript
page.locator('input[placeholder="What needs to be done?"]')
page.locator('button.submit')
page.locator('#email-input')
```
✅ Fast, reliable for known selectors

### 2. Text Selector (EASY)
```javascript
page.locator('text=Login')
page.locator('text=/exact match/i')
```
✅ Best for buttons and links with text

### 3. Role Selector (BEST)
```javascript
page.locator('role=textbox')
page.locator('role=button[name="Submit"]')
page.locator('role=checkbox')
```
✅ Most reliable, accessibility-based

### 4. Attribute Selector
```javascript
page.locator('[placeholder*="search"]')     // Contains
page.locator('[id^="btn-"]')                // Starts with
page.locator('[class$="-primary"]')         // Ends with
```
✅ Flexible pattern matching

### 5. XPath
```javascript
page.locator('xpath=//button[@type="submit"]')
page.locator('xpath=//div[@class="container"]//button')
```
⚠️ Powerful but complex

---

## 🎬 7 Actions

| Action | Code | Use Case |
|--------|------|----------|
| **Click** | `await element.click()` | Click buttons, links |
| **Fill** | `await element.fill('text')` | Type in input (fast) |
| **Type** | `await element.type('text')` | Slow, realistic typing |
| **Check** | `await element.check()` | Check checkbox |
| **Uncheck** | `await element.uncheck()` | Uncheck checkbox |
| **Hover** | `await element.hover()` | Trigger hover effects |
| **Press** | `await element.press('Enter')` | Press keyboard keys |

---

## ⏳ Smart Waits

Playwright **automatically** waits before actions:
- ✅ Element attached to DOM
- ✅ Element visible
- ✅ Element enabled
- ✅ No animations
- ✅ Element stable

**No explicit waits needed!**

---

## 🧪 Tests Created

| Test | Topic | Status |
|------|-------|--------|
| TC2.1 | CSS Selector | ✅ |
| TC2.2 | Text Selector | ✅ |
| TC2.3 | Role Selector | ✅ |
| TC2.4 | Attribute Selector | ✅ |
| TC2.5 | XPath | ✅ |
| TC2.6 | Click Action | ✅ |
| TC2.7 | Fill & Type | ✅ |
| TC2.8 | Check/Uncheck | ✅ |
| TC2.9 | Hover | ✅ |
| TC2.10 | Press Keys | ✅ |
| TC2.11 | Smart Waits | ✅ |
| TC2.12 | Complete Workflow | ✅ |

**Total: 12/12 Passing ✅**

---

## 💡 Best Practices

1. **Prefer Role Selectors** - Most reliable
2. **Use Text for Buttons** - Natural, readable
3. **Avoid XPath** - Complex, brittle
4. **Fill over Type** - Faster unless you need slow typing
5. **Let Playwright Wait** - Don't add explicit waits
6. **Test Real User Flow** - Don't just test individual actions

---

**Date**: Day 2
**Status**: ✅ Complete
**Tests**: 12/12 Passing