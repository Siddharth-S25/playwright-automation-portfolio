# 📖 Day 1: Foundations & Setup

## ✅ Completed Tasks

- [x] Initialized npm project
- [x] Installed Playwright
- [x] Created playwright.config.js
- [x] Created first test file
- [x] All 5 tests passing

## 🎯 Test Results

Running 5 tests using 1 worker

- ✓ TC1.1 - Navigate to website and verify title
- ✓ TC1.2 - Verify page heading and input field exist
- ✓ TC1.3 - Test different selector types on same element
- ✓ TC1.4 - Test filling input and checking element visibility
- ✓ TC1.5 - Test element visibility and DOM attachment checks
- 5 passed (52.0s) ✅

## 📚 Key Learnings

### Website Used: TodoMVC
- URL: https://demo.playwright.dev/todomvc/
- Real, stable demo app for testing
- Perfect for learning Playwright

### Test Structure (AAA Pattern)
```javascript
test('name', async ({ page }) => {
  // Arrange: Setup
  await page.goto(url);
  
  // Act: Do something
  await element.fill('text');
  
  // Assert: Verify
  await expect(element).toHaveValue('text');
});
```

### 3 Selectors Learned

1. **CSS Selector**
```javascript
   page.locator('input[placeholder="What needs to be done?"]')
```

2. **Role Selector (BEST)**
```javascript
   page.locator('role=textbox')
```

3. **Attribute Selector**
```javascript
   page.locator('[placeholder*="needs"]')
```

### Assertions Used

| Assertion | What it checks |
|-----------|----------------|
| `toHaveTitle()` | Page title matches |
| `toBeVisible()` | Element visible on page |
| `toBeAttached()` | Element in DOM |
| `toBeHidden()` | Element hidden |
| `toHaveValue()` | Input field value |

## 🧪 Tests Created

| Test | Status | Time |
|------|--------|------|
| TC1.1 | ✅ Pass | 21.0s |
| TC1.2 | ✅ Pass | 4.6s |
| TC1.3 | ✅ Pass | 5.8s |
| TC1.4 | ✅ Pass | 6.7s |
| TC1.5 | ✅ Pass | 5.6s |

**Total: 5/5 Passing ✅**

## 💡 Commands Used
```bash
npm init -y
npm install --save-dev @playwright/test
npx playwright install
npm test
npm run test:report
```

## 🎓 What's Next (Day 2)

- Advanced selectors
- Action methods (click, type, hover)
- Smart waits
- Handling forms

