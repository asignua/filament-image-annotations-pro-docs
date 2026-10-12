# Changelog

All notable changes to `asignua/filament-image-annotations-pro` are documented here.

## v1.0.2 - 2026-10-12

- Licence terms (`LICENSE.md`): the commercial licence that comes with an Anystack licence key; prices in the README.
- Docs: `scripts/sync-docs.sh` points the screenshots at the public docs repository.

## v1.0.1 - 2026-10-12

- Docs: screenshots, cover and a workbench demo.

## v1.0.0 - 2026-10-09

- Chat Pro integration (auto-enabled when `asignua/filament-chat-pro` ^1.1 is installed): `ChatAttachmentImageSource`, an «Annotate» button in the chat lightbox, a marks badge on thumbnails, the editor modal placed once on panel pages with the chat, annotations removed with the attachment. Config `chat.*`.

- Per-author layers: one annotation row per user and image, shown together (own layer editable, others read-only underlays / chips,
  author name, stable colour, `others_visible_by_default`).
- Numbered pins with comment threads (`PinThreads` service, `PinComment` model), resolve / reopen, orphan cleanup when a pin or layer goes away.
- Threads panel (Livewire) next to the editor canvas and every annotated image.
- `SourceToken`, the `image-annotations-pro::modal` Livewire component and `<x-image-annotations-pro::open-button>`: open the editor from any page.
- Fix: the threads panel was invisible-text-broken (`sr-only` is not in the panel theme, inline style now); it re-reads on the free `image-annotations:saved` event, so a save through the regular action refreshes it; flexible width next to the image.
- Workbench: `storage-link` build step, a `/demo` page with correctly printed Filament styles/scripts.
- Events `PinCommentAdded`, `PinThreadResolved`, `PinThreadReopened`.
- Ten interface languages.
