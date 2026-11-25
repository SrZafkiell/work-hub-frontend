# work-hub-frontend

The web app of [work-hub](https://github.com/SrZafkiell/work-hub): one place for your
work and your personal projects, with tasks, meetings, notes and calendars kept in
separate workspaces.

> Status: planning. The plan, the decisions and the risk register live in
> [work-hub](https://github.com/SrZafkiell/work-hub/blob/main/docs/PLAN.md). The issues
> of this repository are created from that plan and tracked on one
> [project board](https://github.com/users/SrZafkiell/projects/2).

## What lives here

- The React and TypeScript web app, installable on a phone and on a computer.
- The service worker: the app shell offline, and notifications through Web Push.
- The API client, generated from a pinned version of the backend's contract.
- The screens of every module: sign-in with a passkey, workspaces and focus mode, tasks
  and the Today view, notes and search, the agenda, reminders and meeting notes.

## What lives elsewhere

- The API, the worker and the contract:
  [work-hub-backend](https://github.com/SrZafkiell/work-hub-backend).
- The server setup, the Compose files, the deploy agent, the release manifests and the
  end-to-end tests: [work-hub](https://github.com/SrZafkiell/work-hub).
- The desktop app, planned:
  [work-hub-desktop](https://github.com/SrZafkiell/work-hub-desktop).

## How it ships

CI builds, scans and signs one image of static files on `main`. A release of the product
is a signed manifest in `work-hub` that pins this image together with an API image that
passed the end-to-end tests with it. The server pulls and verifies; no CI system holds a
credential for it.

## License

Apache-2.0. See [LICENSE](LICENSE).
