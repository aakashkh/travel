# Travel Blog - Hugo Site

A travel blog built with Hugo featuring enhanced blog posts with custom shortcodes and organized image galleries.

## 📁 Folder Structure

### Source Files (What You Edit)

**`content/`** - Your blog content
- `posts/` - All blog posts (.md files)
  - `kuari-pass.md`, `kota-trip.md`, etc.
- `_index.md` - Homepage content

**`static/`** - Static assets (images, files)
- `images/` - Your organized photos
  - `kota-trip/`, `kuari-pass/` folders

**`layouts/`** - Custom HTML templates
- `shortcodes/` - Custom components (alert, gallery, etc.)

**`assets/`** - Processed assets
- `css/custom.css` - Your custom styles

**`themes/ananke/`** - Theme files (don't edit directly)

**`hugo.toml`** - Site configuration

### Generated Files (Hugo Creates These)

**`public/`** - Final website (generated when you build)
- `posts/` - HTML versions of your blog posts
- `images/` - Copied from static/
- `categories/`, `tags/` - Auto-generated taxonomy pages

**`resources/`** - Hugo's cache for processed assets

## 🚀 Quick Start

### Option 1: Using Batch File (Recommended for Windows)
```bash
.\run-server.bat
```

### Option 2: Direct Hugo Commands
1. **Install Hugo Extended:**
   ```bash
   winget install Hugo.Hugo.Extended
   ```

2. **Start Development Server:**
   ```bash
   hugo server -D
   ```

3. **Build for Production:**
   ```bash
   hugo --minify
   ```

**View Site:** http://localhost:1313

## 🎨 Custom Features

- **Image Slider/Carousel:** Hugo Codex slider for photo galleries
- **GitHub Comments:** Giscus integration using GitHub Discussions
- **Custom Shortcodes:** Alert boxes, trek stats, weather guides
- **Enhanced Blog Posts:** Featured images, TOC, reading time
- **Organized Images:** Structured gallery system
- **Responsive Design:** Mobile-friendly layouts with wider content area

## 🔄 Hugo Build Process

1. **Source**: `content/posts/kota-trip.md`
2. **Processing**: Hugo + Theme + Shortcodes  
3. **Output**: `public/posts/kota-trip/index.html`

## 📝 Adding New Posts

1. **Create post file:**
   ```bash
   hugo new posts/my-new-post.md
   ```

2. **Create image folders:**
   ```
   assets/images/my-new-post/
   assets/images/my-new-post/gallery/
   ```

3. **Add optimized images:**
   - Hero image: `assets/images/my-new-post/hero.jpg`
   - Gallery images: `assets/images/my-new-post/gallery/`

4. **Update front matter:**
   ```yaml
   ---
   title: "Your Post Title"
   featured_image: "/images/my-new-post/hero.jpg"
   ShowToc: true
   comments: true
   ---
   ```

5. **Use responsive images in content:**
   ```markdown
   {{< img src="images/my-new-post/photo.jpg" alt="Description" >}}
   ```

## 🖼️ Image Management

### Adding Images to New Posts

1. **Create folder structure:**
   ```
   assets/images/[post-name]/
   assets/images/[post-name]/gallery/
   ```

2. **Optimize images before adding:**
   - **Format:** JPG/PNG (avoid HEIC)
   - **Size:** Max 1920px width
   - **Quality:** 80-90% for hero images, 70-80% for gallery

3. **Use responsive image shortcode:**
   ```markdown
   {{< img src="images/post-name/photo.jpg" alt="Description" >}}
   ```

4. **Gallery slider usage:**
   ```markdown
   {{< slider id="my-gallery" >}}
     <div>{{< img src="images/post-name/gallery/photo1.jpg" alt="Description" >}}</div>
     <div>{{< img src="images/post-name/gallery/photo2.jpg" alt="Description" >}}</div>
   {{< /slider >}}
   ```

### Image Processing Features
- **Auto-compression:** WebP format at 75% quality
- **Responsive sizes:** 400px, 800px, 1200px widths
- **Lazy loading:** Images load when visible
- **Size reduction:** 50-70% smaller files

## 💬 Comments System

- **Powered by:** GitHub Discussions (Giscus)
- **Features:** Login with GitHub, reactions, replies, moderation
- **Setup:** Enable Discussions in GitHub repo settings
- **Usage:** Add `comments: true` to post front matter

## 🛠️ Development Workflow

```bash
# Create new post
hugo new posts/my-new-post.md

# Start development server
hugo server -D

# Build for production
hugo --minify
```

## 🚀 Deployment

**GitHub Pages (Automatic):**
1. Push to GitHub repository: `https://github.com/aakashkh/travel`
2. GitHub Actions automatically builds and deploys
3. Site available at: `https://aakashkh.github.io/travel/`

**Local Development:**
```bash
# Start development server
hugo server -D

# Build for production
hugo --minify
```

**Manual Deploy:**
1. Run `hugo --minify`
2. Upload `public/` folder to web server