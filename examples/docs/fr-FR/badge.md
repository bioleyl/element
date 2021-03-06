## Badge

Un numéro ou un statut affiché sur un bouton ou une icône

### Utilisation de base

Affiche la quantité de nouveaux messages.

::: demo Le montant est défini avec `valeur` qui accepte un `Number` ou une `String`.
```html
<el-badge :value="12" class="item">
  <el-button size="small">commentaires</el-button>
</el-badge>
<el-badge :value="3" class="item">
  <el-button size="small">réponses</el-button>
</el-badge>

<el-dropdown trigger="click">
  <span class="el-dropdown-link">
    Click Me<i class="el-icon-caret-bottom el-icon--right"></i>
  </span>
  <el-dropdown-menu slot="dropdown">
    <el-dropdown-item class="clearfix">
      comments
      <el-badge class="mark" :value="12" />
    </el-dropdown-item>
    <el-dropdown-item class="clearfix">
      replies
      <el-badge class="mark" :value="3" />
    </el-dropdown-item>
  </el-dropdown-menu>
</el-dropdown>

<style>
.item {
  margin-top: 10px;
  margin-right: 40px;
}
</style>
```
:::

### Valeur maximale

Vous pouvez personnaliser la valeur max.

::: demo La valeur max est définie par la propriété `max` qui est un `Number`. Notez que cela ne fonctionne que lorsque `value` est aussi un `Number`.
```html
<el-badge :value="200" :max="99" class="item">
  <el-button size="small">commentaires</el-button>
</el-badge>
<el-badge :value="100" :max="10" class="item">
  <el-button size="small">réponses</el-button>
</el-badge>

<style>
.item {
  margin-top: 10px;
  margin-right: 40px;
}
</style>
```
:::

### Personnalisations

Affiche du texte autre que des numéros.

::: demo Lorsque `value` est une` String`, il peut afficher du texte personnalisé.
```html
<el-badge value="new" class="item">
  <el-button size="small">commentaires</el-button>
</el-badge>
<el-badge value="hot" class="item">
  <el-button size="small">réponses</el-button>
</el-badge>

<style>
.item {
  margin-top: 10px;
  margin-right: 40px;
}
</style>
```
:::

### Petit point rouge

Utilisez un point rouge pour marquer le contenu qui doit être remarqué.

::: demo Utilisez l'attribut `is-dot`. C'est un `Boolean`.
```html
<el-badge is-dot class="item">query</el-badge>
<el-badge is-dot class="item">
  <el-button class="share-button" icon="share" type="primary"></el-button>
</el-badge>

<style>
.item {
  margin-top: 10px;
  margin-right: 40px;
}
</style>
```
:::

<style scoped>
  .share-button {
    width: 36px;
    padding: 10px;
  }

  .mark {
    margin-top: 8px;
    line-height: 1;
    float: right;
  }

  .clearfix {
    @utils-clearfix;
  }

  .item {
    margin-right: 40px;
  }
</style>

### Attributs
| Attributs          | Description            | Type            | Valeurs acceptées                 | Défaut   |
|-------------  |---------------- |---------------- |---------------------- |-------- |
| value          | valeur affichée      | string, number          |          —             |    —     |
| max          |  Valeur maximale, affiche '{max} +' quand elle est dépassée. Fonctionne uniquement si `value` est un` Number`   | number  |         —              |     —    |
| is-dot       | Si un petit point est affiché   | boolean  |  —  |  false |
