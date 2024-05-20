# Agenda de Contatos

Este projeto é uma aplicação web para gerenciar uma agenda de contatos. Utiliza o Vue.js com Vuetify para a interface do usuário e inclui funcionalidades para adicionar, editar e deletar contatos. Além disso, implementa uma formatação especial para números de telefone com DDD 11, destacando essas entradas com um fundo azul e texto branco.

## Tecnologias Utilizadas

- **Vue.js**: Framework JavaScript progressivo para a construção de interfaces de usuário.
- **Vuetify**: Biblioteca de componentes de UI para Vue.js, baseada no Material Design.
- **Bootstrap**: Biblioteca de CSS para estilização rápida e responsiva.
- **VMask**: Plugin Vue para máscaras de entrada.

## Funcionalidades

- **Adicionar Contato**: Adicione novos contatos à agenda.
- **Editar Contato**: Edite as informações de contatos existentes.
- **Deletar Contato**: Remova contatos da agenda.
- **Formatação de Telefone**: Máscara para formatação de números de telefone.
- **Destaque de DDD 11**: Contatos com DDD 11 são destacados com uma cor de fundo azul e texto branco.

<p align="center">

https://user-images.githubusercontent.com/93441084/198377088-877b8c49-fc22-4186-b849-d3afa7b1f69e.mp4
</p>

## Estrutura do Projeto

- **index.html**: Arquivo principal contendo a estrutura HTML e a lógica Vue.js.
- **style**: Seção de estilos onde as classes CSS são definidas, incluindo a classe especial `.ddd-11`.

## Como Executar

1. **Clone o Repositório**

   ```bash
   git clone https://github.com/seu-usuario/agenda-de-contatos.git
   cd agenda-de-contatos
   ```

2. **Abra o Arquivo HTML**

   Abra o arquivo `index.html` no seu navegador preferido para visualizar e interagir com a aplicação.

## Alterações e Customizações

### Adicionando a Classe CSS para DDD 11

No arquivo `index.html`, dentro da tag `<style>`, adicionamos a classe CSS `.ddd-11` para estilizar linhas com o DDD 11:

```css
<style>
  .ddd-11 {
    background-color: blue !important;
    color: white;
  }
</style>
```

### Aplicando a Classe CSS no `v-data-table`

Modificamos o componente `v-data-table` para aplicar a classe condicionalmente usando a propriedade `:item-class`:

```html
<v-data-table :headers="headers" :items="desserts" class="elevation-2" :item-class="applyClass">
  <!-- ...restante do código... -->
</v-data-table>
```

### Adicionando o Método `applyClass`

No script Vue, adicionamos o método `applyClass` para retornar a classe `ddd-11` se o telefone começar com "(11)":

```js
methods: {
  applyClass(item) {
    return item.phone.startsWith('(11)') ? 'ddd-11' : '';
  },
  // ...restante dos métodos...
}
```

## Contribuição

1. **Fork o Projeto**
2. **Crie sua Feature Branch**

   ```bash
   git checkout -b feature/nova-feature
   ```

3. **Commit suas Mudanças**

   ```bash
   git commit -m 'Adiciona nova feature'
   ```

4. **Push para a Branch**

   ```bash
   git push origin feature/nova-feature
   ```

5. **Abra um Pull Request**

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo `LICENSE` para mais detalhes.

## Agradecimentos

Agradecemos a todos os contribuidores e à comunidade open source por tornar este projeto possível.
