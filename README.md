# Documentation for `BrootHub` Theme

**Be root Hub** - intended meaning behind the name BrootHub

The **BrootHub** theme is a custom Hugo theme for building static websites.  
It is currently under development and subject to change.  

⚠️ Please review the **[LICENSE](./LICENSE)** or **[LICENSE.md](./LICENSE.md)** file before using this theme.  
Use is restricted to **private, non-commercial purposes** unless explicitly permitted by the copyright holder.

Original Repository: https://github.com/Hin7zer/BrootHub
Owner: https://github.com/Hin7zer/BrootHub 

---

## 1. Getting Started with Hugo

Before using the theme, make sure you have installed [Hugo](https://gohugo.io/getting-started/installing/).  
Once installed, you can create a new site and apply the theme.

Example for creating a new site:

```bash
hugo new site mysite
cd mysite
git init
git clone https://github.com/Hin7zer/BrootHub.git themes/BrootHub
```

## 2. Configuring the Theme

Configuration is handled through your Hugo config file (```config.yml```,```config.toml```.```hugo.toml```).
An example can be found in the demo page under ```exampleSite/config.toml```aswell as demo pages.

## 3. Theme Shortcodes 

This theme provides a set of shortcodes to include standardized legal and contact information in your site. They are designed to work for companies, clubs, and private users, and can adapt to multiple languages. Currently only German is supported.

1. How Shortcodes Work

Legal and contact info are stored in params.Legal in your config.yaml.
This includes address lines, phone, email, website, entity type, entity details, and optional bank details.

Shortcodes read these parameters dynamically: Only fields that have content are rendered. Empty fields are automatically skipped.
This ensures your site always shows relevant legal info without manual editing.

Usage in content files:
Include a shortcode for a specific language like this:

```
---
title: "Contact"
---
{{< de/kontakt >}} 
{{< en/contact >}}
```

Shotcodes can be combined. Ther are already some shortcodes defined for some usecases to reduce the effort for users. Feel free to extend it. If shortcodes do not match your usecase define your own or create custom pages.

Shortcodes are stored in ```layouts/shortcodes/``` for multiple countries it is separated in directories to make everything easier.

There is also a default Home layout available for the ```_index.md``` file. For Home articles or Blog posts you can use templates to show them in your home page. shotcodes for the home are named with home in the shortcodes directory. They to not relate to specific languages.

2. Benefits

Shortcodes can be seen as templates. They contain html code and formatations to be used. This can be used simply in the content pages itself. be careful and check them before using them in productive environments.



## 4. Customizing the Color Layout

The color layout of the theme is defined in: ```./static/css/00-vars.css```


This file defines CSS variables for the theme’s color scheme.
You may override these values with your own, but always review your custom file before upgrading to a new version.
Otherwise, some elements may become invisible or hard to read.

Example:

```css
/* CSS Variables */
:root {
    --primary-color: #ff7332;
    --secondary-color: #d95e27;
    --accent-color: #27d927;
    --background-color: #ffffff;
    --background-accent-color: #e6e6e6;
    --dark-background-color: #1a1a1a;
    --dark-background-accent-color: #272727;
    --text-color: #000000;
    --link-color: #ff8c42;
    --link-hover-color: #ff8c42;
    --dark-text-color: #ffffff;
    --submenu-background-color: #dbdbdb;
    --submenu-hover-color: #777777;
    --dark-submenu-background-color: #393939;
    --dark-submenu-hover-color: #777777;
    --button-background-color: #5c5c5c;
    --button-default-color: #ffffff;
    --button-hover-color: #670000;
}
```


## 5. Running Hugo with the Theme

Useful Hugo commands:

```bash
# Run a local development server with drafts enabled
hugo server -D --cleanDestinationDir

# Build the site to a custom directory (e.g., "../../public")
hugo --destination "../../public" --cleanDestinationDir

# Build with minification enabled
hugo --minify --destination "../../public" --cleanDestinationDir
```

For further information, see the official Hugo documentation

## 6. License

This theme is distributed under a Proprietary License.

Allowed: private, non-commercial use.

Not allowed: commercial use, redistribution, or modification for profit.

For full details, see the LICENSE

### Notes

This project was built from scratch by human, with selective use of AI for improvements, fixes, and optimizations.
AI was used as a tool — not as a replacement for design, architecture, or creative decisions.

## Author

This theme was originally created by **Benjamin Hinz**.

Original source:  
https://github.com/Hin7zer/BrootHub

Author profile:  
https://github.com/Hin7zer

### Attribution Requirement

If you build upon this project, please give proper credit by linking back to the original repository and naming the original author.
