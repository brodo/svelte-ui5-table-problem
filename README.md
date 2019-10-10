# Svelte UI5 table-row problems

```bash
npm install
npm run dev
```

Take a look at `scr/App.svelte`. It contains two tables one basic HTML one and a UI5 table.
They both use the same array as a data model. If you get rid of the `setImmediate` everything works.

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.
