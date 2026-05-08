# REMCO International Ltd - Design System

This document outlines the core components, typography, and color palette for the REMCO International Ltd website. It serves as a master reference to ensure consistency across all pages.

## 1. Global Styles & Theming

The site relies on Tailwind CSS for styling. Below is the core configuration that should be present on every page.

### Color Palette
- **Primary (Logo Green)**: `#397441` *(Updated from #5d7e62 to match the new logo)*
- **Navy**: `#1F3A4A`
- **Carrier Blue**: `#004595`
- **Toshiba Red**: `#E4002B`
- **Background Light**: `#f7f7f7`
- **Background Dark**: `#171b18`

### Typography
- **Primary Font**: `Inter`, sans-serif (Google Fonts)
- **Weights**: 300, 400, 500, 600, 700, 800, 900
- **Iconography**: Material Symbols Outlined

### Tailwind Configuration Snippet
Include this inside the `<head>` of every document:
```html
<script id="tailwind-config">
    tailwind.config = {
        darkMode: "class",
        theme: {
            extend: {
                colors: {
                    "primary": "#397441", 
                    "navy": "#1F3A4A",
                    "carrier-blue": "#004595",
                    "toshiba-red": "#E4002B",
                    "background-light": "#f7f7f7",
                    "background-dark": "#171b18",
                },
                fontFamily: {
                    "display": ["Inter", "sans-serif"]
                },
                borderRadius: {
                    "DEFAULT": "0.25rem",
                    "lg": "0.5rem",
                    "xl": "0.75rem",
                    "full": "9999px"
                },
            },
        },
    }
</script>
<style>
    body { font-family: 'Inter', sans-serif; }
</style>
```

---

## 2. Master Components

These components are identical across all pages to maintain global layout consistency.

### A. Top Contact Strip
Placed at the very top of the page, above the navigation bar.

```html
<div class="bg-navy text-white/90 py-2 px-6 lg:px-20 flex flex-wrap justify-between items-center text-xs font-medium border-b border-white/10">
    <div class="flex gap-6">
        <span class="flex items-center gap-2">
            <span class="material-symbols-outlined text-sm">call</span>
            +255 2137773 / 2133297
        </span>
        <span class="flex items-center gap-2">
            <span class="material-symbols-outlined text-sm">mail</span>
            remco@cats-net.co.tz
        </span>
    </div>
    <div class="hidden md:flex gap-4 items-center">
        <span>Official Carrier & Toshiba Dealer</span>
        <div class="h-3 w-px bg-white/20"></div>
        <span>Dar es Salaam, Tanzania</span>
    </div>
</div>
```

### B. Sticky Navigation Bar
Contains the new logo. The logo image should be named `logo.png` and placed in your assets folder.

```html
<nav class="sticky top-0 z-50 bg-white/95 backdrop-blur-md shadow-sm border-b border-gray-100 px-6 lg:px-20 py-4">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
        
        <!-- Logo Section -->
        <div class="flex items-center">
            <a href="index.html">
                <img src="logo.png" alt="REMCO (International) Ltd" class="h-12 md:h-14 w-auto object-contain" />
            </a>
        </div>
        
        <!-- Links -->
        <div class="hidden lg:flex items-center gap-8">
            <a href="index.html" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">Home</a>
            <a href="#" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">About</a>
            <a href="#" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">Solutions</a>
            <a href="#" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">Projects</a>
            <a href="#" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">Certifications</a>
            <a href="#" class="text-navy text-sm font-bold uppercase tracking-wider hover:text-primary transition-colors">Contact</a>
        </div>
        
        <!-- CTA -->
        <button class="bg-primary text-white px-6 py-2.5 rounded-lg text-sm font-bold uppercase tracking-widest hover:bg-primary/90 transition-all shadow-md active:scale-95">
            Get a Quote
        </button>
    </div>
</nav>
```

### C. Footer
Contains quick links, contact information, and the new logo.

```html
<footer class="bg-white pt-24 pb-12 px-6 lg:px-20 border-t border-gray-100">
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-20">
        
        <!-- Company Info & Logo -->
        <div>
            <div class="flex items-center mb-8">
                <img src="logo.png" alt="REMCO (International) Ltd" class="h-12 w-auto object-contain" />
            </div>
            <p class="text-gray-500 text-sm leading-relaxed mb-8">Authorized Carrier and Toshiba dealer in Tanzania with 27+ years of engineering excellence in premium HVAC systems.</p>
            <div class="flex gap-4">
                <a href="#" class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center text-navy hover:bg-primary hover:text-white transition-colors">
                    <span class="material-symbols-outlined text-lg">public</span>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center text-navy hover:bg-primary hover:text-white transition-colors">
                    <span class="material-symbols-outlined text-lg">work</span>
                </a>
            </div>
        </div>
        
        <!-- Quick Links -->
        <div>
            <h6 class="text-navy font-black text-sm uppercase tracking-widest mb-8">Quick Links</h6>
            <ul class="space-y-4">
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Company Overview</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Our Projects</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Certifications</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Service & Maintenance</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Careers</a></li>
            </ul>
        </div>
        
        <!-- Solutions -->
        <div>
            <h6 class="text-navy font-black text-sm uppercase tracking-widest mb-8">HVAC Solutions</h6>
            <ul class="space-y-4">
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">VRF Systems</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Chiller Systems</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Packaged Units</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Air Handling Units</a></li>
                <li><a href="#" class="text-gray-500 text-sm hover:text-primary transition-colors">Building Management</a></li>
            </ul>
        </div>
        
        <!-- Contact -->
        <div>
            <h6 class="text-navy font-black text-sm uppercase tracking-widest mb-8">Contact Info</h6>
            <ul class="space-y-6">
                <li class="flex gap-4">
                    <span class="material-symbols-outlined text-primary">location_on</span>
                    <span class="text-gray-500 text-sm">PO BOX 76058, Samora Avenue,<br>Dar es Salaam, Tanzania</span>
                </li>
                <li class="flex gap-4">
                    <span class="material-symbols-outlined text-primary">call</span>
                    <span class="text-gray-500 text-sm">+255 2137773 / 2133297</span>
                </li>
                <li class="flex gap-4">
                    <span class="material-symbols-outlined text-primary">print</span>
                    <span class="text-gray-500 text-sm">+255 22 2137774</span>
                </li>
                <li class="flex gap-4">
                    <span class="material-symbols-outlined text-primary">mail</span>
                    <span class="text-gray-500 text-sm">remco@cats-net.co.tz</span>
                </li>
            </ul>
        </div>
    </div>
    
    <!-- Footer Bottom -->
    <div class="max-w-7xl mx-auto pt-10 border-t border-gray-100 flex flex-col md:flex-row justify-between items-center gap-6">
        <p class="text-gray-400 text-xs uppercase tracking-widest font-bold">© 2024 REMCO (International) Ltd. All Rights Reserved.</p>
        <div class="flex gap-8">
            <a href="#" class="text-gray-400 text-xs uppercase tracking-widest font-bold hover:text-navy">Privacy Policy</a>
            <a href="#" class="text-gray-400 text-xs uppercase tracking-widest font-bold hover:text-navy">Terms of Service</a>
        </div>
    </div>
</footer>
```
