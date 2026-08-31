# HAMZA Watch Images - Reference Mapping

## Image to Watch Mapping Guide

Use this guide to name and organize your watch image files correctly.

---

## Marine Collection (Divers)
| Image File | Watch Name | Type | Price | Description |
|---|---|---|---|---|
| `imag1.jpg` | Neptune Abyss | Diver | ₹4,299 | 200m water resistance and a luminous, unidirectional bezel |
| `imag8.jpg` | Cosmos Skeleton | Diver | ₹6,499 | An open-worked dial exposing the movement beneath |
| `imag9.jpg` | Blue Horizon | Diver | ₹5,799 | A travel-ready GMT hand and ocean-blue dial for crossing time zones |
| `imag13.jpg` | Pacific Deep | Diver | ₹5,199 | A blue-dial diver with a steel bracelet and high-contrast lume |
| `imag14.jpg` | Aqualite 300 | Diver | ₹6,999 | A serious dive companion with a ceramic bezel and screw-down crown |
| `imag15.jpg` | Harbour Watch | Diver | ₹4,499 | An easy-wearing everyday diver with a practical date window |

---

## Chronograph Collection (Precision Timing)
| Image File | Watch Name | Type | Price | Description |
|---|---|---|---|---|
| `imag2.jpg` | Pulse Chronos | Chronograph | ₹5,499 | A sharp tri-compax dial with timing precision to the fifth of a second |
| `imag6.jpg` | Velocity RS | Chronograph | ₹5,999 | Racing-red accents, brushed steel and a sapphire-coated crystal |
| `imag11.jpg` | Sprint Chrono | Chronograph | ₹4,699 | A compact racing chronograph with a clean, readable layout |
| `imag16.jpg` | Stealth Black | Chronograph | ₹5,799 | A blacked-out chronograph with crisp white timing registers |
| `imag17.jpg` | Track One | Chronograph | ₹4,999 | A compact motorsport-inspired chronograph for fast-moving days |
| `imag18.jpg` | Velocity Tach | Chronograph | ₹6,299 | A detailed tachymeter bezel rewards a closer look |

---

## Heritage Collection (Classic Dress)
| Image File | Watch Name | Type | Price | Description |
|---|---|---|---|---|
| `imag3.jpg` | Elegance Crown | Classic | ₹3,799 | Slim proportions, domed crystal and a warm gold-toned bezel |
| `imag7.jpg` | Blossom Rose | Classic | ₹3,999 | Rose-tone case and a soft blush dial in classic proportions |
| `imag10.jpg` | Midnight Noir | Classic | ₹3,599 | Minimal black dial, slim case and a strap that softens with wear |
| `imag19.jpg` | Silver Grand | Classic | ₹4,299 | A refined silver dial with an oversized date display |
| `imag20.jpg` | Cream Dial | Classic | ₹3,899 | Warm ivory dial details in a slim case |
| `imag21.jpg` | Regent Steel | Classic | ₹4,599 | A polished steel bracelet brings the Regent into the week |
| `imag22.jpg` | Ocean Blue | Classic | ₹4,199 | A cool blue dial with gold accents in refined proportions |

---

## Field Collection (Adventure)
| Image File | Watch Name | Type | Price | Description |
|---|---|---|---|---|
| `imag4.jpg` | Shadow Trail | Field | ₹3,299 | A matte, high-contrast companion for trails, travel and daily knocks |
| `imag5.jpg` | Horizon Pro | Field | ₹4,899 | Cockpit-inspired legibility with an oversized crown for easy adjustment |
| `imag12.jpg` | Explorer Trail | Field | ₹2,899 | Lightweight, water-resistant and built around a dial you can read at a glance |

---

## Quick Setup Instructions

### Step 1: Prepare Your Images
1. Collect all 22 watch images (or use placeholder images)
2. Name them exactly as shown in the mapping above:
   - `imag1.jpg`
   - `imag2.jpg`
   - ... up to `imag22.jpg`

### Step 2: Placement Options

**Option A: Same Folder (Recommended for local testing)**
```
hamzaWatchesWeb/
├── index.html
├── shop.html
├── about.html
├── brand.html
├── contact.html
├── imag1.jpg
├── imag2.jpg
├── ...
└── imag22.jpg
```

**Option B: Images Subfolder (Better for production)**
```
hamzaWatchesWeb/
├── index.html
├── shop.html
├── images/
│   ├── imag1.jpg
│   ├── imag2.jpg
│   ├── ...
│   └── imag22.jpg
```

If using Option B, update the image references in HTML:
```javascript
// Change this:
['Neptune Abyss','Diver','Hamza Marine',4299,7999,'imag1',...

// To this:
['Neptune Abyss','Diver','Hamza Marine',4299,7999,'images/imag1',...
```

