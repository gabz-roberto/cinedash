# Arquitetura do CineDash

## Geral

O **CineDash** é um projeto pessoal desenvolvido com o objetivo de experimentar novas arquiteturas de software e explorar diferentes estratégias de estilização de componentes. 

Para a organização do código, utilizei uma abordagem modular inspirada nos conceitos de Feature-Sliced Design (FSD). O foco principal foi testar na prática a separação rigorosa de responsabilidades da aplicação, garantindo que regras de negócio, componentes visuais, consumo de API e gerenciamento de estado não ficassem acoplados.

A estrutura foi organizada nas seguintes camadas:

- `app`: Configurações globais, provedores e rotas.
- `pages`: Páginas da aplicação que compõem as telas principais.
- `widgets`: Blocos autônomos de UI que combinam features e entidades.
- `features`: Funcionalidades práticas focadas no usuário (ex: busca, filtros, autenticação).
- `entities`: Domínio do negócio e modelos principais (ex: filmes, gêneros).
- `shared`: Recursos reutilizáveis, utilitários, hooks, chamadas de API e design system base.

Por se tratar de um ambiente de testes e aprendizado, o Feature-Sliced Design não foi aplicado de forma rígida. A estrutura foi adaptada para manter o projeto pragmático, priorizando a legibilidade, facilidade de manutenção e flexibilidade no desenvolvimento dos componentes.

---

## Estrutura do projeto

```text
src/
├── app/
│   ├── providers/
│   └── router/
│
├── components/
│   └── ui/
│
├── entities/
│   ├── genre/
│   └── movie/
│
├── features/
│   ├── auth/
│   ├── movie-filters/
│   ├── movie-pagination/
│   ├── movie-search/
│   ├── theme/
│   └── watchlist/
│
├── pages/
│   ├── discover/
│   ├── login/
│   ├── movie-details/
│   └── watchlist/
│
├── shared/
│   ├── api/
│   ├── config/
│   ├── hooks/
│   ├── lib/
│   └── types/
│
├── test/
│
└── widgets/
    ├── app-shell/
    └── movie-grid/
```

> **P.S.:** A aplicação foi construída para fins de estudo e experimentação — alimentada por código, café e muito punk rock tocando ao fundo.