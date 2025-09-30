# Scaffold with TopAppBar, BottomBar, and FAB (Compose)

**Goal**
- Implement a `Scaffold` with:
  - **TopAppBar** showing the app title
  - **Bottom navigation bar** with 3 items (Home, Settings, Profile)
  - **FAB** that triggers a **Snackbar** message
- Apply `innerPadding` from `Scaffold` content lambda to avoid overlap.

## How it works
- `Scaffold` provides structure: `topBar`, `bottomBar`, `floatingActionButton`, `snackbarHost`.
- Bottom bar uses `NavigationBar` + `NavigationBarItem`; the selected tab is held in state.
- FAB uses `SnackbarHostState` + `coroutineScope` → `snackbarHostState.showSnackbar("...")`.
- The screen content applies `Modifier.padding(innerPadding)` to respect bars & FAB.