### Step 3: Verify
1. Open `shop.html` in a browser
2. All 22 watches should display with images
3. Images should be properly sized and aligned

---

## Image Specifications (Recommended)

### File Format
- **Format:** JPG or PNG
- **Size:** 400×400px minimum (square images recommended)
- **Quality:** 72-100 DPI for web
- **File Size:** 50-200KB per image (optimized for web)

### Dimensions for Different Uses
- **Thumbnail:** 200×200px
- **Product Grid:** 300×300px
- **Product Detail:** 600×600px (if needed in future)

### Color Space
- **sRGB** (standard for web)
- **No alpha channel needed** (no transparency required)

---

## File Naming Convention

**Current Format:** `imag[1-22].[ext]`

Examples:
- ✅ `imag1.jpg` - Correct
- ✅ `imag10.png` - Correct
- ❌ `image1.jpg` - Wrong (needs 'imag', not 'image')
- ❌ `imag1.JPG` - Case sensitive (use lowercase)
- ❌ `imag1.gif` - Format (use jpg/png)

---

## Bulk Rename Script (Windows PowerShell)

If you have 22 images in the folder and want to rename them:

```powershell
# Navigate to your images folder
cd C:\Users\nik20\OneDrive\Desktop\hamzaWatchesWeb

# Rename files in sequence
$images = Get-ChildItem *.jpg | Sort-Object
$count = 1
foreach ($img in $images) {
    Rename-Item $img.FullName "imag$count.jpg"
    $count++
}
```

---

## Testing the Images

### Test 1: Shop Page
1. Open `shop.html`
2. All 22 watches should appear in a grid
3. All images should be visible (not broken links)
4. Images should be square/rectangular and properly sized

### Test 2: Brand Filtering
1. Go to `shop.html`
2. Click "Marine" filter
3. Should show only 6 diver watches (imag1, 8, 9, 13, 14, 15)
4. Click "Chronograph" filter
5. Should show only 6 chronograph watches (imag2, 6, 11, 16, 17, 18)

### Test 3: Individual Brand Pages
1. Navigate to `brand.html?brand=Hamza%20Marine`
2. Should show 6 Marine collection watches
3. Navigate to `brand.html?brand=Hamza%20Chrono`
4. Should show 6 Chronograph collection watches

### Test 4: Mobile Responsiveness
1. Open `shop.html` on mobile device
2. Images should scale properly
3. Grid should stack to 2 columns on mobile
4. All images should remain visible

---

## Troubleshooting

### Images Not Showing
**Problem:** Seeing broken image icon (?)  
**Solution:** 
- Check file names match exactly (case-sensitive)
- Verify file extension is `.jpg` or `.png`
- Ensure files are in correct folder
- Check browser console for 404 errors

### Images Look Pixelated
**Problem:** Images appear low quality  
**Solution:**
- Use higher resolution images (min 400×400px)
- Check file isn't compressed too much
- Increase file size if too aggressive optimization

### Wrong Images Display
**Problem:** Images show under wrong watches  
**Solution:**
- Verify image numbering is sequential
- Check product array in HTML matches image numbers
- Ensure no images are missing (must be 22 total)

---

## Backup Reference: Old External URLs

If you need to restore the original external image URLs:

### Marine Collection
- Neptune Abyss: https://www.king-wear.com/photo/pl198789280-kw252a_premium_classic_design_amoled_smart_watch.jpg
- Cosmos Skeleton: https://www.datocms-assets.com/99008/1697469125-epic_x_black-red.webp
- Blue Horizon: https://raritywatches.com/wp-content/uploads/2023/01/Epos-3504-Diver-blue-3.jpg
- Pacific Deep: https://raritywatches.com/wp-content/uploads/2023/01/Epos-3504-Diver-blue-3.jpg
- Aqualite 300: https://www.datocms-assets.com/99008/1697469125-epic_x_black-red.webp
- Harbour Watch: https://www.king-wear.com/photo/pl198789280-kw252a_premium_classic_design_amoled_smart_watch.jpg

*[Additional URLs for other collections available upon request]*

---

## Summary

| Metric | Value |
|--------|-------|
| **Total Images** | 22 |
| **File Format** | JPG or PNG |
| **Naming Pattern** | imag1, imag2, ... imag22 |
| **Min Resolution** | 400×400px |
| **Recommended Size** | 300×300px (grid view) |
| **Max File Size** | 200KB (optimized) |

---

**Last Updated:** August 31, 2026  
**Image System Version:** 1.0 - Local Integration
