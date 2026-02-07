# 🧪 TESTING GUIDE - How to Test All New Features

## Quick Testing Checklist

### 1. PC CUSTOMIZER (customize.html)
- [ ] Click "Build PC" in navigation
- [ ] Select CPU from dropdown list
- [ ] Select GPU option
- [ ] Pick RAM configuration
- [ ] Choose storage (SSD or HDD)
- [ ] Select CPU cooler
- [ ] Choose PSU wattage
- [ ] Pick case design
- [ ] **Verify:** Total price updates in sidebar ✓
- [ ] **Verify:** Compatibility status shows ✓
- [ ] **Verify:** Performance metrics display ✓
- [ ] Click "Save Build" button - name your build
- [ ] Click "Add to Cart" - should show success message
- [ ] Check cart badge in navigation - should show 1 item
- [ ] **Action:** Try incompatible components (e.g., Intel CPU with AMD motherboard)
   - Should show red warning about socket mismatch

### 2. REVIEWS PAGE (reviews.html)
- [ ] Click "Reviews" link (on home page or in footer)
- [ ] **Verify:** Shows 4.8 rating and 2,847 reviews
- [ ] Click "★★★★★ 5 Stars" filter button
- [ ] **Verify:** Shows only 5-star reviews
- [ ] Click "✓ Verified Purchases" filter
- [ ] **Verify:** Shows only verified review badges
- [ ] Scroll to review form section
- [ ] Enter your details in review form
- [ ] Click star rating (select 5 stars)
- [ ] Enter review title and text
- [ ] Click "Submit Review"
- [ ] **Verify:** Success message appears
- [ ] **Verify:** Your review appears at top of list with ✓ Verified badge

### 3. WARRANTY PAGE (warranty.html)
- [ ] Click "Warranty Plans" in footer
- [ ] **Verify:** 3 main plans displayed (Standard, Extended, Premium Pro)
- [ ] **Verify:** Pricing shown: Included, $199, $349
- [ ] Scroll down to see coverage comparison table
- [ ] **Verify:** Table shows differences between plans
- [ ] Scroll to "Protection Add-ons" section
- [ ] Hover over add-on cards - check styling
- [ ] Click "Add to Cart" on add-ons
- [ ] **Verify:** Button changes to "✓ Added"
- [ ] Scroll to FAQ section
- [ ] Click FAQ questions - they expand with answers
- [ ] Click again - they collapse

### 4. FINANCING PAGE (financing.html)
- [ ] Click "Financing Options" in footer or home page
- [ ] **Verify:** Payment calculator visible at top
- [ ] Drag price slider left and right
- [ ] **Verify:** Monthly payment updates instantly
- [ ] Select "24 Months" from duration dropdown
- [ ] **Verify:** Monthly payment recalculates
- [ ] Scroll to financing cards
- [ ] **Verify:** 3 partners shown (Affirm, PayPal, Klarna)
- [ ] **Verify:** Interest rates and terms displayed
- [ ] Scroll down to FAQ accordion
- [ ] Click accordion items - they expand
- [ ] Verify each answer content appears
- [ ] Click benefit cards - verify styling

### 5. EXPERT SUPPORT PAGE (support.html)
- [ ] Click "Support" in navigation or links
- [ ] **Verify:** Live chat widget visible on left
- [ ] Verify it shows "Online Now" status
- [ ] Type a message in chat input
- [ ] Press Enter or click "Send"
- [ ] **Verify:** Your message appears in chat
- [ ] **Verify:** Auto-reply appears after 1-2 seconds
- [ ] Scroll down to see expert team
- [ ] **Verify:** 4 expert cards with avatars
- [ ] Click phone number to test calling
- [ ] Scroll to consultation form
- [ ] Fill out form fields
- [ ] Submit consultation
- [ ] **Verify:** Success message appears

### 6. NAVIGATION UPDATES (All Pages)
- [ ] Go to any page (home, products, about, etc.)
- [ ] Check top navigation menu
- [ ] **Verify:** "Build PC" link exists
- [ ] Click it - should go to customize.html ✓
- [ ] Check footer links
- [ ] **Verify:** "Warranty Plans" → warranty.html ✓
- [ ] **Verify:** "Financing" → financing.html ✓
- [ ] **Verify:** "Reviews" visible on pages ✓
- [ ] **Verify:** Cart badge shows item count ✓
- [ ] Click cart icon → goes to checkout.html ✓
- [ ] Click account icon → goes to account.html ✓

### 7. HOME PAGE UPDATES (home.html)
- [ ] Go to home.html
- [ ] Scroll down past featured products
- [ ] **Verify:** New "More Than Just PCs" section visible
- [ ] **Verify:** 4 feature cards shown:
   - 🛠️ Custom PC Builder
   - ⭐ Customer Reviews (2,800+)
   - 🛡️ Warranty Plans (up to 5-year)
   - 💳 Flexible Financing (0% APR)
- [ ] Hover over cards - check hover effects
- [ ] Click each card - should navigate to relevant page ✓
- [ ] Scroll to footer
- [ ] Check footer has updated links

