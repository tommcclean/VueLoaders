# VueLoaders
VueLoaders is a library of Vue components which help you to make loading times provide a bettr user experience.

$ npm install @thomaswilliammcclean/vuepanels --save

```javascript
<script>
  import "@thomaswilliammcclean/vuepanels";
</script>
```

## Included Components
### Loading Container:
That accepts loading state as a prop and conditionally renders a spinner or your content in a slot.
```html
<loading-container :is-loading="true">
    <p slot="loader">Is loading</p>
    <p slot="content">Is NOT loading</p>
</loading-container>
```

### Loading Button
A button which when clicked accepts a loading state and conditionally renders a spinner inside the button.
```html
<loading-button :is-loading="true" text="Submit">
    <span>[ Is Loading ]</span>
</loading-button>
```
