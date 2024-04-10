```css
@media (max-width: 1180px) {
}

@media (max-width: 1024px) {
}

@media (max-width: 820px) {
  .flex {
    flex-direction: column;
  }
  .flex > * {
    width: 100%;
    --basis: 100% !important;
  }
}

@media (max-width: 768px) {
}

@media (max-width: 450px) {
  .flex {
    padding-inline: 25px;
  }
}
```