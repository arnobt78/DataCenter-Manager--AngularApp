# DataCenter-Manager (Official Commercial Mobile App)

![Screenshot 2024-08-25 at 05 56 42](https://github.com/user-attachments/assets/c4651899-7e59-4d42-93c8-a98011e2b8e6)

![Screenshot 2024-08-25 at 05 57 02](https://github.com/user-attachments/assets/a8ef6255-e423-4b8e-8471-24e4c38f8500)

![Screenshot 2024-08-25 at 05 57 52](https://github.com/user-attachments/assets/e098df5c-915e-4bfd-b46f-a36ee29a3e3a)     ![Screenshot 2024-08-25 at 05 58 10](https://github.com/user-attachments/assets/...)

![Screenshot 2024-08-25 at 05 58 25](https://github.com/user-attachments/assets/a21e1ea7-4f07-48f0-a9cf-484ccca025d7)     ![Screenshot 2024-08-25 at 05 58 43](https://github.com/user-attachments/assets/...)

---

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technical Stack](#technical-stack)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Project Structure](#project-structure)
- [Development & Build](#development--build)
- [Screenshots](#screenshots)
- [References](#references)
- [License](#license)

---

## Project Overview

**DataCenter-Manager** is a commercial mobile application designed to provide remote access and management capabilities for data centers and servers. With this app, users can create servers, manage storage, take and retrieve HDD snapshots, connect/disconnect to servers or data centers, and power servers on or off, all from a mobile interface.

This project aims to simplify data center management by providing an intuitive, mobile-friendly dashboard for IT administrators and technical users.

You can view the project on the official webpage: [https://gil.gmbh/en/projects/project_02/](https://gil.gmbh/en/projects/project_02/)

---

## Key Features

- **Remote Server Creation:** Instantly create and configure new servers remotely.
- **Storage Management:** Manage hard drive snapshots, retrieve backups, and monitor current storage usage.
- **Server Connectivity:** Connect or disconnect to remote servers or entire data centers.
- **Server Power Controls:** Remotely power on/off servers or data center components.
- **Snapshot Management:** Take, view, and restore HDD snapshots for disaster recovery.
- **User-Friendly Dashboard:** Intuitive UI for monitoring and managing data center resources.
- **Mobile-First Design:** Optimized for mobile devices, leveraging Ionic/Cordova for cross-platform compatibility.

---

## Technical Stack

- **Frontend:** Ionic Framework, AngularJS, TypeScript, HTML, CSS
- **Mobile Integration:** Cordova
- **Data/Communication:** JSON, JavaScript
- **Other:** Swift (for iOS-specific features)

---

## Installation & Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (preferably the latest LTS version)
- [npm](https://www.npmjs.com/) (included with Node.js)
- [Ionic CLI](https://ionicframework.com/docs/cli) (`npm install -g @ionic/cli`)
- [Cordova CLI](https://cordova.apache.org/docs/en/latest/guide/cli/) (`npm install -g cordova`)
- [Git](https://git-scm.com/)

### Clone the Repository

```bash
git clone https://github.com/arnobt78/DataCenter-Manager--AngularApp.git
cd DataCenter-Manager--AngularApp
```

### Install Dependencies

```bash
npm install
```

### Add Platforms

Depending on your target device, add the appropriate platforms:

```bash
ionic cordova platform add android
ionic cordova platform add ios
```

> **Note:** For iOS development, you must use a Mac with Xcode installed.

---

## Usage Guide

### Running the App in a Browser

For development/testing purposes:

```bash
ionic serve
```

### Running on a Device

To run the app on a connected device or emulator:

```bash
ionic cordova run android
ionic cordova run ios
```

### Building for Production

```bash
ionic cordova build android --prod --release
ionic cordova build ios --prod --release
```

---

## Project Structure

- `/src/` - Main application source code
    - `/app/` - Angular modules, components, services
    - `/assets/` - Static assets such as images, icons, etc.
    - `/environments/` - Environment-specific configuration
- `/hooks/` - Cordova hooks/scripts
- `/resources/` - Icon and splash screen assets
- `config.xml` - Cordova configuration file
- `package.json` - Node/NPM project configuration

---

## Screenshots

![Screenshot 2024-08-25 at 05 56 42](https://github.com/user-attachments/assets/c4651899-7e59-4d42-93c8-a98011e2b8e6)

![Screenshot 2024-08-25 at 05 57 02](https://github.com/user-attachments/assets/a8ef6255-e423-4b8e-8471-24e4c38f8500)

![Screenshot 2024-08-25 at 05 57 52](https://github.com/user-attachments/assets/e098df5c-915e-4bfd-b46f-a36ee29a3e3a)     ![Screenshot 2024-08-25 at 05 58 10](https://github.com/user-attachments/assets/...)

![Screenshot 2024-08-25 at 05 58 25](https://github.com/user-attachments/assets/a21e1ea7-4f07-48f0-a9cf-484ccca025d7)     ![Screenshot 2024-08-25 at 05 58 43](https://github.com/user-attachments/assets/...)

---

## References

- [Ionic Framework Docs](https://ionicframework.com/docs)
- [Cordova Documentation](https://cordova.apache.org/docs/en/latest/)
- [AngularJS Docs](https://angularjs.org/)
- [Official Project Page](https://gil.gmbh/en/projects/project_02/)

---

## License

This project is licensed for commercial use by the project owner.

---

## Keywords

Ionic, Cordova, AngularJS, HTML, CSS, JSON, JavaScript, Swift, TypeScript
