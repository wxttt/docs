# Navbar

> A top navigation panel, similar to <a v-link="{path:'/tabbar'}">Tabbar</a>. Dependent on tab-item.

------------

## Import

```javascript
import { Navbar, TabItem } from 'mint-ui';

Vue.component(Navbar.name, Navbar);
Vue.component(TabItem.name, TabItem);
```

## Example
Works with <a v-link="{path:'/tab-container'}">tab-container</a>

```html
<mt-navbar v-model="selected">
  <mt-tab-item id="1">option A</mt-tab-item>
  <mt-tab-item id="2">option B</mt-tab-item>
  <mt-tab-item id="3">option C</mt-tab-item>
</mt-navbar>

<!-- tab-container -->
<mt-tab-container v-model="selected">
  <mt-tab-container-item id="1">
    <mt-cell v-for="n in 10" :title="'content ' + n" />
  </mt-tab-container-item>
  <mt-tab-container-item id="2">
    <mt-cell v-for="n in 4" :title="'content ' + n" />
  </mt-tab-container-item>
  <mt-tab-container-item id="3">
    <mt-cell v-for="n in 6" :title="'content ' + n" />
  </mt-tab-container-item>
</mt-tab-container>
```

## API

### navbar

| option | description | type | acceptable values | default |
|------|-------|---------|-------|--------|
| fixed | if the component is fixed at the top | Boolean | | false |
| value | id of the selected tab-item | * | |  |

### tab-item
| option | description | type | acceptable values | default |
|------|-------|---------|-------|--------|
| id | id of tab-item | * | |  |

## Slot
### navbar
| name | description |
|------|--------|
| - | content |

### tab-item
| name | description |
|------|--------|
| - | displayed text |
|icon | icon |
