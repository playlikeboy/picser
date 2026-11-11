# 🚀 Picser - Free GitHub Image Hosting with jsDelivr CDN

> **Lightning-fast, self-hostable image hosting using GitHub repositories and jsDelivr CDN. Get permanent URLs that work forever, even if your repo gets deleted.**

![Picser Banner](https://cdn.jsdelivr.net/gh/playlikeboy/picser@main/public/og/og-image.png)

[![GitHub Stars](https://img.shields.io/github/stars/playlikeboy/picser?style=social)](

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/playlikeboy/picser)
[![Deploy to Cloudflare Pages](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/playlikeboy/picser)

[![Visitors](https://api.visitorbadge.io/api/combined?path=https%3A%2F%2Fgithub.com%2Fplaylikeboy%2Fpicser&countColor=%232ccce4&labelStyle=upper)](https://visitorbadge.io/status?path=https%3A%2F%2Fgithub.com%2Fplaylikeboy%2Fpicser)

## ✨ Why Choose Picser?

- **⚡ Lightning Fast**: Global jsDelivr CDN with 99.9% uptime and edge caching
- **🔒 Permanent URLs**: Commit-based URLs work even if repository/files are deleted
- **💰 Completely Free**: No limits, no subscriptions - just upload and share
- **🛡️ Self-Hostable**: Deploy on your own infrastructure for full control
- **🌍 Global CDN**: Images load instantly from 100+ edge locations worldwide
- **📦 Git-Backed**: All images stored in Git with full version control
- **🎨 Modern UI**: Beautiful glassmorphism interface built with Next.js 15 & Tailwind CSS
- **📱 Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **🔄 Upload History**: Track all your uploads with smart URL management
- **🏷️ Smart Badges**: Visual indicators for CDN status and URL permanence

## 🎯 Key Features

### 🖼️ **Smart Image Upload**

- Drag & drop interface with instant preview
- Support for JPG, PNG, GIF, WebP (up to 100MB)
- Automatic optimization and multiple URL formats

### ⚡ **jsDelivr CDN Integration**

- **Primary Feature**: Commit-based CDN URLs for maximum performance
- Global edge network with heavy caching
- Permanent links that survive repository changes
- 99.9% uptime guarantee

### 🔗 **Multiple URL Types**

1. **jsDelivr CDN (Permanent)** ⭐ *Recommended*
   - `https://cdn.jsdelivr.net/gh/user/repo@commit/image.png`
   - ✅ Lightning fast global CDN
   - ✅ Heavy caching and edge optimization
   - ✅ Permanent URLs (work even if repo deleted)

2. **Raw GitHub (Permanent)**
   - `https://raw.githubusercontent.com/user/repo/commit/image.png`
   - ✅ Direct GitHub access
   - ✅ Permanent commit-based URLs

3. **jsDelivr CDN (Dynamic)**
   - `https://cdn.jsdelivr.net/gh/user/repo@branch/image.png`
   - ✅ CDN performance
   - 📝 Updates with repository changes

### 🌐 **Public API**

- RESTful API for external integrations
- Support for user-provided GitHub credentials
- Comprehensive documentation with examples
- Edge runtime for global performance

### 📊 **Upload Management**

- Visual upload history with thumbnails
- One-click URL copying
- Repository source links
- File metadata tracking

## 🚀 Quick Start

### Option 1: One-Click Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/playlikeboy/picser)

[![Deploy to Cloudflare Pages](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/playlikeboy/picser)

### Option 2: Manual Setup

1. **Clone and Install**

```bash
npm install
```

Then, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Environment Setup

Create a `.env.local` file with your GitHub configuration:

```env
GITHUB_TOKEN=your_github_token
GITHUB_OWNER=your_github_username
GITHUB_REPO=your_repository_name
GITHUB_BRANCH=main
```

## GitHub Token Setup

1. Go to [GitHub Settings > Developer settings > Personal access tokens](https://github.com/settings/tokens)
2. Create a new **Fine-grained personal access token** or **Classic token**
3. For fine-grained tokens, select your repository and grant these permissions:
   - **Contents**: Write (to upload files)
   - **Metadata**: Read (to access repository info)
4. For classic tokens, select these scopes:
   - `repo` (Full control of private repositories)
5. Copy the token to your `.env.local` file

## 🚀 Quick Start Options

### Option 1: Use Hosted Version (Easiest) ⭐

**No setup required!** Use our hosted version directly:

```bash
curl -X POST \
  -F "file=@/path/to/your/image.png" \
  -F "github_token=ghp_your_token_here" \
  -F "github_owner=your_username" \
  -F "github_repo=your_repo" \
  https://picser.pages.dev/api/public-upload
```

**🔒 Privacy & Security:**

- Your credentials are used **only** for the upload request
- **Nothing is stored** on our servers
- Direct communication with GitHub API
- Completely stateless and secure

**🌐 Web Interface:** Visit [picser.pages.dev](https://picser.pages.dev) for drag-and-drop uploads!

### Option 2: Self-Host on Cloudflare Pages (Free)

1. **Fork the repository**: [github.com/playlikeboy/picser](https://github.com/playlikeboy/picser)
2. **Connect to Cloudflare Pages**:
   - Visit [Cloudflare Pages](https://pages.cloudflare.com)
   - Connect your GitHub account
   - Select your forked repository
3. **Deploy**: Cloudflare will automatically build and deploy
4. **Optional**: Add your custom domain

**Benefits of self-hosting:**

- ✅ Complete privacy and control
- ✅ Custom domain support
- ✅ Free hosting on Cloudflare Pages
- ✅ Global CDN included
- ✅ Automatic deployments from GitHub

## Usage

### 🌐 Using Hosted Version (Recommended)

**Web Interface:**

1. Visit [picser.pages.dev](https://picser.pages.dev)
2. Enter your GitHub credentials in the form
3. Drag and drop an image or click to browse
4. Get instant CDN URLs with multiple formats

**API Integration:**

1. Visit [picser.pages.dev/api-docs](https://picser.pages.dev/api-docs) for complete documentation
2. Use `https://picser.pages.dev/api/public-upload` endpoint
3. Send your GitHub credentials with each request
4. Get 6 different URL formats for your uploaded image

### 🏠 Self-Hosted Development

**Local Development:**

1. Configure your `.env.local` with your GitHub repository details
2. Run `npm run dev` and visit `http://localhost:3000`
3. Drag and drop an image or click to browse
4. Get 6 different URL formats for your uploaded image

**API Documentation:**

1. Visit `http://localhost:3000/api-docs` for complete API documentation
2. Test your GitHub configuration at `/api/test-config`
3. Use `/api/public-upload` to upload images to any GitHub repository

## 💡 Quick Example

**Upload an image using the hosted API:**

```bash
# Replace with your actual GitHub credentials
curl -X POST \
  -F "file=@screenshot.png" \
  -F "github_token=ghp_your_github_token" \
  -F "github_owner=your_username" \
  -F "github_repo=your_repo" \
  https://picser.pages.dev/api/public-upload
```

**Response (JSON):**

```json
{
  "success": true,
  "filename": "screenshot-1704123456789.png",
  "url": "https://cdn.jsdelivr.net/gh/user/repo@abc123/uploads/screenshot-1704123456789.png",
  "urls": {
    "jsdelivr_commit": "https://cdn.jsdelivr.net/gh/user/repo@abc123/uploads/screenshot-1704123456789.png",
    "raw_commit": "https://raw.githubusercontent.com/user/repo/abc123/uploads/screenshot-1704123456789.png",
    "github_commit": "https://github.com/user/repo/blob/abc123/uploads/screenshot-1704123456789.png"
  },
  "size": 142857,
  "type": "image/png"
}
```

**✨ That's it!** Your image is now available globally via jsDelivr CDN with a permanent URL.

### URL Types Explained

**Branch-based URLs** (may change if files are updated):

- `github`: View file in GitHub web interface
- `raw`: Direct access to raw file content  
- `jsdelivr`: Fast CDN access with global caching

**Commit-based URLs** (permanent, never change):

- `github_commit`: Permanent link to specific commit version
- `raw_commit`: Direct access to specific commit version
- `jsdelivr_commit`: CDN access to specific commit version

## Deployment

### Cloudflare Pages

This application is optimized for Cloudflare Pages with Edge Runtime:

1. Connect your GitHub repository to Cloudflare Pages
2. Set build command: `npm run build`
3. Set output directory: `.next`
4. Add environment variables in Cloudflare Pages settings
5. Deploy automatically on git push

### Vercel

Deploy easily on Vercel:

1. Connect your GitHub repository
2. Add environment variables  
3. Deploy with zero configuration

## Tech Stack

- **Framework**: Next.js 15 with App Router
- **Styling**: Tailwind CSS 4
- **Icons**: Lucide React
- **GitHub API**: Octokit/rest
- **TypeScript**: Full type safety
- **Storage**: GitHub repository + localStorage for history

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
