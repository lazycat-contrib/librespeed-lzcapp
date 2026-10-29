# LibreSpeed for LazyCat

- Upstream: https://github.com/librespeed/speedtest
- Package: `community.lazycat.app.librespeed`; initial upstream version 6.3.1.
- Official image: `ghcr.io/librespeed/speedtest`; runtime mirror: `ghcr.1ms.run/librespeed/speedtest`.
- Image delivery requires matching source/mirror digests; target is Linux amd64, OS 1.5.0+.
- Standalone mode, telemetry disabled, external IP/ISP lookups disabled, inherited statistics password cleared.
- No database or persistent history. No file-chooser interceptor. LazyCat's normal entry authentication stays enabled.
- Only community publication is authorized. Both automatic store publishers are initially disabled; publish the verified versioned Release URL after checking its SHA256.

The workflow tests the exact upstream image on a GitHub runner: frontend HTTP response, ping endpoint, 1 MiB download with no-cache header, 1 MiB upload, inaccessible statistics endpoint, and restart. These checks validate endpoints, not numerical speed accuracy.

This measures the connection between the browser and this server. A proxy, VPN or LazyCat gateway changes that path and can affect measured throughput. It is not a speed test initiated from the NAS to a public server.

LazyCat-device installation, browser measurement UI and gateway performance have not been end-to-end tested. Do not describe the runner tests as real-device validation.
