# PE Notes Website — Setup Guide

## 1. Upload each chapter to Google Drive with download blocked
For every chapter PDF:
1. Upload the PDF to your Google Drive.
2. Right-click it → **Share**.
3. Under "General access," set it to **Anyone with the link** → **Viewer**.
4. Click the settings gear icon (top-right of the share dialog) and **uncheck** "Viewers and commenters can download, print, and copy." This is available on a free personal Google account.
5. Copy the file's link — it looks like `https://drive.google.com/file/d/1AbCdEfGhIjKlMnOpQrS/view?usp=sharing`. The long string between `/d/` and `/view` is the **file ID** you need next.

## 2. Link each chapter to its file
Open `class-11.html` or `class-12.html` and find the chapter you want to connect. Each one has a link like:

```html
<a href="reader.html?id=PASTE_DRIVE_ID_HERE&title=Changing%20Trends...">Read Online</a>
```

Replace `PASTE_DRIVE_ID_HERE` with the file ID you copied in step 1. Do this for all 20 chapters as you upload them.

`reader.html` embeds that file in an in-page viewer on your own site — the visitor never leaves your domain, and the download/print controls stay disabled because of the Drive setting.

## 3. Host it for free — GitHub Pages
1. Create a free account at github.com if you don't have one.
2. Click **New repository**, name it exactly `<your-username>.github.io`.
3. Upload every file here (`index.html`, `class-11.html`, `class-12.html`, `buy-book.html`, `reader.html`, `style.css`) using **Add file → Upload files**.
4. Go to **Settings → Pages**, confirm the source is your main branch, root folder.
5. Your site is live at `https://<your-username>.github.io` within a couple of minutes.

You no longer need the `notes/` folder for chapter PDFs since they now live on Drive — feel free to delete it, or keep it for your own backup copies.

## 4. What this does and doesn't protect against
- ✅ Blocks the obvious paths: no download button, no "Save As," Ctrl+P gives a blocked/greyed-out print dialog from Drive's own viewer.
- ❌ Doesn't stop screenshots, screen recording, or someone photographing the screen. No web-based method can fully prevent that — treat this as a deterrent for casual copying, not airtight protection.

## 5. Set up the physical book order flow (free)
The "Order on WhatsApp" button on `buy-book.html` points to a placeholder number:
`https://wa.me/91XXXXXXXXXX?text=...`
Replace `91XXXXXXXXXX` with your real number in international format (e.g. `919812345678`). For payment, share a UPI ID or QR code manually after they message you — free, no setup. Razorpay Payment Pages (razorpay.com) can automate this later for a small per-transaction fee only.

## 6. Set up Amazon affiliate links (free)
1. Sign up at affiliate-program.amazon.in — free.
2. Once approved, generate affiliate links for each book from the Associates toolbar.
3. Replace the `href="#"` placeholders in the "Recommended reads" cards on `buy-book.html`.
4. Keep the earnings disclosure text — it's legally required.

## 7. Optional: a free custom domain
`<your-username>.github.io` already works at no cost. A shorter custom domain (like a `.com`/`.in`) typically runs ₹500–900/year from Namecheap or GoDaddy — the hosting itself stays free either way.
