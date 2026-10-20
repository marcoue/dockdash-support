---
title: DockDash
description: Keep your Mac’s Dock on the display you choose.
platform: macOS
---

# DockDash

**Keep your Dock on the display you choose.**

DockDash helps keep the macOS Dock on a selected display. Choose a screen in the dashboard or menu bar, and DockDash attempts to bring the Dock there while protecting the bottom edges of other displays.

> DockDash requires the Dock to be positioned at the bottom of the screen. Protection requires macOS Accessibility and event access, and depends on DockDash remaining open.

## Features

- Choose a connected display as the Dock’s home screen.
- Give displays custom names to tell them apart.
- Start or stop protection from the dashboard or menu bar.
- Automatically attempt to move the Dock to the selected display.
- See whether protection is active and whether DockDash has confirmed the Dock’s location.
- Choose the app’s appearance and interface language.

## Requirements

- macOS 15.4 or later
- The Dock set to **Bottom** in **System Settings → Desktop & Dock**
- Accessibility and event access for DockDash

DockDash supports the Dock at the bottom of the screen. Left and right Dock positions are not supported.

## Install and set up

1. Download DockDash from the [DockDash website](https://dashapps.app/dockdash/).
2. Move `DockDash.app` to Applications and open it.
3. Set the Dock position to **Bottom** in **System Settings → Desktop & Dock**.
4. In DockDash, choose **Lock Dock to Screen** beside the display you want to use.
5. If macOS requests access, allow DockDash under **System Settings → Privacy & Security → Accessibility**, then return to DockDash.

DockDash also checks the event permissions needed to protect display edges and move the Dock. If protection cannot start, follow the status message in the app and review the permissions macOS shows for DockDash.

## Use DockDash

### Choose a display

Open the **Displays** section in the dashboard. Select **Lock Dock to Screen** beside a connected display to select it and start protection. The **(Primary)** label identifies the primary display reported by macOS.

To rename a display, select its pencil button, enter an alias, and choose **Save**. Aliases appear in DockDash; they do not change the display’s macOS name. Displays with stable identifiers keep their aliases between launches.

### Move the Dock

If the Dock is not on the selected display, DockDash attempts a brief pointer movement near that display’s bottom edge to bring it there. The pointer may move or briefly disappear during the attempt, then returns to its previous position. Mouse movement, a click, a drag, or scrolling interrupts the attempt. DockDash makes up to three automatic transfer attempts each time protection starts.

While protection is active, pointer movement near the bottom edge of other displays may be limited. Choose **Unlock Dock from Screen** to stop protection and restore unrestricted access to those edges. Unlocking leaves the Dock where it is.

### Check protection status

DockDash distinguishes active protection from confirmed Dock placement:

- **Dock is locked to the selected screen** means DockDash has observed the Dock on the selected display.
- **Protection active** means the protection engine is running, but DockDash has not confirmed the Dock’s location. An automatic transfer may still be attempted.
- Permission, display, orientation, or engine messages indicate what needs attention.

The menu-bar popover shares the selected display and status with the dashboard. Use **Settings** to open the dashboard, the update action to check for releases, **About DockDash** to view app information, or **Quit** to stop protection and close the app. Closing the dashboard does not stop protection.

## Preferences

The dashboard’s **General** section includes startup, appearance, and language settings.

**Start Dock protection when DockDash starts** requests protection at app launch using the saved display. It does not prompt for permissions at launch; grant any required access and return to DockDash so it can retry.

In version 1.0, **Show the app icon in the Dock**, **Start DockDash when I sign in**, and **Open the dashboard when DockDash starts** save their preferences, but their associated behavior is not implemented. DockDash currently appears in the Dock, does not register itself as a login item, and opens the dashboard at launch. To launch at sign-in, add DockDash under **System Settings → General → Login Items → Open at Login**.

Choose **System**, **Light**, or **Dark** for appearance, and **EN**, **FR**, or **ES** for the interface language.

## Known limitations

- Protection only supports a bottom-positioned Dock.
- Active protection does not guarantee the Dock’s location; DockDash reports placement as confirmed only after observing it on the selected display.
- Display arrangements, Spaces, sleep and wake, display reconnections, and macOS event handling can affect behavior.
- Stacked, mirrored, virtual, or identical displays and mixed display scaling need additional verification.
- DockDash protects one selected display at a time.

## Build from source

1. Open `DockDash.xcodeproj` in Xcode.
2. Select the **DockDash** scheme.
3. Build and run on macOS 15.4 or later.

The project uses Swift and SwiftUI with AppKit integration. Sparkle is used for app updates.

## Privacy

DockDash processes display information locally and uses Accessibility to inspect the Dock’s location. While protection is active, it handles mouse movement, dragging, button, and scroll events. A brief pointer movement may be used when attempting to move the Dock. DockDash does not record keystrokes or save a continuous pointer history.

See the [DockDash Privacy Policy](https://dashapps.app/dockdash/privacy-policy/) for more information.

## Documentation and support

- [Quick Start Guide](https://dashapps.app/dockdash/quick-start-guide/)
- [User Manual](https://dashapps.app/dockdash/user-manual/)
- [DockDash website](https://dashapps.app/dockdash/)
- [Support and contact](https://dashapps.app/contact/)
- [GitHub support repository](https://github.com/marcoue/DockDash-Support/)

For support, email [dash.app.support@gmail.com](mailto:dash.app.support@gmail.com).
