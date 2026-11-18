# Jellyflix 4.5

Jellyflix is a community CSS theme for Jellyfin Web 12 in Modern display mode. It layers a dark palette, a two-column library grid and horizontally scrolling media rows over ElegantFin. When Media Bar is installed, Jellyflix rounds the slides and uses the banner height supplied by the upstream stylesheets to keep the library grid below the banner.

## Installation

1. Select **Modern** in Jellyfin Web's display settings.
2. If you want the featured banner, follow the [Media Bar plugin's own installation instructions](https://github.com/IAmParadox27/jellyfin-plugin-media-bar#installation) and check that the banner appears before applying Jellyflix.
3. Save a copy of your current Custom CSS. For a per-user test, open **Settings → Display → Custom CSS** where available. For a server-wide install, use the dashboard's **Branding → Custom CSS** field.
4. Open [jellyflix.css](jellyflix.css), switch to the raw file view on GitHub and paste the entire stylesheet into Custom CSS. The file already imports ElegantFin, its Media Bar styling add-on and the Modern compatibility stylesheet. Remove duplicate imports from the existing configuration and keep the three imports at the top, in their original order.
5. Save and reload Jellyfin Web. If the previous styles persist, try a hard refresh.

To uninstall, restore your saved Custom CSS or remove the pasted stylesheet and reload.

## Compatibility and limitations

- The reference setup was Jellyfin Web 12 Modern with ElegantFin and Media Bar in desktop Firefox. The layout was confirmed on that installation. Other browsers, devices, Jellyfin builds and plugin versions have not been independently validated.
- Library captions below the images are hidden. Use library artwork with readable labels. The grid was designed with two libraries in mind. Additional libraries, keyboard navigation and small viewports have not been comprehensively tested.
- The banner needs a working Media Bar installation. Jellyflix supplies styling and layout overrides.
- The stylesheet uses modern selectors such as `:has()` and depends on Jellyfin's markup. Legacy mode, native clients and older browser engines are outside the tested setup.
- The imports load from jsDelivr and track upstream's `main` branches. All three original URLs served CSS during release preparation. Upstream changes, CDN outages and client network restrictions can affect the result.
- For layout reports, include your Jellyfin Web version, browser version, viewport dimensions, display mode and plugin version. Use sample media in any public screenshots.

## Credits

| Project | Role | License |
| --- | --- | --- |
| [ElegantFin by lscambo13](https://github.com/lscambo13/ElegantFin) | Base theme and imported Media Bar styling add-on | [GNU GPL v2](https://github.com/lscambo13/ElegantFin/blob/main/LICENSE) |
| [elegantfin-jf12 by mihaif7](https://github.com/mihaif7/elegantfin-jf12) | Imported Modern layout compatibility stylesheet | [GNU GPL v2](https://github.com/mihaif7/elegantfin-jf12/blob/main/LICENSE) |
| [Jellyfin Media Bar by MakD](https://github.com/MakD/Jellyfin-Media-Bar), with the [plugin integration by IAmParadox27](https://github.com/IAmParadox27/jellyfin-plugin-media-bar) | Separately installed featured content banner | [Plugin license file](https://github.com/IAmParadox27/jellyfin-plugin-media-bar/blob/main/LICENSE.md) and [upstream README terms](https://github.com/IAmParadox27/jellyfin-plugin-media-bar#license) |

The Media Bar plugin repository provides a DBAD 1.2 license file credited to MakD. Its README separately describes restrictions on commercial use and redistribution. Consult both sources and obtain clarification from the maintainers before including the plugin in a commercial offering. Jellyflix distributes its own stylesheet and references the upstream ElegantFin stylesheets through their published imports.

## License

The Jellyflix stylesheet is released under the [GNU General Public License, version 2](LICENSE). Third-party projects retain their own licenses and attribution. Jellyflix is an independent community project.
