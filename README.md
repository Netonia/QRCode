# QR Code Generator

A lightweight, client-side QR code generator built with **Blazor WebAssembly** and **.NET 9**.

## Features

✨ **Core Features:**
- Generate QR codes from text or URLs instantly
- Download QR codes as PNG images
- Fully client-side - no data sent to server
- Works offline after initial load
- Responsive design for mobile and desktop
- Clean and intuitive user interface

## Technology Stack

- **Framework:** .NET 9 / Blazor WebAssembly
- **Language:** C#
- **QR Library:** [QRCoder](https://github.com/codebude/QRCoder)
- **UI Framework:** Bootstrap 5
- **State Management:** Local component state

## Getting Started

### Prerequisites

- [.NET 9 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)

### Running Locally

1. Clone the repository:
```bash
git clone https://github.com/Netonia/QRCode.git
cd QRCode/QRCodeGenerator
```

2. Run the application:
```bash
dotnet run
```

3. Open your browser and navigate to `http://localhost:5152`

### Building for Production

```bash
dotnet publish -c Release
```

The output will be in `bin/Release/net9.0/publish/wwwroot/`

## Deployment

This application can be deployed to:
- GitHub Pages
- Azure Static Web Apps
- Netlify
- Vercel
- Any static web hosting service

## Usage

1. Enter text or URL in the input field
2. Click **Generate QR Code**
3. The QR code will be displayed instantly
4. Click **Download QR Code** to save as PNG

## Screenshots

### Desktop View
![Desktop View](https://github.com/user-attachments/assets/8daa1433-7801-456c-8a73-6c93aa3e4fd1)

### Mobile View
![Mobile View](https://github.com/user-attachments/assets/43fcb547-354e-4330-850a-f4246ef4bce6)

## Project Structure

```
QRCodeGenerator/
├── Pages/
│   └── Home.razor          # Main QR code generator component
├── Layout/
│   ├── MainLayout.razor    # App layout
│   └── NavMenu.razor       # Navigation menu
├── wwwroot/
│   ├── index.html          # Main HTML page
│   └── css/                # Stylesheets
├── Program.cs              # Application entry point
└── QRCodeGenerator.csproj  # Project file
```

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.