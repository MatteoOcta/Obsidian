## 1 + 2 items GRID 
```css
section.page-blog__home .items-leading{
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 50% 50%;
}
section.page-blog__home .items-leading > article {
  min-width: 100%;
  margin-bottom: 0;
}
section.page-blog__home .items-leading .leading-0 {
  grid-column: 1 / 1;
  grid-row: span 2;
}
section.page-blog__home .items-leading .leading-1 {
  grid-column: 2 / 2;
  grid-row: 1 / 1;
}
section.page-blog__home .items-leading .leading-2{
  grid-column: 2 / 2;
  grid-row: 2 / 2;
  align-self: end;
}
.page-blog .items-leading .item .item-content .blog_inner{
  padding: 40px 40px 12px;
}
```