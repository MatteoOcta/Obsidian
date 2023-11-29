
## Formulaire home grid 

![[Pasted image 20231123145938.png]]

```css
.mod_tm_ajax_contact_form > fieldset > .row {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 20px;
  grid-row-gap: 5px;
}
.mod_tm_ajax_contact_form > fieldset > .row input,
.mod_tm_ajax_contact_form > fieldset > .row > div {
  margin: 0;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(1) {
  grid-area: 1 / 3 / 4 / 5;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(2) {
  grid-area: 1 / 1 / 2 / 3;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(3) {
  grid-area: 2 / 1 / 3 / 3;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(4) {
  grid-area: 3 / 1 / 4 / 3;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(5) {
  grid-area: 4 / 1 / 5 / 5;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(6) {
  grid-area: 5 / 1 / 6 / 5;
}
.mod_tm_ajax_contact_form > fieldset > .row > div:nth-child(7) {
  grid-area: 6 / 1 / 6 / 5;
}
.row:before,
.row:after {
  content: none !important;
}
.mod_tm_ajax_contact_form input{
  height: 59px !important;
}
.mod_tm_ajax_contact_form textarea {
  height: 227px !important;
}
```