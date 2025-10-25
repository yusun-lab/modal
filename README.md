# Modal (Vue 3 Teleport Modals)

A minimal Vue 3 + TypeScript demo showcasing how to render modals outside the app root using Teleport. Includes two modal instances with slots and simple toggle handlers.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

## Usage
- **Open first modal**: Click "Open modal (alt)" while holding Alt.
- **Open second modal**: Click "Open modal (shift)" while holding Shift.
- Modals emit a `close` event handled in `App.vue` to toggle visibility.

## Key files
- `src/App.vue` — Demo page toggling two modals with `Teleport`.
- `src/components/Modal.vue` and `src/components/ModalTwo.vue` — Modal components with slots.
- `public/index.html` — Teleport targets: a div with class `modal` and a div with id `modal-two` used as render hosts.

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
