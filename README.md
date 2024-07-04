<p align="center">
<img src="https://github.com/coliff/bootstrap-forced-colors-css/blob/main/.github/preview.png?raw=true" width="500" alt="Bootstrap 5 Forced Colors CSS">
</p>

<h3 align="center">Bootstrap Forced Colors CSS</h3>

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/coliff/bootstrap-forced-colors-css/main/LICENSE)
[![GitHub stars image](https://img.shields.io/github/stars/coliff/bootstrap-forced-colors-css.svg?label=GitHub%20Stars)](https://github.com/coliff/bootstrap-forced-colors-css)
[![npm Version](https://img.shields.io/npm/v/bootstrap-forced-colors-css)](https://www.npmjs.com/package/bootstrap-forced-colors-css)
[![jsdelivr](https://data.jsdelivr.com/v1/package/npm/bootstrap-forced-colors-css/badge)](https://www.jsdelivr.com/package/npm/bootstrap-forced-colors-css)

Enhances the accessibility of Bootstrap 5 when using with [Hight Contrast themes in Windows](https://blogs.windows.com/msedgedev/2020/09/17/styling-for-windows-high-contrast-with-new-standards-for-forced-colors/).

This CSS file fixes many issues and adds enhancements to make Bootstrap 5 more accessible in Firefox, Chrome, Edge on Windows using the [`forced-colors: active` media query](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/forced-colors).

## Quick start

- Download the [latest release](https://github.com/coliff/bootstrap-forced-colors-css/releases/latest)
- Clone the repository `git clone https://github.com/coliff/bootstrap-forced-colors-css.git`
- Install with [npm](https://www.npmjs.com/package/bootstrap-forced-colors-css) `npm install bootstrap-forced-colors-css`
- Install with [yarn](https://classic.yarnpkg.com/en/package/bootstrap-forced-colors-css) `yarn add bootstrap-forced-colors-css`
- Install with [Composer](https://packagist.org/packages/coliff/bootstrap-forced-colors-css) `composer require coliff/bootstrap-forced-colors-css`

## Usage

Add this in the `<head>` which will load the CSS using a media query as follow:

```html
<link rel="stylesheet" href="/css/bootstrap-forced-colors.min.css" media="screen and (forced-colors: active)">
```

The CSS can be loaded via a CDN:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-forced-colors-css@1.0.4/css/bootstrap-forced-colors.min.css" media="screen and (forced-colors: active)">
```

Or you can import the CSS into your own CSS file:

```scss
@import bootstrap-forced-colors.min.css
```

> [!NOTE]
> bootstrap-forced-colors-css improves the accessibility of Bootstrap 5 for Windows users in forced colors mode, but you should still test your site to ensure it meets your accessibility requirements.

## FAQS

### What does this fix/improve?

- [Accordion](https://coliff.github.io/bootstrap-forced-colors-css/tests/#accordion) buttons have improved contrast in dark mode
- [Badges](https://coliff.github.io/bootstrap-forced-colors-css/tests/#badge) within buttons have a 1px border to improve contrast
- [Buttons](https://coliff.github.io/bootstrap-forced-colors-css/tests/#buttons) have improved focus state contrast (2px visible outline rather than 1px)
- [Disabled buttons](https://coliff.github.io/bootstrap-forced-colors-css/tests/#buttons) display the correct color using the `GrayText` name
- [Carousel](https://coliff.github.io/bootstrap-forced-colors-css/tests/#carousel) indicators have background-color issue resolved
- [Close button](https://coliff.github.io/bootstrap-forced-colors-css/tests/#toasts) has improved contrast by reducing the opacity
- [Dropdown](https://coliff.github.io/bootstrap-forced-colors-css/tests/#dropdowns) toggle arrows appear correctly (as triangles and not rectangles)
- [List Group](https://coliff.github.io/bootstrap-forced-colors-css/tests/#list-group) disabled items display the correct color using the `GrayText` name
- [Modal](https://coliff.github.io/bootstrap-forced-colors-css/tests/#modal) backdrop opacity changed from 0.5 to 0.8
- [Navbar](https://coliff.github.io/bootstrap-forced-colors-css/tests/#navbar) Menu (hamburger) toggle icons display correctly
- [Pagination](https://coliff.github.io/bootstrap-forced-colors-css/tests/#pagination): Active page link has outline to indicate active page
- [Pagination](https://coliff.github.io/bootstrap-forced-colors-css/tests/#pagination): Disabled page link display the correct color using the `GrayText` name
- [Placeholder](https://coliff.github.io/bootstrap-forced-colors-css/tests/#placeholder): Fix for invisible placeholder boxes
- [Popovers](https://coliff.github.io/bootstrap-forced-colors-css/tests/#popovers): Fixed invisible arrow issue
- [Progress](https://coliff.github.io/bootstrap-forced-colors-css/tests/#progress): Is no longer invisible
- [Spinners](https://coliff.github.io/bootstrap-forced-colors-css/tests/#spinners): Fixed animation
- [Tables](https://coliff.github.io/bootstrap-forced-colors-css/tests/#tables): Have a 1px outline to improve contrast
- [Toasts](https://coliff.github.io/bootstrap-forced-colors-css/tests/#toasts): Fixed invisible close/dismiss button
- [Tooltips](https://coliff.github.io/bootstrap-forced-colors-css/tests/#tooltips): Fix for arrows appearing as rectangles
- [Tooltips](https://coliff.github.io/bootstrap-forced-colors-css/tests/#tooltips): Add 1px border to tooltips content

### Known Issues

- Check the [open issues at GitHub](https://github.com/coliff/bootstrap-forced-colors-css/issues).

## Demo

See this in action at: [https://coliff.github.io/bootstrap-forced-colors-css/tests/](https://coliff.github.io/bootstrap-forced-colors-css/tests/)

## Testing

Currently, only Windows 10 & 11 with Edge, Firefox, and Chrome support forced colors mode. To test, you can enable forced colors mode in:

- Windows 10: Go to `Settings > Ease of Access > High contrast` and select a theme.
- Windows 11: Go to `Settings > Accessibility > Contrast themes` and select a theme.

You can also use the [Forced Colors Mode Emulation](https://developer.chrome.com/docs/devtools/rendering/emulate-css#emulate_css_media_feature_forced-colors) in Edge and Chrome on all platforms.

> [!NOTE]
> By default, the Forced Colors Mode emulation is a dark mode theme, but you can switch to a light theme by forcing the `prefers-color-scheme` to light in the Dev Tools. Remember that the user can't use Bootstrap's light/dark mode theme toggle. The color scheme is set by the user at the OS level.

Note that [CanIUse lists Safari as supporting forced colors mode](https://caniuse.com/mdn-css_at-rules_media_forced-colors), however macOS itself doesn't have a Forced Colors / High Contrast mode which means it's not possible to use this with Safari at all.
