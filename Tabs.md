
```html
<div class="tabs-group">
<div class="tab-buttons"><button class="tab-link" data-tab="tab1-1">Onglet 1.1</button></div>
<div id="tab1-1" class="tab-content">
<p>Contenu de l'onglet 1.1</p>
</div>
</div>
```

```js
document.addEventListener('DOMContentLoaded', function() {
    var tabGroups = document.querySelectorAll('.tabs-group');

    tabGroups.forEach(function(group) {
        var tabLinks = group.querySelectorAll('.tab-link');
        var tabContents = group.querySelectorAll('.tab-content');

        tabLinks.forEach(function(link) {
            link.addEventListener('click', function() {
                var tabId = this.getAttribute('data-tab');
                var content = document.getElementById(tabId);

                if (this.classList.contains('active')) {
                    // Si l'onglet est déjà actif, on le désactive et on cache le contenu
                    this.classList.remove('active');
                    content.style.display = 'none';
                } else {
                    // Sinon, on active cet onglet et on affiche le contenu
                    tabLinks.forEach(function(link) {
                        link.classList.remove('active');
                    });

                    tabContents.forEach(function(content) {
                        content.style.display = 'none';
                    });

                    this.classList.add('active');
                    content.style.display = 'block';
                }
            });
        });
    });
});
```


```css
.tab-content {
  display: none; /* Tout le contenu des onglets est caché par défaut */
  padding: 10px;
  border: 1px solid #ccc;
  margin-top: 20px;
}
.tab-buttons button {
  padding: 10px;
  margin-right: 5px;
  cursor: pointer;
}
.tab-buttons .active {
  background-color: #ccc;
}
```

https://chatgpt.com/share/9477f7d8-e2ab-477b-a6f3-e35142708bd4