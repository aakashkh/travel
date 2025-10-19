# Travel Blog - Hugo Site

A travel blog built with Hugo featuring enhanced blog posts with custom shortcodes, organized image galleries, and interactive features.

## 📁 Folder Structure

### Source Files (What You Edit)

**`content/`** - Your blog content
- `posts/` - All blog posts (.md files)
  - `kuari-pass.md`, `kota-trip.md`, etc.
- `_index.md` - Homepage content
- `search.md` - Search page

**`assets/`** - Processed assets
- `images/` - Your organized photos (optimized by Hugo)
  - `kota-trip/`, `kuari-pass/` folders
- `css/custom.css` - Your custom styles

**`layouts/`** - Custom HTML templates
- `shortcodes/` - Custom components (alert, gallery, etc.)
- `partials/` - Reusable components (search, social share, etc.)

**`themes/PaperMod/`** - Theme files (don't edit directly)

**`hugo.toml`** - Site configuration

### Generated Files (Hugo Creates These)

**`public/`** - Final website (generated when you build)
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

## 🎨 Features

### 🔍 Interactive Features
- **Search & Filters** - Find posts by location, difficulty, season
- **Related Posts** - Similar destinations automatically suggested
- **Social Sharing** - Twitter, Facebook, WhatsApp, Email, Copy Link
- **Print-Friendly** - Clean offline itinerary printing
- **Comments** - GitHub Discussions integration (Giscus)

### 🖼️ Image Optimization
- **Responsive Images** - Auto-generates 3 sizes (400px, 800px, 1200px)
- **WebP Compression** - 75% quality, 50-70% size reduction
- **Lazy Loading** - Images load when visible
- **Image Slider/Carousel** - Hugo Codex slider for photo galleries

### 📱 Modern Features
- **Mobile-Friendly** - Responsive design
- **Dark Mode** - Auto theme switching
- **TOC** - Table of contents for long posts
- **Reading Time** - Estimated read duration
- **Breadcrumbs** - Easy navigation

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
   tags: ["location", "difficulty", "season"]
   categories: ["Trekking", "Travel"]
   ---
   ```

5. **Use responsive images in content:**
   ```markdown
   {{< img src="images/my-new-post/photo.jpg" alt="Description" >}}
   ```

## 🔍 Search & Filtering

Posts are automatically searchable and filterable by:
- **Location** - Himalayas, Rajasthan, Himachal Pradesh
- **Difficulty** - Easy, Moderate, Hard
- **Season** - Winter, Summer, Monsoon

Add relevant tags to your posts for better filtering.

## 💬 Comments System

- **Powered by:** GitHub Discussions (Giscus)
- **Features:** Login with GitHub, reactions, replies, moderation
- **Setup:** Enable Discussions in GitHub repo settings
- **Usage:** Add `comments: true` to post front matter

## 🗂️ Data & Layout System

### Using Data Files
- **`data/destinations.yaml`** - Structured destination information
- **`data/travel_tips.yaml`** - Packing lists, safety tips, seasonal guides

### Custom Shortcodes
```markdown
# Display destination info from data
{{< destination-card destination="kuari_pass" >}}

# Show packing checklist
{{< packing-list >}}

# Display safety guidelines
{{< safety-tips >}}

# Responsive image with optimization
{{< img src="images/post-name/photo.jpg" alt="Description" >}}
```

### Layout Templates
- **`layouts/_default/destinations.html`** - All destinations page
- **`layouts/shortcodes/`** - Reusable components
- **`layouts/partials/`** - Page sections (search, social share, etc.)

## 🛠️ Development Workflow

```bash
# Create new post
hugo new posts/my-new-post.md

# Add destination data
# Edit data/destinations.yaml

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

## 📊 Performance

- **Site Size:** ~25MB (down from 100MB with image optimization)
- **Load Time:** <2 seconds on 3G
- **Lighthouse Score:** 95+ on all metrics
- **Image Savings:** 50-70% through WebP compression

## 🎯 SEO Features

- **Structured Data** - Rich snippets for search engines
- **Open Graph** - Social media previews
- **Twitter Cards** - Enhanced Twitter sharing
- **Sitemap** - Auto-generated XML sitemap
- **Robots.txt** - Search engine instructions

## 🔧 Customization

- **CSS:** Edit `assets/css/extended/custom.css`
- **Layouts:** Modify files in `layouts/`
- **Shortcodes:** Add custom components in `layouts/shortcodes/`
- **Config:** Update `hugo.toml` for site settings

## 📱 Mobile Optimization

- **Responsive Design** - Works on all screen sizes
- **Touch-Friendly** - Large buttons and easy navigation
- **Fast Loading** - Optimized images and minimal CSS/JS
- **Offline Reading** - Print-friendly layouts

## 📊 Data-Driven Features

### Destination Management
- **Centralized data** in YAML files
- **Consistent information** across all posts
- **Easy updates** - change once, reflect everywhere
- **Structured display** with custom layouts

### Available Shortcodes
- **destination-card** - Shows destination details from data
- **packing-list** - Essential items by category
- **safety-tips** - Important safety guidelines
- **img** - Responsive images with WebP compression
- **slider** - Image carousel galleries
- **social-share** - Share buttons for social media

### Menu Structure
- **Posts** - All blog entries
- **Search** - Filter by location, difficulty, season
- **Destinations** - Data-driven destination overview
- **Tags** - Browse by topics

## 🌟 Future Enhancements

- **Interactive Maps** - Route visualization
- **Weather Widgets** - Best time to visit
- **Cost Calculators** - Budget planning tools
- **Trip Planner** - Multi-destination itineraries
- **Bookmarks** - Save favorite posts
- **PWA Support** - Offline reading capability