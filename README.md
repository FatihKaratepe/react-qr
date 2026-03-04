# @mfk/react-qr

A customizable and easy-to-use React component for generating QR codes with support for SVG, Canvas, and optional embedded images.

## Features

- Renders as SVG or Canvas.
- Customizable colors, size, and error correction levels.
- Support for embedded logo/images inside the QR code.
- Fully typed using TypeScript.
- Based on the reliable qrcodegen library.

## Installation

```bash
npm install @mfk/react-qr
# or
yarn add @mfk/react-qr
# or
pnpm add @mfk/react-qr
# or
bun add @mfk/react-qr
```

## Usage

```tsx
import { QRCodeSVG, QRCodeCanvas } from "@mfk/react-qr";

function App() {
  return (
    <div>
      {/* Rendering as SVG with an embedded logo */}
      <QRCodeSVG
        value="https://example.com"
        size={256}
        bgColor="#ffffff"
        fgColor="#000000"
        level="Q"
        imageSettings={{
          src: "path/to/logo.png",
          height: 24,
          width: 24,
          excavate: true,
        }}
      />

      {/* Rendering as Canvas */}
      <QRCodeCanvas value="https://example.com" size={128} />
    </div>
  );
}

export default App;
```

---

# @mfk/react-qr (Türkçe)

SVG, Canvas ve isteğe bağlı gömülü görsel (logo) desteği ile QR kodları oluşturmak için özelleştirilebilir ve kullanımı kolay bir React bileşeni.

## Özellikler

- SVG veya Canvas olarak render edebilme imkanı.
- Özelleştirilebilir renk, boyut ve hata düzeltme seviyeleri (error correction level).
- QR kodunun içine logo veya görsel ekleme desteği.
- TypeScript ile tam tip desteği (fully typed).
- Kararlı qrcodegen kütüphanesini temel alır.

## Kurulum

```bash
npm install @mfk/react-qr
# veya
yarn add @mfk/react-qr
# veya
pnpm add @mfk/react-qr
# veya
bun add @mfk/react-qr
```

## Kullanım

```tsx
import { QRCodeSVG, QRCodeCanvas } from "@mfk/react-qr";

function App() {
  return (
    <div>
      {/* Logonun içine eklendiği bir SVG örneği */}
      <QRCodeSVG
        value="https://example.com"
        size={256}
        bgColor="#ffffff"
        fgColor="#000000"
        level="Q"
        imageSettings={{
          src: "path/to/logo.png",
          height: 24,
          width: 24,
          excavate: true, // Logonun arkasındaki QR desenini silerek okunabilirliği artırır
        }}
      />

      {/* Basit bir Canvas örneği */}
      <QRCodeCanvas value="https://example.com" size={128} />
    </div>
  );
}

export default App;
```
