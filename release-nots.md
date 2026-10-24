## CSS `scroll-marker-group` modes

The `scroll-marker-group` property supports two modes that control the focus order and accessibility behavior of `::scroll-marker-group` and `::scroll-marker` following WAI-ARIA patterns:

- `links` (default): The generated `::scroll-marker-group` operates like a navigation list (`navigation` role), and `::scroll-marker` elements act as standard links (`link` role). All `::scroll-marker` elements are sequential tab stops. Activating a link marker moves focus to the target element.
- `tabs`: The generated `::scroll-marker-group` operates like a tablist (`tablist` role), `::scroll-marker` elements take on the `tab` role, and originating elements get the `tabpanel` role. Only the active `::scroll-marker` acts as a tab stop, and users navigate between markers with arrow keys. Content from inactive tabs is hidden from the accessibility tree, and focus stays on the marker when activated.
-