### 8. SHOPPING WORKFLOW
- [ ] Go to customize.html
- [ ] Build a custom PC (select all 8 components)
- [ ] **Verify:** "Add to Cart" button becomes enabled
- [ ] Click "Add to Cart"
- [ ] **Verify:** Success notification shows
- [ ] **Verify:** Cart badge shows "1" item
- [ ] Click cart icon
- [ ] **Verify:** You're on checkout page
- [ ] **Verify:** Your custom build is listed in cart
- [ ] Fill out shipping info
- [ ] Select shipping method
- [ ] Fill out payment info
- [ ] Click "Complete Order"
- [ ] **Verify:** Order confirmation page shows
- [ ] **Verify:** Shows order ID, date, items, total

### 9. ACCOUNT PAGE (account.html)
- [ ] Go to account.html
- [ ] **Verify:** Your profile displays (or shows login prompt)
- [ ] If logged in, verify profile info shows:
   - Full name
   - Email
   - Phone
   - Member since date
- [ ] **Verify:** Order history section shows
- [ ] **Verify:** Your order from above appears in list
- [ ] Click "Edit Profile"
- [ ] Change name and phone
- [ ] **Verify:** Profile updates instantly

### 10. LOCAL STORAGE VERIFICATION
- [ ] Open Developer Tools (F12)
- [ ] Go to Application tab → LocalStorage
- [ ] **Verify:** You can see:
   - `shoppingCart` - should have items
   - `currentBuild` - your custom build
   - `reviews` - user-submitted reviews
   - `currentUser` - logged-in user data
- [ ] Click on each to view contents
- [ ] Data should persist after page refresh

---

## 🎯 TEST SCENARIOS

### Scenario 1: Complete Builder & Purchase
1. Start on home page
2. Click "Custom PC Builder" card
3. Build PC with components
4. Save build with custom name
5. Add to cart
6. Go to checkout
7. Fill order form
8. Place order
9. See order confirmation
10. Go to account - verify order appears

### Scenario 2: Review & Warranty
1. Go to Reviews page
2. Read existing reviews
3. Filter by rating
4. Submit new review
5. Go to Warranty page
6. Compare plans
7. Add protection add-ons
8. View FAQ

### Scenario 3: Financing Check
1. Go to Financing page
2. Use calculator for different prices
3. Check different durations
4. Review financing partners
5. Read FAQ about credit impact
6. Check benefit cards

### Scenario 4: Get Expert Help
1. Go to Support page
2. Send live chat message
3. Scroll to expert team
4. View expert profiles
5. Fill consultation booking
6. See form confirmation

---

## ✅ EXPECTED RESULTS

### Customizer
- Price updates in real-time
- Compatibility warnings appear for socket mismatches
- Performance metrics show appropriate tier
- Builds save to localStorage
- Add to cart adds to shopping cart

### Reviews
- Can filter by rating
- Can filter by verified purchases
- Can submit new reviews
- Reviews appear immediately
- Ratings display correctly
- Average rating shows 4.8 stars

### Warranty
- 3 plans displayed with pricing
- Coverage table compares all plans
- Add-ons can be toggled
- FAQ items expand/collapse
- All sections responsive

### Financing
- Calculator updates in real-time
- Monthly payment calculates correctly
- 3 financing partners display
- Interest rates shown for each
- FAQ accordion works
- All responsive on mobile

### Support
- Live chat messages send
- Auto-reply appears
- Expert team displays with info
- Consultation form submits
- Multiple contact options listed
- All styling matches site theme

### Navigation
- All new links work
- Footer links point to right pages
- Cart badge shows correct count
- Active state highlights current page
- Mobile hamburger menu works

### Home Page
- New services section visible
- Cards have hover effects
- Cards link to correct pages
- Footer updated with new links
- All responsive

---

## 🐛 DEBUGGING TIPS

If something doesn't work:

1. **Check Browser Console** (F12)
   - Look for JavaScript errors
   - Check Network tab for 404s

2. **Check LocalStorage**
   - Open DevTools → Application → LocalStorage
   - Verify data is saving

3. **Clear Cache**
   - Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
   - Or clear browser cache manually

4. **Check File Paths**
   - All images should use `assets/` path
   - All scripts should load from `assets/js/`

5. **Test in Incognito**
   - Opens fresh browser session
   - No cache interference
   - LocalStorage still works

---

## 📱 MOBILE TESTING

Test on mobile devices or mobile emulation:

- [ ] All pages responsive
- [ ] Navigation adapts for smaller screens
- [ ] Chat widget displays correctly
- [ ] Forms are easy to fill on mobile
- [ ] Buttons are touch-friendly (40x40px minimum)
- [ ] Text readable at mobile sizes
- [ ] Images scale properly
- [ ] No horizontal scrolling issues

Use DevTools → Toggle Device Toolbar (Ctrl+Shift+M) for testing.

---

## 🎉 COMPLETION CHECKLIST

Once you've tested everything:

- [ ] All new pages load without errors
- [ ] Navigation links all work
- [ ] Customizer builds PCs and adds to cart
- [ ] Reviews submit and display
- [ ] Warranty plans show correctly
- [ ] Financing calculator works
- [ ] Support page functional
- [ ] Home page shows new features
- [ ] All data persists to localStorage
- [ ] Mobile responsive works
- [ ] No console errors
- [ ] All forms validate
- [ ] Styling matches theme
- [ ] Links navigate correctly
- [ ] Success messages appear

**If all checkmarks complete - Site is ready for use/deployment!** ✅
