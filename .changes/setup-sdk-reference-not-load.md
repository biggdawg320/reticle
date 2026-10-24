### Fixed

- **`@reticlehq/server`: setup said "The SDK IS in the page" when the page only referenced it.** The check reads the HTML text, so a page whose import of `@reticlehq/browser` failed (a CDN 404 for a version that is not published yet, a private registry, a blocked script) got the same sentence as a page where the SDK loaded. Setup now says that the page references the SDK, and tells you to open the browser console and look for a failed import of `@reticlehq/browser` when no SDK session dialled.
