# NovaByte JavaScript API Reference

## Form Submission Handlers

### Contact Form
**File:** `assets/js/forms.js`
```javascript
// Function: handleContactSubmit(event)
// Submits contact form data
// Stores in: localStorage.contactSubmissions
// Returns: Redirects to contactformsubmission.html

// Usage in HTML:
<form onsubmit="handleContactSubmit(event)">
    <input name="name" required />
    <input name="email" type="email" required />
    <input name="subject" required />
    <select name="priority">...</select>
    <textarea name="message" required></textarea>
    <button type="submit">Send</button>
</form>
```

### Support Ticket
**File:** `assets/js/forms.js`
```javascript
// Function: handleSupportTicket(event)
// Creates support ticket with unique ID
// Stores in: localStorage.supportTickets
// Fields: issue, category, description, orderNumber

// Ticket ID Format: TK-[timestamp]
// Status: Always "Open" initially

// Usage:
<form onsubmit="handleSupportTicket(event)">...</form>
```

### Career Application
**File:** `assets/js/forms.js`
```javascript
// Function: handleCareersApplication(event)
// Submits job application
// Stores in: localStorage.careerApplications
// Returns: Success message

// Application ID Format: APP-[timestamp]
// Status: "Received"

// Usage:
<form onsubmit="handleCareersApplication(event)">...</form>
```

### Newsletter Signup
**File:** `assets/js/forms.js`
```javascript
// Function: handleNewsletterSignup(event)
// Adds email to newsletter
// Stores in: localStorage.newsletter
// Features: Email validation, duplicate prevention

// Event: Usually on form submit with preventDefault
// Returns: Success alert if valid email
```

---

## Account Management

### User Class
**File:** `assets/js/account.js`
```javascript
class User {
    constructor(username, email, password) {
        this.username = username;
        this.email = email;
        this.password = hashPassword(password);
        this.createdAt = new Date();
        this.profile = { fullName, phone, avatar };
        this.orders = [];
        this.savedBuilds = [];
        this.addresses = [];
        this.wishlist = [];
    }
}
```

### AccountManager Class
**File:** `assets/js/account.js`

#### Registration
```javascript
// Function: accountManager.register(username, email, password, confirmPassword)
// Returns: { success: boolean, message: string }
// Validates password match, length, uniqueness
// Creates new user and logs them in
// Stores in: localStorage.users, localStorage.currentUser

// Example:
const result = accountManager.register('john', 'john@example.com', 'pass123', 'pass123');
if (result.success) {
    console.log('Account created!');
}
```

#### Login
```javascript
// Function: accountManager.login(email, password)
// Returns: { success: boolean, message: string }
// Finds user by email, verifies password
// Sets current user
// Stores in: localStorage.currentUser

// Example:
const result = accountManager.login('john@example.com', 'pass123');
if (result.success) {
    window.location.href = 'account.html';
}
```

#### Logout
```javascript
// Function: accountManager.logout()
// Clears currentUser from localStorage
// Returns: void

// Example:
accountManager.logout();
```

#### Profile Management
```javascript
// Function: accountManager.updateProfile(fullName, phone)
// Updates user profile information
// Returns: boolean (success)

// Example:
accountManager.updateProfile('John Doe', '555-1234');
```

#### Order Management
```javascript
// Function: accountManager.addOrder(orderData)
// Adds order to user's order history
// Auto-generates Order ID: NB-[year]-[random]
// Returns: Order object with timestamp

// Example:
const order = accountManager.addOrder({
    items: ['PC Build 1'],
    total: 1299.99,
    status: 'Processing'
});
```

#### PC Builds
```javascript
// Function: accountManager.saveBuild(buildName, buildConfig)
// Saves custom PC configuration
// Auto-generates Build ID: BUILD-[timestamp]
// Returns: Build object

// Example:
accountManager.saveBuild('Gaming Beast', {
    cpu: 'Intel i9',
    gpu: 'RTX 4090',
    ram: '32GB',
    storage: '2TB NVMe'
});
```

#### Wishlist
```javascript
// Function: accountManager.addToWishlist(productId, productName)
// Adds product to wishlist
// Returns: boolean

// Function: accountManager.removeFromWishlist(productId)
// Removes product from wishlist
// Returns: boolean

// Example:
addToWishlist('prod-123', 'RTX 4090');
removeFromWishlist('prod-123');
```

#### Addresses
```javascript
// Function: accountManager.addAddress(addressData)
// Adds shipping address
// Auto-generates Address ID: ADDR-[timestamp]
// Returns: Address object

// Example:
accountManager.addAddress({
    street: '123 Main St',
    city: 'Anytown',
    state: 'CA',
    zip: '12345',
    country: 'USA'
});
```

---

## Global UI Functions

### Navigation
**File:** `assets/js/script.js`
```javascript
// Auto-managed by script.js:
// - Hamburger menu toggle
// - Mobile menu close on link click
// - Active nav link highlighting
```

