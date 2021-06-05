# CSS

## A Cascata (cascading)

A escolha do browser de qual regra aplicar, cajo haja muitas regras para o mesmo elemento.

- Seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo

inline > tag style > tag link

#### Inline

```html
<h1 style="color: green">Teste</h1>
```

#### Tag style

```html
<style>
    h1 {
        color: gray;
    }
</style>
```

#### Tag link

```css
h1 {
    color: yellow;
}
```

### Especificidade

É um calculo matemático, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados.

- 0: Universal selector (`*`) e negation pseudo-class `:not()`
- 1: Element type selector (`h1`) e pseud-element `::before()` `::after`
- 10: Classes e attribute selectors `[type="radio"]`
- 100: ID selector
- 1000: Inline

### A regra `!important`

- Cuidado, evite o uso
- Não é considerado uma boa prática
- Quebra o fluxo natural da cascata

---

## At-rules @

- Está relacionado ao comportamento do CSS
- Começa com o sinal de `@` seguido do identificador e valor

### Exemplos comuns

- `@important`: incluir um CSS externo

```css
@import "Http://local.com/style.css"
```

- `@media`: regras condicionais para dispositivos

```css
@media (min-width: 500px){

}
```

- `@font-face`: Fontes externas

```css
@font-face {

}
```

- `@keyframes`: Animation

```css
@keyframes nameofanimation {

}
```
