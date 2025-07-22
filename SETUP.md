# 🚀 Complete Setup & Configuration Guide

Welcome to your Minecraft Portal template! This guide will walk you through everything you need to know to customize and deploy your professional server website.

## 📋 Table of Contents

- [Quick Start](#-quick-start)
- [Complete Configuration Reference](#-complete-configuration-reference)
- [Customization Examples](#-customization-examples)
- [Deployment Guide](#-deployment-guide)
- [Troubleshooting](#-troubleshooting)
- [Advanced Features](#-advanced-features)

---

## 🚀 Quick Start

### System Requirements

- **Node.js**: Version 18.0.0 or higher
- **npm**: Usually comes with Node.js
- **Modern Browser**: Chrome, Firefox, Safari, or Edge
- **Text Editor**: VS Code recommended

### Installation Steps

1. **Open Terminal/Command Prompt**
   - Windows: Search "PowerShell" or "cmd"
   - Mac: Press Cmd+Space, type "Terminal"
   - Linux: Press Ctrl+Alt+T

2. **Navigate to Template**

   ```bash
   cd ReactVer
   ```

3. **Install Dependencies**

   ```bash
   npm install
   ```

   This downloads all required libraries and tools.

4. **Start Development Server**

   ```bash
   npm run dev
   ```

5. **Open in Browser**
   - Visit the URL shown in the console.
   - You should see your website running!

### First Configuration

1. **Open `public/config.json` in your text editor**
2. **Update basic information:**

   ```json
   {
     "general-info": {
       "name": "Your Server Name Here",
       "theme-color": "#e5383b"
     },
     "minecraft-widget": {
       "ip": "play.yourserver.com"
     }
   }
   ```

3. **Save the file**
4. **Reload the website and see your changes live.**

---

## 🎛️ Complete Configuration Reference

### 🏠 General Information

```json
{
  "general-info": {
    "theme-color": "#e5383b",
    "name": "Your Server Name",
    "page-title": "Your Server - Amazing Minecraft Experience",
    "description": "This is the new kind of minecraft experience.",
    "meta-tags": "minecraft,server,gaming,portal,multiplayer,community",
    "author": "Your Name",
    "language": "en"
  }
}
```

**Options Explained:**

- `theme-color`: Main color (generates entire palette automatically)
- `name`: Your server's display name
- `page-title`: The title shown in browser tabs
- `description`: Appears in search results and social shares
- `meta-tags`: Search engine keywords (comma-separated, no spaces)
- `author`: Website creator (for SEO)
- `language`: Two-letter language code (en, es, fr, de, etc.)

### 🔍 Advanced SEO Configuration

```json
{
  "seo": {
    "title": "Your Server - Best Minecraft Server | Join Now",
    "description": "Join the best Minecraft server! Active community, Discord channel, regular events. Copy IP and start playing right now!",
    "keywords": "Minecraft, server, game, Discord, multiplayer, community, best server",
    "author": "Your Server Team",
    "robots": "index, follow",
    "language": "en",
    "canonical_url": "https://yourserver.com"
  }
}
```

**SEO Options Explained:**

- `title`: Main SEO title (appears in Google search results)
- `description`: Meta description for search engines (160 characters max)
- `keywords`: SEO keywords (comma-separated with spaces allowed)
- `author`: Content author for search engines
- `robots`: Search engine crawling instructions
- `language`: Language code for search engines
- `canonical_url`: Primary URL for this page (prevents duplicate content)

### 📱 Social Media SEO (Open Graph)

```json
{
  "open-graph": {
    "title": "Your Server - Best Minecraft Server",
    "description": "Join the best Minecraft server! Active community, Discord channel, regular events.",
    "type": "website",
    "url": "https://yourserver.com",
    "image": "https://yourserver.com/img/title.png",
    "site_name": "Your Server",
    "locale": "en_US"
  }
}
```

**Open Graph Options:**

- `title`: Title when shared on social media
- `description`: Description when shared on social media
- `type`: Content type (usually "website")
- `url`: Canonical URL of the page
- `image`: Full URL to preview image (1200x630px recommended)
- `site_name`: Your website/brand name
- `locale`: Language and region code

### 🐦 Twitter Card Configuration

```json
{
  "twitter": {
    "card": "summary_large_image",
    "title": "Your Server - Best Minecraft Server",
    "description": "Join the best Minecraft server! Active community, Discord channel, regular events.",
    "image": "https://yourserver.com/img/title.png",
    "site": "@YourTwitterHandle"
  }
}
```

**Twitter Options:**

- `card`: Card type ("summary_large_image" recommended)
- `title`: Title when shared on Twitter
- `description`: Description when shared on Twitter
- `image`: Full URL to preview image
- `site`: Your Twitter handle (optional)

### 🖼️ Favicon Configuration

```json
{
  "favicons": {
    "favicon": "/favicon.ico",
    "apple-touch-icon": "/apple-touch-icon.png",
    "favicon-32x32": "/favicon-32x32.png",
    "favicon-16x16": "/favicon-16x16.png",
    "manifest": "/site.webmanifest"
  }
}
```

**Favicon Options:**

- `favicon`: Main favicon file (ICO format)
- `apple-touch-icon`: iOS home screen icon (180x180px)
- `favicon-32x32`: 32x32px PNG favicon
- `favicon-16x16`: 16x16px PNG favicon
- `manifest`: Web app manifest file

### 🎮 Minecraft Server Widget

```json
{
  "minecraft-widget": {
    "ip": "play.yourserver.com",
    "enable-widget": true,
    "enable-tracking": true
  }
}
```

**Options Explained:**

- `ip`: Your Minecraft server's IP address or domain (without http:// or port)
- `enable-widget`: Show/hide the entire server status widget
- `enable-tracking`: Enable live player count tracking (uses mcstatus.io API)

**Widget Behavior:**

- **When tracking is enabled and server is online**: Shows live player count
- **When tracking is enabled and server is offline**: Shows offline message from lang config
- **When tracking is disabled**: Shows only the server IP for copying

**Server Status Detection:**

The widget automatically detects if your server is offline by checking:
1. If the mcstatus.io API can reach your server
2. If the API returns valid player data
3. If there are any network connectivity issues

When offline, it displays the customizable offline message from your language configuration.

### 💬 Discord Server Widget

```json
{
  "discord-widget": {
    "invite-link": "https://discord.gg/yourinvite",
    "server-id": "123456789012345678",
    "enable-widget": true,
    "enable-tracking": false
  }
}
```

**Options Explained:**

- `invite-link`: Your Discord server invite URL
- `server-id`: 18-digit Discord server ID (from Discord Developer Portal)
- `enable-widget`: Show/hide Discord widget
- `enable-tracking`: Show live member count

**Finding Your Discord Server ID:**

1. Enable Developer Mode in Discord (User Settings > Advanced)
2. Right-click your server name
3. Click "Copy Server ID"

### 🖼️ Images and Media

```json
{
  "images": {
    "logo": "img/title.png",
    "background": "img/bg.jpg",
    "favicon": "img/minecraft.svg",
    "discord-logo": "img/discord.svg",
    "minecraft-logo": "img/minecraft.svg",
    "facebook-logo": "img/facebook.svg",
    "instagram-logo": "img/instagram.svg",
    "tiktok-logo": "img/tiktok.svg",
    "twitter-logo": "img/twitter.svg",
    "telegram-logo": "img/telegram.svg"
  }
}
```

**Adding Custom Images:**

1. Place your image in `public/img/` folder
2. Add reference to config:

   ```json
   "images": {
     "my-custom-logo": "img/my-logo.png"
   }
   ```

3. Use anywhere in config with key `"my-custom-logo"`

### 🌐 Navigation Menu

```json
{
    "navbar": [
        {
            "text": "Home",
            "link": "#"
        },
        {
            "text": "Store",
            "link": "https://store.yourserver.com"
        },
        {
            "text": "Rules",
            "link": "/rules"
        }
    ]
}
```

**Options Explained:**

- `text`: Display text for the navigation item
- `link`: URL destination (use "#" for current page or full URLs for external links)

### 📱 Social Media Links

```json
{
    "social-media-links": {
        "facebook": {
            "icon": "facebook-logo",
            "link": "https://facebook.com/yourpage"
        },
        "instagram": {
            "icon": "instagram-logo",
            "link": "https://instagram.com/yourpage"
        },
        "discord": {
            "icon": "discord-logo",
            "link": "https://discord.gg/yourinvite"
        },
        "tiktok": {
            "icon": "tiktok-logo",
            "link": "https://tiktok.com/@yourpage"
        },
        "twitter": {
            "icon": "twitter-logo",
            "link": "https://twitter.com/yourpage"
        },
        "telegram": {
            "icon": "telegram-logo",
            "link": "https://t.me/yourgroup"
        }
    }
}
```

**Options Explained:**

- `icon`: Reference to image key from the images section
- `link`: Full URL to your social media profile or group
- Remove any platform you don't use to hide it from the website

### 🦶 Footer Configuration

```json
{
    "footer": {
        "enable-footer": true,
        "enable-logo": true,
        "logo-text": "The best Minecraft server with amazing community and custom features!",
        "categories": [
            {
                "title": "Navigation",
                "links": [
                    {"text": "Home", "link": "/"},
                    {"text": "Store", "link": "/store"},
                    {"text": "Rules", "link": "/rules"}
                ]
            },
            {
                "title": "Community",
                "links": [
                    {"text": "Discord", "link": "https://discord.gg/yourinvite"},
                    {"text": "Forums", "link": "/forums"}
                ]
            }
        ]
    }
}
```

**Options Explained:**

- `enable-footer`: Show/hide the entire footer section
- `enable-logo`: Show/hide logo in footer
- `logo-text`: Descriptive text about your server (appears below logo)
  - **Set to empty string (`""`) to center the logo vertically without text**
  - **When logo is disabled, footer links automatically center**
- `categories`: Organized groups of footer links
    - `title`: Category heading text
    - `links`: Array of link objects with `text` and `link` properties

**Footer Layout Options:**

- **Standard Layout**: Logo + text on left, links on right
- **Centered Logo**: Set `logo-text: ""` to center logo vertically (no text)
- **Centered Links**: Set `enable-logo: false` to center footer links
- **Disabled Footer**: Set `enable-footer: false` to hide entire footer

### 🌍 Language & Text Customization

```json
{
    "lang": {
        "click-to-copy-ip": "Click to copy server IP",
        "ip-copied": "IP has been copied to clipboard!",
        "minecraft-people-online": "Currently ${minecraft-online} people online",
        "minecraft-server-offline": "Server is currently offline",
        "join-discord": "Join our Discord server",
        "discord-people-online": "Currently ${discord-online} people online",
        "footer-links-title": "Quick Links",
        "copyright": "© 2025 ${general-info.name}. All rights reserved."
    }
}
```

**Options Explained:**

- `click-to-copy-ip`: Small text inside the minecraft widget (tooltip text)
- `ip-copied`: Success message after copying IP to clipboard
- `minecraft-people-online`: Player count display text (use ${minecraft-online} for dynamic count)
- `minecraft-server-offline`: Message shown when server is offline or unreachable
- `join-discord`: Small text inside the discord widget
- `discord-people-online`: Discord member count text (use ${discord-online} for dynamic count)
- `footer-links-title`: Footer section heading
- `copyright`: Footer copyright text (use ${general-info.name} for server name)

**Text Variables:**

- `${minecraft-online}`: Current online players (only when server is online)
- `${discord-online}`: Current Discord members
- `${general-info.name}`: Server name from config

**Server Status Messages:**

The minecraft widget shows different messages based on server status:
- **Server Online + Tracking Enabled**: Shows `minecraft-people-online` with player count
- **Server Offline + Tracking Enabled**: Shows `minecraft-server-offline` message
- **Tracking Disabled**: Shows only the server IP for copying

---

## 🎨 Customization Examples

### Gaming Community Server

```json
{
    "general-info": {
        "name": "Epic Gaming Network",
        "description": "The ultimate Minecraft gaming experience",
        "theme-color": "#7289da"
    },
    "minecraft-widget": {
        "ip": "play.epicgaming.net",
        "enable-tracking": true
    },
    "lang": {
        "minecraft-people-online": "${minecraft-online} gamers online",
        "join-discord": "Join the Epic Community"
    }
}
```

### Roleplay Server

```json
{
    "general-info": {
        "name": "Medieval Kingdoms",
        "description": "Enter a world of medieval roleplay and adventure",
        "theme-color": "#8b4513"
    },
    "lang": {
        "minecraft-people-online": "${minecraft-online} citizens in the realm",
        "minecraft-server-offline": "The kingdom is currently closed",
        "join-discord": "Join the Royal Court"
    }
}
```

### Competitive PvP Server

```json
{
    "general-info": {
        "name": "Pro PvP Arena",
        "description": "Test your skills in competitive Minecraft PvP",
        "theme-color": "#ff6b35"
    },
    "lang": {
        "minecraft-people-online": "${minecraft-online} warriors online",
        "minecraft-server-offline": "Arena is temporarily closed",
        "join-discord": "Join the Battle"
    }
}
```

### Creative Building Server

```json
{
    "general-info": {
        "name": "Creative Builders Hub",
        "description": "Unleash your creativity in our building community",
        "theme-color": "#00a8cc"
    },
    "lang": {
        "minecraft-people-online": "${minecraft-online} builders creating",
        "minecraft-server-offline": "Creative world is offline",
        "join-discord": "Share Your Builds"
    }
}
```

---

## 🚀 Deployment Guide

### Building for Production

1. **Build the website:**

   ```bash
   npm run build
   ```

2. **This creates a `dist/` folder** with your optimized website

### Hosting Options

#### 🌐 Static Hosting (Recommended)

**Netlify (Free)**

1. Visit [netlify.com](https://netlify.com)
2. Drag the `dist/` folder to the deploy area
3. Your site is live instantly!

**Vercel (Free)**

1. Visit [vercel.com](https://vercel.com)
2. Import your project or upload `dist/` folder
3. Automatic deployments on changes

**GitHub Pages (Free)**

1. Create repository on GitHub
2. Upload `dist/` contents to `gh-pages` branch
3. Enable GitHub Pages in repository settings

#### 🖥️ Traditional Web Hosting

1. **Upload `dist/` folder contents** to your web server's root directory
2. **Ensure your server supports Single Page Applications (SPA)**
3. **Configure redirects** if needed for React Router

### Domain Configuration

1. **Point your domain** to the hosting service
2. **Update `canonical-url`** in config to your domain
3. **Test all functionality** after deployment

---

## 🔧 Troubleshooting

### Common Issues & Solutions

#### ❌ Server Status Not Showing

**Problem**: Minecraft widget shows "Offline" when server is online

**Solutions:**

1. **Check server IP format:**

   ```json
   "ip": "play.yourserver.com"  // ✅ Correct
   "ip": "https://play.yourserver.com"  // ❌ Wrong
   ```

2. **Verify server accepts status queries:**
   - Most servers allow this by default
   - Check server.properties: `enable-query=true`

3. **Test API manually:**
   - When looking up your server on [MCS](https://mcstatus.io/)
   - The website should return server data

#### ❌ Discord Widget Not Working

**Problem**: Discord member count not showing

**Solutions:**

1. **Verify Server ID is 18 digits:**

   ```json
   "server-id": "123456789012345678"  // ✅ Correct (18 digits)
   "server-id": "12345"  // ❌ Wrong (too short)
   ```

2. **Enable Discord Widget:**
   - Server Settings > Widget
   - Enable "Enable Server Widget"

3. **Check Server Privacy:**
   - Ensure server is not private/invite-only for widget API

#### ❌ Images Not Loading

**Problem**: Logo or background images don't appear

**Solutions:**

1. **Verify file paths:**

   ```json
   "logo": "img/my-logo.png"  // ✅ Correct (relative to public/)
   "logo": "/img/my-logo.png"  // ❌ May cause issues
   ```

2. **Check file exists:**
   - Ensure image is in `public/img/` directory
   - File names are case-sensitive

3. **Supported formats:**
   - PNG, JPG, SVG, WebP

#### ❌ Colors Not Applying

**Problem**: Theme color changes don't show

**Solutions:**

1. **Valid hex color format:**

   ```json
   "theme-color": "#e5383b"  // ✅ Correct
   "theme-color": "red"  // ❌ Use hex codes
   ```

2. **Clear browser cache:**
   - Hard refresh: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)

3. **Restart development server:**

   ```bash
   npm run dev
   ```

#### ❌ Configuration Errors

**Problem**: Website shows default content after config changes

**Solutions:**

1. **Validate JSON syntax:**
   - Use a JSON validator online
   - Check for missing commas, quotes, or brackets

2. **Check file encoding:**
   - Save config.json as UTF-8

3. **Verify file location:**
   - Must be `public/config.json`

### Development Tips

#### 🔍 Browser Console

1. **Open Developer Tools:**
   - F12 or Right-click > Inspect

2. **Check Console tab for errors:**
   - Red errors indicate problems
   - Yellow warnings are usually okay

#### 📝 Configuration Validation

**Valid JSON Example:**

```json
{
  "general-info": {
    "name": "My Server",
    "theme-color": "#e5383b"
  }
}
```

**Common Mistakes:**

```json
{
  "general-info": {
    "name": "My Server",  // ✅ Comma needed
    "theme-color": "#e5383b"  // ✅ No comma on last item
  },  // ❌ Remove comma before closing brace
}
```

#### 🚀 Building and testing

1. **Test build locally:**

   ```bash
   npm run build
   npm run preview
   ```

---

## 🎯 Advanced Features

### Custom Particle Effects

**Modify `public/cfg/particlesjs-config.json`:**

```json
{
  "particles": {
    "number": {
      "value": 80
    },
    "color": {
      "value": "#ffffff"
    }
  }
}
```

### Analytics Integration

**Add to HTML head in index.html:**

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### Custom CSS Styling

**Add to `src/App.css`:**

```css
/* Custom styles */
.my-custom-class {
  background: var(--theme-color);
  color: white;
  padding: 1rem;
}
```

---

## 📊 Performance Optimization

### Image Optimization

1. **Compress images** before adding to `public/img/`
2. **Use WebP format** for better compression
3. **Recommended sizes:**
   - Logo: 200x60px
   - Background: 1920x1080px
   - Icons: 32x32px or SVG file format

### Loading Speed

1. **Minimize config.json** - remove unused sections
2. **Optimize particle count** in particles config
3. **Use CDN** for faster global loading

---

## 🛡️ Security Considerations

### Configuration Security

1. **Don't include sensitive data** in config.json
2. **Use environment variables** for API keys
3. **Validate user inputs** if adding forms

### Deployment Security

1. **Use HTTPS** for production
2. **Keep dependencies updated:**

   ```bash
   npm audit
   npm update
   ```

3. **Secure server** hosting the Minecraft server

---

**🎮 You're all set! Your professional Minecraft server website is ready to impress your community.**

**Need more help? Check the troubleshooting section or review the configuration examples above.**
