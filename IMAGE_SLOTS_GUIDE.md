# NovaByte Image Slots Guide

## Overview
All pages now have image slots ready for you to add banner images and content images. Simply replace the file paths with your actual image files.

---

## Image Slots by Page

### 1. **home.html** - Hero Banner
**Location:** Hero section (top of page)  
**Image Path:** `assets/game.webp`  
**Recommended Size:** 1920x600px  
**Purpose:** Main hero banner background  
**Edit:** Change the `url('assets/game.webp')` to your image path

---

### 2. **products.html** - Products Section Banner
**Location:** Products section header  
**Image Path:** `assets/products-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Products page banner background  
**Edit:** Update `url('assets/products-banner.png')` with your image

---

### 3. **about.html** - About Hero Banner
**Location:** About hero section  
**Image Path:** `assets/about-banner.png`  
**Recommended Size:** 1920x500px  
**Purpose:** Company/team information banner  
**Edit:** Update `url('assets/about-banner.png')` with your image

---

### 4. **contact.html** - Contact Page Banner
**Location:** Page header section  
**Image Path:** `assets/contact-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Contact and support page banner  
**Edit:** Update `url('assets/contact-banner.png')` with your image

---

### 5. **careers.html** - Careers Banner
**Location:** Careers hero section  
**Image Path:** `assets/careers-banner.png`  
**Recommended Size:** 1920x500px  
**Purpose:** Job opportunities and company culture banner  
**Edit:** Update `url('assets/careers-banner.png')` with your image

---

### 6. **blog.html** - Blog Header Banner
**Location:** Blog hero section  
**Image Path:** `assets/blog-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Blog articles and tech insights banner  
**Edit:** Update `url('assets/blog-banner.png')` with your image

---

### 7. **FAQ.html** - FAQ Banner
**Location:** FAQ hero section  
**Image Path:** `assets/faq-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Help center and FAQ banner  
**Edit:** Update `url('assets/faq-banner.png')` with your image

---

### 8. **warranty.html** - Warranty Banner
**Location:** Warranty header section  
**Image Path:** `assets/warranty-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Warranty and protection plans banner  
**Edit:** Update `url('assets/warranty-banner.png')` with your image

---

### 9. **financing.html** - Financing Banner
**Location:** Financing header section  
**Image Path:** `assets/financing-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Payment plans and financing options banner  
**Edit:** Update `url('assets/financing-banner.png')` with your image

---

### 10. **reviews.html** - Reviews Banner
**Location:** Reviews header section  
**Image Path:** `assets/reviews-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Customer reviews and testimonials banner  
**Edit:** Update `url('assets/reviews-banner.png')` with your image

---

### 11. **support.html** - Support Banner
**Location:** Support consultation header  
**Image Path:** `assets/support-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Expert support and consultation banner  
**Edit:** Update `url('assets/support-banner.png')` with your image

---

### 12. **checkout.html** - Checkout Banner
**Location:** Page header section  
**Image Path:** `assets/checkout-banner.png`  
**Recommended Size:** 1920x400px  
**Purpose:** Shopping cart and checkout banner  
**Edit:** Update `url('assets/checkout-banner.png')` with your image

---

## How to Add Images

### Step 1: Save Your Images
Place your banner images in the `assets/` folder

### Step 2: Update the Image Paths
Find the corresponding file and locate the `url()` reference  
Replace with your image filename

### Example:
**Current:** `background-image: url('assets/game.webp');`  
**Updated:** `background-image: url('assets/my-banner.png');`

---

## Recommended Image Specifications

| Aspect | Size | Format | Notes |
|--------|------|--------|-------|
| **Width** | 1920px | Common | Desktop standard |
| **Height** | 400-600px | Common | Varies by section |
| **Format** | PNG, JPG, WebP | Supported | WebP recommended (faster) |
| **File Size** | <500KB | Optimal | Compressed for web |
| **Compression** | 70-85% quality | Recommended | Good quality/size balance |

---

## Quick Setup Guide

1. **Create banner images** using Photoshop, Canva, or online tools
2. **Export** in PNG or WebP format (1920 x 400-600px)
3. **Compress** to reduce file size (use TinyPNG.com or similar)
4. **Save** to `assets/` folder with matching names:
   - `game.webp` (or your hero image)
   - `products-banner.png`
   - `about-banner.png`
   - `contact-banner.png`
   - `careers-banner.png`
   - `blog-banner.png`
   - `faq-banner.png`
   - `warranty-banner.png`
   - `financing-banner.png`
   - `reviews-banner.png`
   - `support-banner.png`
   - `checkout-banner.png`

5. **Done!** Images will automatically display on each page

---

## Tips for Best Results

- ✅ Use high-quality banner images
- ✅ Ensure images are the correct aspect ratio
- ✅ Compress images for faster loading
- ✅ Test on mobile to ensure good appearance
- ✅ Use consistent design style across all banners
- ✅ Include overlay text if needed (design in advance)

---

## Support
All images use responsive CSS with `background-size: cover` and `background-position: center`, ensuring they look good on all screen sizes.
