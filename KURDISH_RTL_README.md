# Kurdish RTL Support for Hugoplate

This document describes the Kurdish (RTL) language implementation for the Hugoplate Hugo theme.

## Features Implemented

### 1. Language Configuration
- Added Kurdish (`ku`) language configuration in `config/_default/languages.toml`
- Kurdish content directory: `content/kurdish/`
- Language code: `ku`
- Language name: `کوردی`

### 2. RTL CSS Support
- Created `themes/hugoplate/assets/css/rtl.css` with comprehensive RTL styles
- Includes RTL support for:
  - Typography and text direction
  - Navigation menus
  - Forms and input fields
  - Buttons and button groups
  - Cards and containers
  - Lists and blockquotes
  - Tables and pagination
  - Alerts and modals
  - Dropdowns and tooltips
  - Utility classes (margins, padding, positioning)

### 3. HTML Structure Updates
- Updated `themes/hugoplate/layouts/_default/baseof.html` to include `dir` attribute
- Automatically sets `dir="rtl"` for Kurdish pages and `dir="ltr"` for English

### 4. Font Support
- Added Google Fonts support for Noto Sans Kurdish
- Font is loaded only for Kurdish language pages
- Fallback fonts: Segoe UI, Tahoma, Geneva, Verdana, sans-serif

### 5. Translation Files
- Created `i18n/ku.yaml` with Kurdish translations for common UI elements
- Created `config/_default/menus.ku.toml` with Kurdish menu items

### 6. Sample Content
- Homepage: `content/kurdish/_index.md`
- About page: `content/kurdish/about/_index.md`
- Blog: `content/kurdish/blog/_index.md` and sample post
- Contact page: `content/kurdish/contact/_index.md`
- Authors: `content/kurdish/authors/_index.md` and sample author
- Elements page: `content/kurdish/pages/elements.md`
- Privacy policy: `content/kurdish/pages/privacy-policy.md`

## How to Use

### Switching Languages
1. The language switcher is automatically available in the header
2. Users can switch between English and Kurdish
3. URLs will include language prefix (e.g., `/ku/` for Kurdish)

### Adding Content
1. Create content in `content/kurdish/` directory
2. Use the same structure as English content
3. Write content in Kurdish using proper RTL formatting

### Customizing RTL Styles
1. Edit `themes/hugoplate/assets/css/rtl.css` for custom RTL styles
2. The RTL styles are automatically applied when `dir="rtl"` is set

### Adding More Translations
1. Add new translations to `i18n/ku.yaml`
2. Update menu items in `config/_default/menus.ku.toml`
3. Add language-specific parameters in `config/_default/params.toml`

## Technical Details

### RTL Implementation
- Uses CSS `direction: rtl` property
- Comprehensive utility class overrides for RTL
- Proper handling of margins, padding, and positioning
- Support for Bootstrap-style components

### Font Loading
- Google Fonts Noto Sans Kurdish is loaded conditionally
- Font weights: 300, 400, 500, 600, 700
- Optimized for Kurdish script rendering

### Content Structure
- Follows Hugo's multilingual content structure
- Maintains same layout templates as English
- Proper front matter for Kurdish content

## Browser Support
- Modern browsers with RTL support
- CSS Grid and Flexbox for layout
- Google Fonts for typography

## Notes
- The implementation maintains compatibility with the existing English content
- RTL styles are only applied when Kurdish language is active
- All existing theme features work with both languages
- Search functionality supports both languages

## Future Enhancements
- Add more Kurdish fonts
- Implement Kurdish-specific date formatting
- Add Kurdish number formatting
- Enhance RTL support for complex layouts 