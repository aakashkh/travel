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

1. Create `.md` file in `content/posts/`
2. Add front matter with metadata:
   ```yaml
   ---
   title: "Your Post Title"
   ShowToc: true
   comments: true
   featured_image: "/travel/images/your-image.jpg"
   ---
   ```
3. Use custom shortcodes for enhanced content
4. Add images to `static/images/[post-name]/`

## 🖼️ Image Slider Usage

```markdown
{{< slider id="my-gallery" >}}
  <div><img src="/travel/images/photo1.jpg" alt="Description"></div>
  <div><img src="/travel/images/photo2.jpg" alt="Description"></div>
{{< /slider >}}
```

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