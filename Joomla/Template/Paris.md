## Formulaire GRID 

![[Pasted image 20230907131425.png]]

```css
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:first-child { grid-area: 1 / 1 / 2 / 2; }
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:nth-child(3) { grid-area: 2 / 1 / 3 / 2; }
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:nth-child(2) { grid-area: 1 / 2 / 3 / 3; }
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:nth-child(4) { grid-area: 3 / 1 / 4 / 3; }
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:nth-child(5) { grid-area: 4 / 1 / 5 / 3; }
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row > div:last-child{ grid-area: 5 / 1 / 6 / 3; }

.custom .mod_tm_ajax_contact_form textarea {
  height: 157px !important;
  min-height: 157px;
}
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row input{
  height: 69px !important; 
}
.body__home .mod_tm_ajax_contact_form_custom fieldset > .row textarea, .body__home .mod_tm_ajax_contact_form_custom fieldset > .row input{
  border: solid white 3px;
  border-radius: 25px;
  margin-bottom: 0 !important;
}
```