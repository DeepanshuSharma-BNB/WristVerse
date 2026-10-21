# WristVerse

**Interactive universe for Meta Ray-Ban Display**

WristVerse is a standalone, lightweight 600 × 600 web app that renders a 3D-style solar system using Canvas, with animated planets and orbit exploration.

**Website:** https://deepanshusharma-bnb.github.io/WristVerse/

## Using it

- On supported Meta Ray-Ban Display glasses, select **Wrist** and allow orientation access where prompted. Move your wrist to orbit the scene; use **Recenter** to set a neutral wrist orientation.
- Swipe left/right to change planets; use Select/pinch to inspect the selected object.
- On a phone or desktop, drag the scene; Left/Right changes objects, Enter inspects, and Down moves focus into the action bar.

### Sensor compatibility

This app attempts `RelativeOrientationSensor({frequency: 30, referenceFrame: 'device', sensorId: 'emg-wrist'})`. This Meta-specific wrist capability depends on the wearable browser, firmware and permissions. The app displays an error if unavailable, and touch/keyboard controls remain accessible. Wrist support has been simulated in development but **has not yet been verified on physical Ray-Ban Display hardware**.

There is no backend, analytics, external JavaScript library, CDN, camera/microphone access, account requirement, or remote processing of sensor data. All rendering and sensor processing happens locally in the glasses' web browser.

Planet sizes and orbital distances are artistic approximations, not to scale.

## Deployment

This public repository is configured for automatic GitHub Pages deployment on pushes to `main`. Enable it once in **Settings → Pages → Build and deployment → Source: GitHub Actions**, if the site hasn't yet been enabled.

When deployment succeeds, register the URL above in Meta AI under the web-app developer app connections and open it on your glasses.

Documentation: https://wearables.developer.meta.com/docs/develop/webapps/build/wrist
