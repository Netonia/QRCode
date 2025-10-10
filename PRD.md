# QR Code Generator - Blazor WebAssembly

## 1. Overview
The **QR Code Generator** is a lightweight, client-side web application built with **Blazor WebAssembly**.  
It allows users to quickly generate and download QR codes based on user-provided input such as text, URLs, or contact data.

The app is designed for speed, simplicity, and portability — with no server dependency.

---

## 2. Objectives
- Provide a fast, intuitive interface for generating QR codes.
- Run entirely in the browser (no backend).
- Allow users to customize and download generated QR codes.
- Demonstrate Blazor WASM capabilities with clean component design.

---

## 3. Target Users
- **General users** who need QR codes for links or text.
- **Small businesses** creating QR codes for products or promotions.
- **Developers/designers** integrating QR codes into projects or demos.

---

## 4. Core Features
| Feature | Description |
|----------|--------------|
| **Input Field** | Users can enter text, URL, or other data. |
| **Generate Button** | Generates a QR code instantly using a C# QR library. |
| **QR Display** | Displays the generated QR code dynamically in the UI. |
| **Download Option** | Download QR code as a PNG image. |
| **Responsive Layout** | Optimized for mobile and desktop. |

---

## 5. Optional / Future Features
| Feature | Description |
|----------|--------------|
| **Custom Size** | Adjust QR code dimensions (e.g., 150px–500px). |
| **Color Options** | Choose foreground and background colors. |
| **Data Type Presets** | Templates for URLs, emails, phone numbers, vCards, Wi-Fi networks. |
| **History** | Save generated codes in browser local storage. |
| **Dark Mode** | Toggle theme for better accessibility. |

---

## 6. Technical Specifications
- **Framework:** [.NET 9 / Blazor WebAssembly](https://learn.microsoft.com/en-us/aspnet/core/blazor)
- **Language:** C#
- **QR Library:** [QRCoder](https://github.com/codebude/QRCoder)
- **UI Framework:** TailwindCSS or Bootstrap
- **State Management:** Local component state (no global store needed)
- **Hosting Options:** GitHub Pages, Azure Static Web Apps, Netlify, or Vercel

---

## 7. User Flow
1. User opens the web app in the browser.  
2. Enters text or URL into the input field.  
3. Clicks **Generate QR Code**.  
4. The app renders the QR code in real time.  
5. The user clicks **Download** to save the image locally.  

Optional:
- Customize QR code color or size.
- View or re-generate previously created codes.

---

## 8. Non-Functional Requirements
- **Performance:** QR code generation < 2 seconds.
- **Availability:** 99% uptime when hosted statically.
- **Security:** No data stored or transmitted externally.
- **Usability:** Mobile-first responsive UI.
- **Accessibility:** Keyboard and screen-reader friendly.

---

## 9. Success Metrics
- App loads and generates a QR code within 3 seconds.
- At least 95% of users can download a QR code without errors.
- Zero backend or API dependencies.
- Lighthouse performance score > 90.
