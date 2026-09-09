# PaaS Cloud Management Console · Frontend

A management console UI for a **cloud-native PaaS platform**, covering the visual management of applications, services, domains, storage, images and users, plus a "cloud app marketplace" page.

> **Note**: This is a frontend-only implementation, built on top of the open-source [Beagle Admin](https://github.com/themesberg/beagle-admin) template (Bootstrap 4). The corresponding (Go) backend is not included in this repository.

## Pages

| Page | File | Description |
| --- | --- | --- |
| Dashboard | `middle-index.html` | Overview |
| Applications | `pod-index.html` / `pod-create.html` / `pod-detail.html` | Pod list / create / detail |
| Services | `svc-index.html` / `svc-create.html` / `svc-detail.html` | Service list / create / detail |
| Domains | `route-index.html` / `route-create.html` / `route-detail.html` | Route (domain) list / create / detail |
| Volumes | `volume-index.html` / `volume-create.html` / `volume-detail.html` | Storage volume management |
| Users | `user-index.html` | Platform user management |
| App Marketplace | `image-index.html` | Cloud app marketplace (OA, low-code, CRM, alerting, etc.) |

## Tech Stack

- HTML5 / CSS3 / JavaScript
- Bootstrap 4 (Beagle Admin template)
- jQuery, Chart.js, jQuery-Flot, etc. (`assets/lib/` vendored locally)

## Project Structure

```
├── *.html                 # Business pages
└── assets/
    ├── css/               # Custom styles
    ├── img/               # Icons / images
    ├── js/                # Page scripts
    └── lib/               # Third-party frontend libraries (vendored)
```

## Local Preview

No build step required — open any `*.html` in a browser (pages link to each other via relative paths):

```bash
# Or serve statically
python -m http.server 8000
# Visit http://localhost:8000/middle-index.html
```

## License

The UI template follows the original Beagle Admin template's MIT License; the business pages are a personal learning implementation.
