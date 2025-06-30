# DataCenter Manager - Official Commercial Angular Mobile App

![Screenshot 2024-08-25 at 05 56 42](https://github.com/user-attachments/assets/c4651899-7e59-4d42-93c8-a98011e2b8e6)
![Screenshot 2024-08-25 at 05 57 02](https://github.com/user-attachments/assets/a8ef6255-e423-4b8e-8471-24e4c38f8500)
![Screenshot 2024-08-25 at 05 57 52](https://github.com/user-attachments/assets/e098df5c-915e-4bfd-b46f-a36ee29a3e3a)
![Screenshot 2024-08-25 at 05 58 25](https://github.com/user-attachments/assets/a21e1ea7-4f07-48f0-a9cf-484ccca025d7)

---

## Table of Contents

- [Project Summary](#project-summary)
- [Key Features](#key-features)
- [Technical Stack](#technical-stack)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Application Walkthrough](#application-walkthrough)
- [Core Components & Routing](#core-components--routing)
- [API & Services](#api--services)
- [Learning Examples](#learning-examples)
- [References](#references)
- [License](#license)
- [Keywords](#keywords)
- [Conclusion](#conclusion)

---

## Project Summary

**DataCenter-Manager** is an official commercial mobile application designed for IT administrators and technical users to remotely access, monitor, and manage data centers and servers from a mobile device. The app provides a seamless, mobile-first dashboard to create and manage servers, monitor storage, handle snapshots, control server power, and perform other critical data center operations.

The primary goal is to simplify and centralize remote management tasks for servers and data centers, offering an intuitive user experience with robust features.

- Explore more on the [official project webpage](https://gil.gmbh/en/projects/project_02/).

---

## Key Features

- **Remote Server Creation:** Instantly create and configure new servers from anywhere.
- **Storage Management:** Manage hard drive snapshots, monitor storage usage, and retrieve backups.
- **Server Connectivity:** Connect/disconnect to remote servers or full data centers.
- **Server Power Controls:** Remotely power on/off servers or data center components.
- **Snapshot Management:** Take, view, and restore HDD snapshots for disaster recovery.
- **User-Friendly Dashboard:** Intuitive interface for easy monitoring and management.
- **Mobile-First Design:** Developed with Ionic/Cordova for cross-platform mobile compatibility.

---

## Technical Stack

- **Frontend:** Ionic Framework, AngularJS, TypeScript, HTML, CSS
- **Mobile Integration:** Cordova
- **Data/Communication:** JSON, JavaScript
- **Platform-Specific:** Swift (for iOS-specific features)
- **Other Libraries:** angular-translate, localforage, angular-filter, ngSanitize

---

## Project Structure

```
DataCenter-Manager--AngularApp/
├── src/
│   ├── app/             # Angular modules, components, services
│   ├── assets/          # Static assets (images, icons, etc.)
│   └── environments/    # Environment-specific config
├── www/
│   ├── js/
│   │   ├── app-js/      # Main app logic (controllers, services, app.js)
│   │   ├── utilities/   # Utility libraries
│   │   └── sliding-menu/ # Menu-related controllers
│   ├── templates/       # HTML templates for views
│   └── index.html       # Main entry point
├── hooks/               # Cordova hooks/scripts
├── resources/           # App icons, splash screens
├── config.xml           # Cordova config file
├── package.json         # Node/NPM config
└── README.md            # Project documentation
```

---

## Installation & Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (latest LTS recommended)
- [npm](https://www.npmjs.com/)
- [Ionic CLI](https://ionicframework.com/docs/cli): `npm install -g @ionic/cli`
- [Cordova CLI](https://cordova.apache.org/docs/en/latest/guide/cli/): `npm install -g cordova`
- [Git](https://git-scm.com/)

---

### Clone the Repository

```bash
git clone https://github.com/arnobt78/DataCenter-Manager--AngularApp.git
cd DataCenter-Manager--AngularApp
```

---

### Install Dependencies

```bash
npm install
```

---

### Add Platforms

```bash
ionic cordova platform add android
ionic cordova platform add ios
```
> **Note:** iOS development requires a Mac with Xcode installed.

---

## Usage Guide

### Running the App in a Browser

```bash
ionic serve
```

---

### Running on a Device

```bash
ionic cordova run android
ionic cordova run ios
```

---

### Building for Production

```bash
ionic cordova build android --prod --release
ionic cordova build ios --prod --release
```

---

## Application Walkthrough

### Login & First Start

- **Language & Terms:** On first launch, select language and review terms (`login.firstStartLanguage`).
- **Credentials:** Enter login credentials (`login.firstStartCredentials`).
- **PIN Code:** Set or enter a PIN for quick access (`login.setAppCode`).

---

### Main Dashboard

- **All Servers/Storages:** View lists of all servers and storages across datacenters (`app.allServers`, `app.allStorages`).
- **Datacenters:** View and manage all registered datacenters (`app.datacenters`).

---

### Server & Storage Management

- **Servers:** List, view, and manage individual servers (`app.servers`, `app.singleServer`).
- **Storages:** List, view, and manage storage devices (`app.storages`, `app.singleStorage`).
- **Snapshots:** Manage HDD snapshots for backup and recovery (`app.snapshots`).

---

### App Settings & Help

- **Settings:** Configure app preferences and options (`app.settings`).
- **About:** App info and credits (`app.about`).
- **Help:** User guides and support (`app.help`).

---

## Core Components & Routing

### Main Angular Modules

- `datacenterManager`: Root Angular module.
- `datacenterManager.controllers`: All controllers for views.
- `datacenterManager.services`: Services for API and data.
- Utility modules: `pascalprecht.translate`, `angular.filter`, `ngSanitize`.

---

### Key Controllers (Examples)

```javascript
// Example: List of Datacenters Controller
angular.module('datacenterManager.controllers')
  .controller('ListofDatacentersController', function (DemoFactory, UserData, ...) {
    var self = this;
    self.datacenters = UserData.GetDatacenters();
    // Methods for managing datacenters...
  });
```

---

### Main Routes (app.js)

- `/login/firstStartLanguage` → Language & terms screen
- `/login/firstStartCredentials` → Login with credentials
- `/login/setAppCode` → Set PIN code
- `/app/allServers` → All servers
- `/app/allStorages` → All storages
- `/app/datacenters` → Datacenter list
- `/app/servers` → Server list
- `/app/singleServer` → Server details
- `/app/storages` → Storages list
- `/app/singleStorage` → Storage details
- `/app/snapshots` → Snapshot management
- `/app/settings` → Settings
- `/app/about` → About
- `/app/help` → Help

---

## API & Services

- **UserData:** Handles user/session data.
- **DemoFactory:** Demo/mock data and testing support.
- **SSLValidatedAPICall:** Performs secure server API calls.
- **PopUpService:** Shows popup dialogs and alerts.
- **HardwareBackButtonManager:** Manages hardware back button behavior on mobile.
- **Translation:** `angular-translate` for internationalization.

---

## Learning Examples

### Example: Adding a New Server

```javascript
// In ListofServersController
self.addServer = function(serverData) {
  SSLValidatedAPICall.createServer(serverData)
    .then(function(response) {
      // Handle success
    })
    .catch(function(error) {
      // Handle error
    });
};
```

### Example: Router Configuration

```javascript
.state('app.servers', {
  url: '/servers',
  cache: false,
  views: {
    'menuContent': {
      templateUrl: 'templates/listof-servers-layout.html',
      controller: 'ListofServersController as dashServersCtrl'
    }
  }
})
```

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

---

## Conclusion

**DataCenter-Manager** empowers IT professionals with a robust, mobile-first toolkit for managing servers and datacenters securely and efficiently—anytime, anywhere. Its modular Angular/Ionic architecture and intuitive UI make it both powerful and easy to extend. Whether you're learning mobile app development or managing critical infrastructure, this app is a valuable resource.

---

> Happy Coding! 🚀  
> Thank you!
