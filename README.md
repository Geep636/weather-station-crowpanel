# Weather Station CrowPanel

Custom firmware for the [Elecrow CrowPanel ESP32-S3 5.79" E-Paper HMI Display](https://www.elecrow.com/crowpanel-esp32-5-79-e-paper-hmi-display-with-272-792-resolution-black-white-color-driven-by-spi-interface.html), optimized for always-on home weather monitoring.

This project is an independent implementation derived from the excellent [weather-crow5.7](https://github.com/kotamorishi/weather-crow5.7) project by kotamorishi.

## Key Features (Phase 1 Planning)
- **High-Resolution Data**: Switching to Open-Meteo API for 1-hour forecast resolution.
- **Custom Layouts**:
  - **Landscape (Bedroom)**: Large clock + 8-hour dynamic temperature curve with precipitation intensity shading.
  - **Portrait (Bathroom)**: 7-day forecast stack + on-demand tabular hourly timeline.
- **Variable Refresh**: Smart partial refresh intervals to balance glanceability with hardware longevity.

## Getting Started

### Prerequisites
- **PlatformIO**: Recommended for building and flashing.
- **GitHub account**: To track your own customizations.

### Installation
1. **Clone this repository** (your own fork/copy).
2. **Setup Credentials**:
   - Copy `src/config.example.h` to `src/config.h`.
   - **IMPORTANT**: `src/config.h` is git-ignored and contains your real WiFi credentials. Never commit this file.
   - Enter your WiFi SSID and Password.
3. **Build and Flash**:
   ```bash
   pio run --target upload
   ```

## Project Structure
- `firmware/`: The PlatformIO project root (this folder).
- `docs/`: Reference documentation and layout specs.
- `wiki/`: Internal project tracking and decision logs.

## Credits & License

### Base Firmware
- Original project: [weather-crow5.7](https://github.com/kotamorishi/weather-crow5.7) by [kotamorishi](https://github.com/kotamorishi).
- License: MIT (inherited from base project).

### Data & Assets
- **Weather Data**: [Open-Meteo](https://open-meteo.com/) (planned) / [OpenWeatherMap](https://openweathermap.org/) (baseline).
- **Icons**: [Weather Icons](https://erikflowers.github.io/weather-icons/) (SIL OFL 1.1).
- **Fonts**: 
  - [Poppins](https://fonts.google.com/specimen/Poppins) (SIL OFL 1.1).
  - 04b-03 by YUJI OSHIMOTO.
