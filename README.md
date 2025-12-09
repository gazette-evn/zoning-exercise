# Teaching Demo Site Setup

This folder contains everything needed to host the exercise materials on GitHub Pages.

## Folder Structure

```
site/
├── index.html                      # Student landing page (links to all materials)
├── city/
│   └── downtown-initiative.html    # City of Riverside webpage (has hidden HTML)
├── developer/
│   └── index.html                  # Meridian Development Group website
├── files/
│   ├── planning-email.txt          # Email with revealing headers
│   ├── zoning-policy-memo.docx     # YOU CREATE: Word doc with Meridian author metadata
│   └── mayor-working-photo.jpg     # YOU ADD: The close-up photo (for EXIF exercise)
└── images/
    └── developer-meeting.jpg       # YOU ADD: The wide shot (appears on developer site)
```

## Setup Checklist

### 1. Add Your Images

- [ ] Save the **close-up photo** (documents on glass table) as `files/mayor-working-photo.jpg`
- [ ] Save the **wide shot** (developer meeting) as `images/developer-meeting.jpg`

**Important for EXIF:** The close-up photo needs real EXIF GPS data. Either:
- Use one of your AI-generated images as a reference, but take a real photo to use for the actual exercise
- Or manually embed EXIF data using a tool like ExifTool

### 2. Create the Word Document

1. Open `../exercise-files/zoning-policy-memo.md` in Microsoft Word
2. Save as `files/zoning-policy-memo.docx`
3. Add metadata:
   - **Author:** `Marcus Thompson - Meridian Development Group`
   - **Company:** `Meridian Development Group`
4. Save again

### 3. Set Up GitHub Pages

1. Create a new GitHub repo (e.g., `teaching-demo-exercise`)
2. Upload the entire `site/` folder contents to the repo root
3. Go to Settings → Pages
4. Set Source to "Deploy from a branch"
5. Select `main` branch, `/ (root)` folder
6. Save

Your site will be live at: `https://yourusername.github.io/teaching-demo-exercise/`

### 4. Test Everything

- [ ] City page loads and has hidden elements in source
- [ ] Developer page loads and shows the meeting photo
- [ ] Word doc downloads and has correct metadata
- [ ] Email file downloads
- [ ] Photo downloads with EXIF data intact
- [ ] All links work

## URLs for Students

Once hosted, give students this link:
```
https://yourusername.github.io/teaching-demo-exercise/
```

They'll see:
- Links to all the exercise files
- The city website (for HTML inspection)

**Note:** Don't give them the developer site URL directly — they should find it through investigation (or you reveal it during the photo discussion).

## The Investigation Flow

1. **City website** → Students find hidden links to Meridian docs, developer agreement
2. **Policy memo** → Author metadata reveals Meridian wrote it
3. **Email** → Headers show it came from Meridian's servers
4. **Photo EXIF** → GPS shows it wasn't taken at City Hall
5. **Find developer site** → Same table/carpet in their team photo

## Notes on EXIF

GitHub Pages and most web hosting **preserve EXIF data** in images. However, some image optimization tools strip it.

To ensure EXIF is preserved:
- Don't run images through any optimizer
- Upload the original file directly
- Test by downloading and checking EXIF after deployment

