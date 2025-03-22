# ViolateLibertyShame

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

**ViolateLibertyShame** is a project dedicated to documenting and exposing apps that detect root, bootloader unlocking, jailbreaking, and other freedom-enabling actions on devices. We aim to create a public record of these detection methods and provide solutions to bypass them.

## Project Goals

- Document detection methods used by apps to identify root, bootloader unlocking, jailbreaking, etc.
- Provide solutions to bypass these detections.
- Serve as a reference for developers, researchers, and users.

## Data Structure

Each app's record is stored in JSON format with the following fields:

- `format_version`: json format version.
- `app_name`: Name of the app.
- `platform`: Platform (Android/iOS).
- `package_name`: Package name for Android apps (leave empty for the platforms which can not get a package name).
- `detection_methods`: List of detection methods, including:
  - `version_ranges`: Version ranges where the detection behavior applies.
  - `method_name`: Name of the detection method.
  - `description`: Description of the detection method.
  - `implementations`: How the detection is implemented (e.g., code logic or system calls).
  - `solutions`: Solutions to bypass the detection.
- `additional_notes`: Additional relevant information.
- `last_updated`: Date of the last update.

## How to Contribute

We welcome contributions from anyone! Here’s how you can help:

1. **Fork this repository**.
2. Create a new JSON file in the `data/` directory or edit an existing one.
3. Fill in or update the information according to the data structure.
4. Submit a Pull Request and describe your changes.

### Contribution Example

To add a record for an app called `ExampleApp`:

1. Create a file named `example_app.json` in the `data/` directory.
2. Add the following content:
   ```json
   {
     "format_version": "0",
     "app_name": "ExampleApp",
     "platform": "Android",
     "package_name": "com.example.app",
     "detection_methods": [
       {
         "version_ranges": ["1.0.0 - 2.3.0", "2.5.0"],
         "method_name": "Root Check",
         "description": "Checks if the device is rooted",
         "implementation": ["Checks for the existence of /system/bin/su"],
         "solutions": ["Use Magisk Hide to hide root"]
       }
     ],
     "additional_notes": "This app added SafetyNet detection in version 2.3.0",
     "last_updated": "2025-02-18"
   }
   ```
3. Submit a Pull Request.

## Project Roadmap

- [ ] Add more app detection records.
- [ ] Develop automated tools to deal with app detection behaviors.
- [x] Provide a web interface for easy browsing and searching.

## License

This project is licensed under the [MIT License](LICENSE).

---

**Join us in exposing these detection methods and defending user freedom!**
