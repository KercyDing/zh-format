# zh-format

[![English](https://img.shields.io/badge/lang-English-blue.svg)](README.md) [![中文](https://img.shields.io/badge/lang-中文-red.svg)](README_ZH.md) [![Typst Universe](https://img.shields.io/badge/Typst-Universe-239DAD.svg)](https://typst.app/universe/package/zh-format)

zh-format is a Chinese formatting package for Typst, providing better solutions for bold, italic, and underline styles tailored for Chinese typography.

## Usage

```typst
// Import from Typst Universe (recommended)
// #import "@preview/zh-kit:0.1.0": *

// For local development or direct repository usage
#import "../lib.typ": * // assuming lib.typ is in parent directory

#show: zh-format

This is *bold*, _italic_, and #underline[underline] text.

This is #u(width: 8em, offset: 0.4em)[custom underline]
```

### Main Features

#### 1. Bold
- Chinese text uses stroke method (`stroke: 0.02857em`)
- English text uses native font weight
- Automatically distinguishes and handles Chinese and English text separately

#### 2. Italic
- Chinese text uses `skew(ax: -18deg)` transformation
- English text uses native `style: "italic"`
- Intelligently handles mixed Chinese-English text

#### 3. Underline
- Basic underline: `#underline[text]`
- Custom width underline: `#u(width: 8em)[text]`

### Complete Example

See `example/example.typ` for detailed usage examples.

## Changelog

### 0.1.0
- Initial release
- Implemented basic bold, italic, and underline features
- Support for intelligent Chinese-English mixed text recognition
- Added custom width underline function `#u()`

## License

[MIT License](LICENSE)
