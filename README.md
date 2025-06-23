# Corsair H150 RGB Pump Cap - SignalRGB Custom Component

A custom SignalRGB component for Corsair H50/H100/H150 RGB AIO coolers pump cap LED control, featuring precise 13-LED mapping for seamless RGB synchronization.

<video src="https://github.com/jluizpjr/SignalRGB/blob/2194217fd8b75dec435320a7b9d0094cbc570464/SRGB-H150RGB.mp4"></video>

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Compatibility](#compatibility)
- [Installation](#installation)
- [Technical Specifications](#technical-specifications)
- [LED Layout](#led-layout)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## Overview

This custom component enables SignalRGB to properly recognize and control the RGB lighting on Corsair's H50, H100, and H150 RGB AIO cooler pump caps. The component provides accurate LED mapping for the 13 individual LEDs arranged in both inner and outer rings on the pump cap.

### Why This Component?

- Accurate LED Mapping: Precisely mapped 13 LEDs with correct positioning
- Complete Control: Full RGB customization through SignalRGB
- Ring-Based Layout: Supports both inner (5 LEDs) and outer (8 LEDs) ring configurations
- Universal Compatibility: Works across H50, H100, and H150 RGB models
- Seamless Integration: Plug-and-play installation with SignalRGB

## Features

- Dual Ring Architecture: Inner ring (5 LEDs) + Outer ring (8 LEDs)
- Precise Coordinate Mapping: 21x21 grid coordinate system for accurate positioning
- Named LED References: Each LED has a descriptive name for easy identification
- SignalRGB Integration: Full compatibility with SignalRGB's effect engine
- AIO Type Classification: Properly categorized as AIO device type

## Compatibility

### Supported Hardware
- Corsair H50 RGB - 120mm AIO Liquid Cooler
- Corsair H100 RGB - 240mm AIO Liquid Cooler  
- Corsair H150 RGB - 360mm AIO Liquid Cooler

### Software Requirements
- SignalRGB - Latest version recommended
- Windows 10/11 - Required for SignalRGB compatibility
- Administrative Privileges - Required for hardware access

### Hardware Requirements
- Compatible motherboard with USB headers
- Adequate USB bandwidth for RGB data transmission

## Installation

### Method 1: Manual Installation

1. Download the Component
   Download the CorsairH150RGBPumpCap.json file from this repository

2. Locate SignalRGB Components Folder
   Navigate to: %USERPROFILE%\Documents\WhirlwindFX\SignalRGB\Components\

3. Install the Component
   Copy "CorsairH150RGBPumpCap - 13 LED.json" to the Components folder

4. Restart SignalRGB
   Close and restart SignalRGB application

5. Verify Installation
   Check if "CorsairH150RGBPumpCap - 13 LED" appears in device list

### Method 2: SignalRGB Import

1. Open SignalRGB application
2. Navigate to Settings → Components
3. Click Import Component
4. Select the downloaded CorsairH150RGBPumpCap.json file
5. Restart SignalRGB

## Technical Specifications

| Property | Value |
|----------|-------|
| Product Name | CorsairH150RGBPumpCap |
| Display Name | CorsairH150RGBPumpCap - 13 LED |
| Brand | Corsair |
| Device Type | AIO (All-In-One Cooler) |
| LED Count | 13 LEDs |
| Coordinate Space | 21 x 21 grid |
| Ring Configuration | Inner (5) + Outer (8) |

### LED Configuration

The component uses the following LED configuration:
- LedCount: 13
- Width: 21
- Height: 21
- LedMapping: [0,1,2,3,4,5,6,7,8,9,10,11,12]

## LED Layout

![alt text]([layout.png](https://github.com/jluizpjr/SignalRGB/blob/2194217fd8b75dec435320a7b9d0094cbc570464/layout.png)?raw=true)

The pump cap features a dual-ring LED arrangement:

### Inner Ring (LEDs 0-4)
- LED 0: Inner Left [7, 10]
- LED 1: Inner Top [8, 6]
- LED 2: Inner Top Right [12, 7]
- LED 3: Inner Bottom Right [13, 11]
- LED 4: Inner Bottom [9, 13]

### Outer Ring (LEDs 5-12)
- LED 5: Outer Bottom Left [7, 20]
- LED 6: Outer Left Low [0, 12]
- LED 7: Outer Left High [0, 7]
- LED 8: Outer Top Left [7, 0]
- LED 9: Outer Top Right [12, 0]
- LED 10: Outer Right High [20, 7]
- LED 11: Outer Right Low [20, 12]
- LED 12: Outer Bottom Right [12, 20]

### Visual Layout Description

The LEDs are arranged in two concentric rings:

OUTER RING (8 LEDs):
- Top section: LED 8 (Top Left), LED 9 (Top Right)
- Right section: LED 10 (Right High), LED 11 (Right Low)
- Bottom section: LED 12 (Bottom Right), LED 5 (Bottom Left)
- Left section: LED 6 (Left Low), LED 7 (Left High)

INNER RING (5 LEDs):
- Top section: LED 1 (Top), LED 2 (Top Right)
- Bottom section: LED 3 (Bottom Right), LED 4 (Bottom)
- Left section: LED 0 (Left)

## Usage

### Basic Setup

1. Connect Your AIO
   - Ensure your Corsair H50/H100/H150 RGB is properly connected
   - Connect USB cable to motherboard header

2. Launch SignalRGB
   - Open SignalRGB application
   - Allow hardware scanning

3. Select Device
   - Look for "CorsairH150RGBPumpCap - 13 LED" in device list
   - Select the device

4. Apply Effects
   - Choose from available RGB effects
   - Customize colors and patterns
   - Apply settings

### Advanced Configuration

#### Custom Effects
- Use LED names for targeted effects
- Create ring-specific animations
- Combine with other RGB devices for synchronized lighting

#### Effect Examples
- Breathing: Smooth fade in/out across all LEDs
- Rainbow Wave: Color wave rotating around rings
- Temperature Display: Color coding based on CPU temperature
- Ring Chase: Sequential LED activation in rings

## Troubleshooting

### Device Not Detected

Problem: SignalRGB doesn't recognize the pump cap

Solutions:
1. Verify USB connection to motherboard
2. Check Windows Device Manager for USB devices
3. Restart SignalRGB with administrator privileges
4. Re-install the component file

### LEDs Not Responding

Problem: LEDs don't change color or remain off

Solutions:
1. Check power connections to AIO pump
2. Verify iCUE software is closed (conflicts with SignalRGB)
3. Update SignalRGB to latest version
4. Reset device in SignalRGB settings

### Incorrect LED Mapping

Problem: LEDs light up in wrong positions

Solutions:
1. Verify component file integrity
2. Check for duplicate component files
3. Clear SignalRGB cache and restart
4. Reinstall component

### Performance Issues

Problem: Slow response or flickering

Solutions:
1. Reduce effect update frequency
2. Close unnecessary RGB software
3. Check USB bandwidth usage
4. Update motherboard USB drivers

## Contributing

We welcome contributions to improve this component!

### How to Contribute

1. Fork this repository
2. Create a feature branch (git checkout -b feature/improvement)
3. Commit your changes (git commit -am 'Add new feature')
4. Push to branch (git push origin feature/improvement)
5. Create a Pull Request

### Areas for Contribution

- LED Mapping Improvements: More accurate positioning
- Additional Models: Support for other Corsair AIO variants
- Documentation: Enhanced installation guides
- Testing: Compatibility verification across systems

### Reporting Issues

Please report issues with:
- Hardware specifications
- SignalRGB version
- Detailed problem description
- Steps to reproduce

## License

This project is licensed under the MIT License - see the LICENSE file for details.

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software.

## Support

### Getting Help

- GitHub Issues: Create an issue for bugs or questions
- SignalRGB Discord: Join the official SignalRGB community
- Documentation: Check SignalRGB official documentation

### Useful Links

- SignalRGB Official Website: https://signalrgb.com/
- Corsair Support: https://help.corsair.com/
- Component Development Guide: https://docs.signalrgb.com/

---

If this component helped you, please consider giving it a star!

Made with love for the RGB community

---

Disclaimer: This is an unofficial component. Corsair and SignalRGB are trademarks of their respective owners.
