# Temporarily Hidden Features

This branch enables `RAG_DEMO_MODE` in `src/lib/constants.ts`. Routes and backend
logic remain available; the switch only reduces the visible frontend surface.

| Feature        | Hidden UI location                                                                                       | Restore                                                                      |
| -------------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Calendar       | User menu in `src/lib/components/layout/Sidebar/UserMenu.svelte`                                         | Remove the `<!-- ... -->` wrapper marked `Calendar menu temporarily hidden`. |
| Automations    | User menu in `src/lib/components/layout/Sidebar/UserMenu.svelte`                                         | Remove the wrapper marked `Automation menu temporarily hidden`.              |
| Playground     | User menu in `src/lib/components/layout/Sidebar/UserMenu.svelte`                                         | Remove the wrapper marked `Playground menu temporarily hidden`.              |
| Sidebar extras | Search, pinned items/models/notes, channels, and folders in `Sidebar.svelte`                             | Set `RAG_DEMO_MODE` to `false`.                                              |
| Chat extras    | Model picker, sharing, controls, tools, skills, web/image/code integrations, voice/call, and suggestions | Set `RAG_DEMO_MODE` to `false`.                                              |

RAG demo mode keeps local file upload, prompt submission, streamed answers,
citations, new chat, and chat history visible.

These entries are intentionally not deletions. Do not remove their routes or
backend logic when restoring the menu items.
