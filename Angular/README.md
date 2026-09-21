# Conhecimentos em Angular

Durante os estudos de Angular, desenvolvi uma aplicação de loja utilizando uma arquitetura organizada e evoluindo gradualmente desde os fundamentos até conceitos mais avançados.

## Fundamentos do Angular

- Componentes Standalone
- Interpolação
- Property Binding
- Event Binding
- Two-Way Binding
- Diretivas e controle de fluxo com `@if` e `@for`
- `ngModel`
- Comunicação entre componentes
- `@Input`
- `@Output`
- Componentização e reutilização de componentes

## Services e Injeção de Dependências

- Criação e utilização de Services
- `providedIn: 'root'`
- Injeção de dependências
- Separação entre componente, service e armazenamento
- Services para regras de negócio
- Organização por funcionalidades (`features`)

## Signals e Gerenciamento de Estado

- `signal`
- `computed`
- `effect`
- `update`
- Estado somente leitura com Signals
- Stores utilizando Signals
- Separação entre Store, Service e componentes
- Persistência de estado utilizando `localStorage`
- Restauração do estado através de `hydrate`
- Atualização reativa da interface

## Carrinho e Estado Global

Desenvolvimento de um carrinho utilizando Signals, incluindo:

- Adicionar produto
- Aumentar quantidade
- Diminuir quantidade
- Remover produto
- Limpar carrinho
- Cálculo reativo do total
- Persistência no `localStorage`
- Separação entre `CarrinhoStore` e `CarrinhoService`

## Routing

- Angular Router
- Rotas Standalone
- Rotas organizadas por feature
- Parâmetros de rota
- Rotas de criação e edição
- `RouterLink`
- Navegação programática com `Router`
- Lazy Loading
- Organização através de arquivos de rotas específicos

## Guards

Implementação e utilização de Guards:

- `CanActivate`
- Guard de autenticação
- Guard de autorização por perfil
- `CanDeactivate`
- Proteção contra saída de formulário com alterações não salvas

## Resolvers

- Utilização de `Resolve`
- Carregamento de dados antes da criação da página
- Recuperação dos dados através de `ActivatedRoute`
- Integração entre Resolver, Service e Store

## Formulários

Estudo de formulários Angular, principalmente Reactive Forms:

- `FormGroup`
- Controles de formulário
- `formControlName`
- Validações
- `form.invalid`
- `markAllAsTouched`
- `dirty`
- `pristine`
- `getRawValue`
- Formulários reutilizados para criação e edição
- Página própria para criação de produtos
- Página própria para edição de produtos
- `ngSubmit`
- Controle de alterações não salvas

## Arquitetura da aplicação

Organização da aplicação utilizando uma estrutura baseada em responsabilidades:

```text
core/
├── guards/
├── interceptors/
└── ...

shared/
├── components/
└── styles/

features/
├── auth/
├── produtos/
└── ...

```

Aplicação dos conceitos de:

- Separação de responsabilidades
- Componentes focados na apresentação
- Services para regras de negócio
- Stores para gerenciamento de estado
- Guards para proteção de rotas
- Resolvers para carregamento de dados
- Features organizadas por domínio

## Autenticação

Implementação de uma estrutura de autenticação utilizando:

- `AuthStore`
- `AuthService`
- Access Token
- Refresh Token
- Usuário autenticado
- Persistência da sessão
- `hydrate`
- Estado `isLoggedIn`
- Controle de acesso baseado em perfil
- Guards de autenticação e autorização
- Interceptor para utilização do token nas requisições

## HTTP e API

Estudo da integração com APIs utilizando:

- `HttpClient`
- Requisições HTTP
- `GET`
- `POST`
- `PUT`
- `DELETE`
- Observables
- `subscribe`
- `tap`
- Integração entre API, Service e Store
- Atualização do estado após operações de criação, atualização e exclusão

A implementação também foi estudada inicialmente sem backend, utilizando métodos locais para simular as operações e facilitar o entendimento do fluxo.

## RxJS

- `Observable`
- `subscribe`
- Operadores RxJS
- `map`
- `tap`
- `debounceTime`
- Integração entre Observables e estado da aplicação
- Tratamento do fluxo assíncrono

## Interceptors

Estudo de Interceptors para:

- Adicionar token de autenticação às requisições
- Centralizar comportamento das requisições HTTP
- Trabalhar com autenticação e renovação de token

## Loading e tratamento de estado

Utilização de estado para representar:

- Loading
- Erros
- Dados carregados
- Estado vazio

Exemplo:

```ts
loading()
error()
produtos()
```

Também foi estudada a utilização de `effect` e Signals para manter estados sincronizados.

## CRUD

Desenvolvimento de um CRUD de produtos envolvendo:

- Listagem
- Cadastro
- Edição
- Exclusão
- Atualização do Store
- Formulário reutilizado para criação e edição
- Navegação entre páginas
- Resolver para carregamento do produto
- Controle de alterações não salvas

## CSS e Design System

Desenvolvimento de uma base de estilos reutilizável para a aplicação:

- Variáveis CSS
- Tema global
- Reset CSS
- Layout responsivo
- Flexbox
- CSS Grid
- Navbar
- Botões reutilizáveis
- Cards
- Formulários
- Tabelas
- Loading
- Skeleton
- Alertas
- Badges
- Estados de foco
- Animações
- Responsividade para desktop, tablet e mobile

Organização dos estilos:

```text
shared/styles/
├── theme.css
├── layout.css
├── navbar.css
├── buttons.css
├── cards.css
├── forms.css
├── tables.css
└── utilities.css
```

## Projeto prático

Todos esses conceitos foram aplicados em uma aplicação de loja, utilizando produtos, carrinho, autenticação e área administrativa como domínio de estudo.

O projeto foi desenvolvido de forma incremental, evoluindo de componentes simples para uma arquitetura com:

```text
Componentes
     ↓
Services
     ↓
Stores
     ↓
Signals
     ↓
HTTP / API
     ↓
Guards / Resolvers / Interceptors
```

O objetivo do projeto foi compreender não apenas a sintaxe do Angular, mas também como organizar uma aplicação Angular de forma modular, reutilizável e preparada para crescer.