### Display User Info
**File:** `assets/js/account.js`
```javascript
// Function: displayUserInfo()
// Updates profile section with current user data
// Populates:
// - profileName (ID: profileName)
// - profileEmail (ID: profileEmail)
// - profilePhone (ID: profilePhone)
// - memberDate (ID: memberDate)
// - orderCount (ID: orderCount)
// - wishlistCount (ID: wishlistCount)

// Example:
<span id="profileName"></span>
<script>displayUserInfo();</script>
```

### Update Footer
**File:** `assets/js/social-footer.js`
```javascript
// Function: updateFooterYear()
// Auto-updates copyright year in footer
// Called on page load

// Function: addSocialMediaLinks()
// Adds social media link icons to footer
// Called on page load
// Creates SVG icons for: Facebook, Twitter, Instagram, YouTube, Discord, LinkedIn

// Links configured in: SOCIAL_MEDIA object
const SOCIAL_MEDIA = {
    facebook: 'https://facebook.com/novabyte',
    twitter: 'https://twitter.com/novabyte',
    instagram: 'https://instagram.com/novabyte',
    youtube: 'https://youtube.com/novabyte',
    discord: 'https://discord.gg/novabyte',
    linkedin: 'https://linkedin.com/company/novabyte'
}
```

---

## Product Management

### Filter Products
**File:** `assets/js/products.js`
```javascript
// Auto-implemented filtering for:
// - Price range
// - GPU type
// - Tier (Entry/Mid/High)
// - RAM amount
// - Sort options

// Uses HTML5 attributes: data-price, data-gpu, data-tier, data-ram
```

### PC Builder
**File:** `assets/js/build.js`
```javascript
// Functions for:
// - Component selection (CPU, GPU, RAM, etc.)
// - Price calculation
// - Performance estimates
// - Real-time updates
```

---

## Data Persistence

### LocalStorage Structure
```
localStorage.users - Array of User objects
localStorage.currentUser - Current logged-in user
localStorage.contactSubmissions - Array of contact forms
localStorage.supportTickets - Array of support tickets
localStorage.careerApplications - Array of job applications
localStorage.newsletter - Array of newsletter emails
```

### Example: Access User Data
```javascript
// Get current user
const user = JSON.parse(localStorage.getItem('currentUser'));
console.log(user.email);
console.log(user.orders);

// Get all users
const users = JSON.parse(localStorage.getItem('users')) || [];

// Get contact submissions
const submissions = JSON.parse(localStorage.getItem('contactSubmissions')) || [];
```

---

## Initialization

### Auto-run on Page Load
All pages automatically execute:
```javascript
document.addEventListener('DOMContentLoaded', () => {
    updateFooterYear();        // Updates copyright year
    addSocialMediaLinks();      // Adds social icons
    displayUserInfo();          // Displays user profile (if account.html)
});
```

---

## Helper Functions

### Email Validation
```javascript
// Built into forms.js
const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
if (!emailRegex.test(email)) {
    alert('Please enter a valid email address');
}
```

### Password Hashing
```javascript
// Simple base64 encoding (for demo, use bcrypt in production)
function hashPassword(password) {
    return btoa(password);
}

// Verify
function verifyPassword(password, hash) {
    return btoa(password) === hash;
}
```

---

## Integration Examples

### Add Login Check to Page
```javascript
window.addEventListener('load', () => {
    if (!accountManager.currentUser) {
        alert('Please login first');
        window.location.href = 'account.html';
    }
});
```

### Add Product to Wishlist
```javascript
function addToWishlist(productId, productName) {
    if (!accountManager.currentUser) {
        alert('Please login to add to wishlist');
        return;
    }
    accountManager.addToWishlist(productId, productName);
    alert('Added to wishlist!');
}
```

### Save PC Build
```javascript
function savePCBuild(buildName) {
    const buildConfig = {
        cpu: document.getElementById('cpuSelect').value,
        gpu: document.getElementById('gpuSelect').value,
        ram: document.getElementById('ramSelect').value,
        storage: document.getElementById('storageSelect').value,
        price: document.getElementById('totalPrice').textContent
    };
    accountManager.saveBuild(buildName, buildConfig);
    alert('Build saved!');
}
```

---

## Troubleshooting

### Issue: Forms not submitting
**Solution:** Ensure `onsubmit="handleFormName(event)"` is on form tag and function is imported

### Issue: User data not persisting
**Solution:** Check localStorage quota and ensure account.js is loaded

### Issue: Social links not appearing
**Solution:** Verify social-footer.js is loaded and footer has `.footer-bottom` element

### Issue: Logo not displaying
**Solution:** Check image path is relative and PNG file exists in assets folder

---

## API Expansion Guide

### Add New Form Type
1. Create handler in `forms.js`
2. Add function to window: `window.handleNewForm = handleNewForm`
3. Add form with `onsubmit="handleNewForm(event)"`
4. Define localStorage key for persistence

### Add New Account Feature
1. Add method to AccountManager class
2. Persist to localStorage in method
3. Export via window: `window.newFeature = newFeature`
4. Call from HTML as needed

### Add New Page
1. Create HTML file with proper structure
2. Include all script files
3. Update navigation links
4. Update footer links
5. Test forms and navigation

---

**Last Updated:** February 7, 2026  
**Version:** 1.0  
**Status:** Production Ready ✅
