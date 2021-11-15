# ANOTAÇÕES DA AULA:
# Práticas avançadas em projetos com ReactJS

AULA 01

1. Ciclo de Vida
=> Inicialização => Montagem => Atualização => Desmontagem

2. Criando o projeto:
npx create-react-app <nome do projeto>

3. Ciclos
- componentDidMount
- componentDidUpdate
- componentWillUpdate
- shouldComponentUpdate

4. Hooks
Nova forma de escrever o React. Permite usar state e outros recursos sem escrever uma classe.
- Não use Hooks dentro de funções JS comuns;
- Chamar Hooks em componentes React;
- Chamar Hooks dentro de Hooks customizados.

5. Context API

AULA 02

1. Fragments: Um padrão comum no React é que um componente pode retornar múltiplos elementos.
Os Fragmentos permitem agrupar uma lista de filhos sem adicionar nós extras ao DOM.

2. Error boundary: resolver problema onde um erro de JS em parte da UI quebrava toda a aplicação.

3. Error boundary não capturam erros em:
- Manipuladoes de evento;
- Código assíncrono (ex. callbacks de setTimeout ou requestAnimationFrame);
- Renderização no servidor;
- Erros lancados na própria error boundary (ao invés de seus filhos).


4. Render Props
O termo "render prop" é uma técnica de compartilhar código entre componentes React passando uma prop cujo valor é uma função.
O componente com uma render prop recebe uma função que retorna um elemento React e a invoca no momento de renderização,
não sendo necessário para o componente implementar uma lógica própria.

5. Typechecking com PropTypes
Na medida em que sua aplicação cresce, você pode capturar muitos bugs com checagem de tipos.
Em algumas aplicações, você pode usar extensões do JavaScript como Flow ou TypeScript para checar os tipos de toda a sua aplicação.
Porém, mesmo se você não usá-las, React possui algumas habilidades de checagem de tipos nativas.

6. Refs e DOM
Com Refs é possível acessar a árvore do DOM e/ou elementos do React.
Quando utilizar:
- Manipulação de bibliotecas de terceiros
- Gerenciamento de inputs (foco), seleção de textos ou reprodução de mídias
- Animações imperativas

AULA 03

1. Dumb Components:

- Preocupa-se com a apresentação;
- Recebem valores via props;
- Não possuem dependências com o restante da aplicação;
- Não especificam como os dados são carregados ou sofrem mutação;
- Recebem valores e callbacks exclusivamente via props;
- Raramente possuem estado, quando precisam de estado é para controlar a interface e não os dados do usuário;
- São escritos na maioria das vezes como componentes funcionais.

Exemplos: Button, Card, Sidebar, Footer, List, Menu

2. Smart Components:

- Preocupam-se como as coisas vão funcionar;
- Podem conter Smart e Dumb components;
- Providenciam dados e padrões de apresentação ou outros containers;
- Na maioria dos casos possuem estado e podem chamar outros fluxos do sistema.

Exemplos: UserGallery, UserPage, FilterBook, FollowersSidebar, ListCards

3. Organização de Projeto
- assets => imgs / styles
- commons => constants (menu, footer, etc) / utils (utilitários)
- components => dumb e smart components (Button, Form, etc)
- containers
- resources => API
- routes
  
Links das Aulas:

## Aula 01
- [Ciclo de Vida](./life-cycle)
- [Hooks](./hooks)
- [Context API](./context-api)

## Aula 02
- [Fragmentos](./fragments)
- [Error Boundary](./error-boundaries)
- [Render Props](./render-props)
- [Type Checking](./type-checking)
- [Refs DOM](./refs-dom)

## Aula 03 
- [Dumb Components](./dumb-components)
- [Smart Components](./smart-components)
- [Estrutura de projeto](./structure-project)
