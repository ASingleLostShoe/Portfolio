# Project Notes

## Portfolio Website Project (Paused)

### Goal
Convert professional portfolio from Coda.io document into a standalone website hosted on a custom domain.

### Decisions Made
- **Tech approach**: Static HTML/CSS/JS site (user has intermediate skills)
- **Hosting**: Not set up yet. Recommended options: Netlify, GitHub Pages, or Vercel (all free for static sites)
- **Domain**: User owns a domain (name not specified yet)
- **Design inspiration**: Field Operations website (https://www.fieldoperations.net/projects.html)

### Progress Made

#### Files Created/Modified
- `index.html` - Main site structure with all content
- `styles.css` - Responsive styling (minimal white/gray theme)
- `images/` folder with project thumbnails

#### Design Overhaul (Latest Session)
Redesigned site to match Field Operations aesthetic:

**Layout Changes:**
- Changed from blue gradient theme to minimal white/gray design
- Navigation now uses lowercase text with letter-spacing
- Hero section simplified: left-aligned, no background gradient
- Consolidated all 12 projects into a single unified grid (removed category headers)
- Project cards now show just image + title + technology/location (descriptions hidden)
- Text overlays on images with gradient fade for readability

**Dynamic Tile System:**
- Added Masonry.js library for masonry-style grid layout
- Added imagesLoaded.js to calculate positions after images load
- JavaScript randomly assigns tile sizes on each page load
- Tile sizes available:
  - `size-small` - 1 column (1/6 width)
  - `size-medium` - 2 columns (1/3 width)
  - `size-tall` - 2 columns, taller height
  - `size-wide` - 3 columns (1/2 width)
  - `size-large` - 3 columns, taller height
- Up to 6 tiles can fit side-by-side on wide screens

**Responsive Behavior:**
- Grid re-layouts on window resize (debounced)
- Breakpoints:
  - **> 1400px**: 6 columns max
  - **1000-1400px**: 4 columns
  - **768-1000px**: 3 columns
  - **500-768px**: 2 columns
  - **< 500px**: 1 column (full width)
- Consistent 10px gaps between all tiles (horizontal and vertical)

**Libraries Added (via CDN):**
- Masonry.js v4: `https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js`
- imagesLoaded v5: `https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js`

#### Site Structure
1. **Navigation** - Fixed navbar with lowercase links (about, experience, projects, contact)
2. **Hero Section** - Name, title, description, specialty tags, CTA buttons
3. **About Section** - Brief intro paragraph
4. **Experience Section** - 4 work positions + 2 education entries (2-column grid)
5. **Portfolio Section** - 12 projects in dynamic masonry grid
6. **Contact Section** - Links to LinkedIn, GitHub, Email
7. **Footer**

#### Contact Links
- LinkedIn: https://www.linkedin.com/in/pjh-geospatial/
- GitHub: https://github.com/ASingleLostShoe
- Email: pjh.geospatial@gmail.com

#### Project Images
All 12 project cards have thumbnail images:
- `parcel-map.jpg` - Aerial city map (Unsplash)
- `WVDrought.png` - User-provided image
- `miami-beach.jpg` - Coastal cityscape (Unsplash)
- `boulder-hazard.jpg` - Mountain landscape (Unsplash)
- `delivery-network.jpg` - Urban streets (Unsplash)
- `cool-roofs.jpg` - Urban rooftops aerial (Unsplash)
- `lidar.jpg` - Forest canopy (Unsplash)
- `geotiff.jpg` - Code/data matrix (Unsplash)
- `plastic-atlas.jpg` - Plastic materials (Unsplash)
- `wheat-ridge.jpg` - Cycling infrastructure (Unsplash)
- `tableau.jpg` - Data dashboard (Unsplash)
- `coda-pm.jpg` - Project planning (Unsplash)

### Attempted but Reverted
- **Dark mode**: Attempted to add automatic dark mode based on system preferences using `prefers-color-scheme` media query, but it was not detecting light mode correctly. Reverted to light-only theme.

### Next Steps When Resuming
1. Add links to GitHub repos and Story Maps for each project
2. Revisit dark mode implementation if desired
3. Replace placeholder images with actual project screenshots (optional)
4. Set up hosting and connect the domain
5. Consider adding individual project detail pages

### Source Files
- Original content extracted from: `Pat Hall Portfolio.pdf`
- Text extraction saved to: `portfolio_text.txt`

### Notes
- User is comfortable with HTML/CSS and can follow technical instructions
- No hosting currently configured, only the domain
- All Unsplash images are free to use, no attribution required
- Site uses external CDN libraries (Masonry.js, imagesLoaded) - consider self-hosting for production
