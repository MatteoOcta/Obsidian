```css
.flex {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  --col-gap: 0px;
  --row-gap: 0px;
  --basis: 100%;
  column-gap: var(--col-gap);
  row-gap: var(--row-gap);
}

.flex.jstart {
  justify-content: flex-start;
}

.flex.jcenter {
  justify-content: center;
}

.flex.jend {
  justify-content: flex-end;
}

.flex.jbetween {
  justify-content: space-between;
}

.flex.jaround {
  justify-content: space-around;
}

.flex.jevenly {
  justify-content: space-evenly;
}

.flex.istart {
  align-items: flex-start;
}

.flex.iend {
  align-items: flex-end;
}

.flex.istretch {
  align-items: stretch;
}

.flex.icenter {
  align-items: center;
}

.flex.col {
  flex-direction: column;
}

.flex.grow > * {
  flex-grow: 1;
}

.flex.no-grow > * {
  flex-grow: 0;
}

.flex.wrap {
  flex-wrap: wrap;
}

.flex.no-wrap {
  flex-wrap: nowrap;
}

.flex.shrink > * {
  flex-shrink: 1;
}

.flex.no-shrink > * {
  flex-shrink: 0;
}

.flex.no-basis > * {
  flex-basis: auto;
}

.flex.no-gap {
  --col-gap: 0px;
  --row-gap: 0px;
}

.flex.gap-5 {
  --col-gap: 5px;
  --row-gap: 5px;
}

.flex.gap-10 {
  --col-gap: 10px;
  --row-gap: 10px;
}

.flex.gap-15 {
  --col-gap: 15px;
  --row-gap: 15px;
}

.flex.gap-20 {
  --col-gap: 20px;
  --row-gap: 20px;
}

.flex.gap-25 {
  --col-gap: 25px;
  --row-gap: 25px;
}

.flex.gap-30 {
  --col-gap: 30px;
  --row-gap: 30px;
}

.flex.gap-35 {
  --col-gap: 35px;
  --row-gap: 35px;
}

.flex.gap-40 {
  --col-gap: 40px;
  --row-gap: 40px;
}

.flex.gap-50 {
  --col-gap: 50px;
  --row-gap: 50px;
}

.flex.even-10 > * {
  --basis: 10%;
}

.flex.even-20 > * {
  --basis: 20%;
}

.flex.even-25 > * {
  --basis: 25%;
}

.flex.even-33 > * {
  --basis: 33.33333333333333%;
}

.flex.even-50 > * {
  --basis: 50%;
}

.flex.child-80-20 > *:nth-child(odd) {
  --basis: 80%;
}

.flex.child-80-20 > *:nth-child(even) {
  --basis: 20%;
}

.flex.child-20-80 > *:nth-child(odd) {
  --basis: 20%;
}

.flex.child-20-80 > *:nth-child(even) {
  --basis: 80%;
}

.flex.child-75-25 > *:nth-child(odd) {
  --basis: 75%;
}

.flex.child-75-25 > *:nth-child(even) {
  --basis: 25%;
}

.flex.child-25-75 > *:nth-child(odd) {
  --basis: 25%;
}

.flex.child-25-75 > *:nth-child(even) {
  --basis: 75%;
}

.flex.child-70-30 > *:nth-child(odd) {
  --basis: 70%;
}

.flex.child-70-30 > *:nth-child(even) {
  --basis: 30%;
}

.flex.child-30-70 > *:nth-child(odd) {
  --basis: 30%;
}

.flex.child-30-70 > *:nth-child(even) {
  --basis: 70%;
}

.flex.child-60-40 > *:nth-child(odd) {
  --basis: 60%;
}

.flex.child-60-40 > *:nth-child(even) {
  --basis: 40%;
}

.flex.child-40-60 > *:nth-child(odd) {
  --basis: 40%;
}

.flex.child-40-60 > *:nth-child(even) {
  --basis: 60%;
}

.flex > * {
  flex-basis: calc(var(--basis) - var(--col-gap));
}

/*--------------------- Media querries --------------------------*/
@media (max-width: 1300px) {
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