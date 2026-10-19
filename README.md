
# HotWheels Basketball Overlay

A customizable basketball scoreboard for Streamlabs with a separate mobile controller.

## Files

- `index.html` — scoreboard overlay
- `controller.html` — phone-friendly scoreboard controller

## Publish with GitHub Pages

1. Upload both HTML files to the root of the HotWheelsBasketball repository.
2. Open the repository's **Settings**.
3. Select **Pages**.
4. Under the build and deployment section, select **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish the site.

The pages should be available at:

- Overlay: `https://YOUR-USERNAME.github.io/HotWheelsBasketball/`
- Controller: `https://YOUR-USERNAME.github.io/HotWheelsBasketball/controller.html`

Replace `YOUR-USERNAME` with your GitHub username.

## Remote control setup

The controller and overlay use Supabase Realtime Broadcast to share score updates.

1. Create a Supabase project.
2. Find the project URL and public anon/publishable key in the project's API settings.
3. Open `controller.html` on your phone or computer.
4. Enter the project URL, public key, and a room name.
5. Select **Connect / reconnect**.
6. Select **Copy Streamlabs overlay URL**.
7. In Streamlabs, add a Browser Source and paste the copied URL.
8. Set the Browser Source width and height to suit your stream, for example 1920 × 1080.

Use the same room name on all devices. Supabase Realtime must be available for the project.

## Notes

- No database table is required; the pages use Realtime Broadcast.
- Use only your project's public anon/publishable key in the browser. Never put a Supabase service-role key in the page.
- The score controller saves its settings in that browser's local storage.
- Team logos must be reachable image URLs. A direct HTTPS image URL works best.
