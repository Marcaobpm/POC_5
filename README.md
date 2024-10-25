This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/pages/api-reference/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/pages/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn-pages-router) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/pages/building-your-application/deploying) for more details.

## Explicação CSS

Estrutura Geral

1. Variáveis Globais: Usa variáveis CSS no :root para definir as cores padrão e estilos globais, como --background (cor de fundo) e --foreground (cor do texto). A presença do prefers-color-scheme permite a troca automática entre cores claras e escuras, respeitando a preferência do usuário.

2. Reset Básico: Elementos html, body, e * garantem que o conteúdo ocupe a largura da tela (max-width: 100vw) e evite problemas de overflow horizontal.

3. Definições Globais: Tipos de letra e suavização são aplicados ao body para garantir que todo o texto e aparência visual sejam consistentes.

Módulos Específicos

1. .page
Definição de cores adicionais: Define algumas cores para fundos e efeitos (--gray-alpha-100 e --gray-alpha-200), ajustando-as com transparência (rgba) e valores diferentes para o tema claro e escuro.
Grid Layout: Estabelece uma estrutura de página em três linhas (grid-template-rows), centrando conteúdo horizontal e verticalmente.
2. .main
Conteúdo Principal: Define uma lista ordenada ol e um estilo específico para códigos, melhorando a leitura e enfatizando os textos técnicos.
3. .ctas
Botões de Ação (CTAs): Configura botões para navegação e ação (a.primary, a.secondary) com transições suaves e cores que mudam no hover, usando variáveis para facilitar a manutenção.
4. .footer
Rodapé: Exibe links com espaçamento específico e um efeito de sublinhado ao passar o mouse, ajustado para dispositivos com hover habilitado.
5. Responsividade
Em Telas Pequenas: Ajusta o layout com padding reduzido na .page, alinhamento centralizado para a .main ol, e botões de chamada de ação em coluna, tornando o layout mais compacto.
Hover Condicional: Aplicado apenas em dispositivos não-touch, melhora a experiência em desktops sem comprometer a responsividade.

## Componentes simples JS

Como Criar um Componente Simples (Sem Estado)
1. Função JavaScript: Um componente funcional é, basicamente, uma função JavaScript que recebe um parâmetro props.

2. Retorno do JSX: Retorna o JSX que descreve a UI que será exibida.

3. Props como Argumentos: As props são passadas como argumento e permitem que o componente receba dados dinâmicos para renderizar.

Vantagens dos Componentes Simples
1. Desempenho: Como não mantêm um estado interno, são mais leves e rápidos.

2. Reutilização e Modularidade: São ideais para elementos de UI reutilizáveis e pequenos.

3. Legibilidade e Manutenção: Como possuem menos lógica, são mais fáceis de entender e manter.

   Quando Usar Componentes Sem Estado
Esses componentes são ideais quando:

Você só precisa renderizar uma interface com base nas props sem alterar o conteúdo dinamicamente.

Não há necessidade de interações complexas, como gerenciamento de estado ou ciclo de vida do componente.

Componentes simples são essenciais para dividir interfaces complexas em partes menores e modulares, garantindo uma arquitetura de código mais limpa e fácil de manter.

## Estrutura de Projeto NextJS 14 ou superior

# Estrutura de Pastas Padrão
/app (pasta raiz dos componentes)

A app agora é a base para roteamento e renderização. Cada subpasta representa uma rota, e os arquivos dentro das rotas podem incluir componentes, layouts e lógica de renderização.
/components

Para armazenar componentes reutilizáveis e isolados, como botões, cards e headers.
Exemplo: Um componente Button.js que será usado em várias páginas.
/public

Armazena arquivos estáticos, como imagens, fontes e outros assets. Esses arquivos podem ser acessados diretamente via URL.
Exemplo: Acessando uma imagem logo.png armazenada em public/logo.png com "/logo.png".
/styles

Pasta para arquivos de estilos globais e módulos CSS específicos de componentes.
Arquivo comum: globals.css, onde se define o estilo básico da aplicação.
/lib

Destinada a lógica auxiliar e funções utilitárias, como hooks, constantes, e funções de manipulação de dados que podem ser usadas em diversas partes da aplicação.
/api

Next.js permite construir uma API interna na pasta api sob a app/ (ou pages/api se estiver usando o Pages Router), com rotas que criam endpoints diretamente para lógica back-end.
Exemplo: app/api/posts/route.js cria um endpoint em /api/posts.
/middleware.js

Arquivo opcional para middlewares que controlam requisições, geralmente usado para autenticação e redirecionamento.

# Estrutura Interna da app/
1. page.js
Este é o arquivo principal para uma rota específica, ou seja, renderiza a UI que o usuário vê quando acessa uma rota.

2. layout.js
Define o layout compartilhado entre páginas e sub-rotas, como cabeçalhos e rodapés.
Uma vez definido, aplica-se automaticamente a todas as rotas na subpasta onde está.

3. loading.js
Exibe um indicador de carregamento enquanto os dados da página estão sendo carregados. Esse arquivo é opcional e melhora a experiência do usuário ao fornecer feedback visual.

4. error.js
Arquivo opcional para lidar com erros específicos daquela rota, possibilitando customizar a mensagem de erro que o usuário verá.

5. Rotas Dinâmicas ([slug])
Roteamento dinâmico é feito criando pastas com nome entre colchetes ([slug]). Essas rotas podem capturar valores dinâmicos diretamente da URL.
Exemplo: app/blog/[slug]/page.js renderiza uma página específica de blog com um slug passado na URL.

# Estrutura de Código e Renderização
React Server Components (RSC)

Por padrão, o Next.js 13/14 utiliza React Server Components no App Router, o que melhora a performance ao renderizar componentes no servidor. Isso permite que a aplicação busque dados no servidor sem necessidade de estado ou efeitos client-side.
Streaming e Suspense

Com suporte ao streaming e ao Suspense, o Next.js permite que a página comece a renderizar parcialmente antes de todos os dados serem carregados, melhorando o tempo de resposta percebido pelo usuário.
Data Fetching e Cache

A nova estrutura simplifica a busca de dados com métodos como fetch, que pode ser usado diretamente em componentes, com controle de cache e revalidação.

# Como Iniciar com o Next.js 14 e Estruturar o Projeto

1. Para iniciar e criar um projeto com essa estrutura: npx create-next-app@latest my-next-app
2. Adicione Rotas e Componentes: Estruture suas rotas dentro da app/ e crie subpastas para organizar as diferentes partes do seu projeto, seguindo a estrutura modularizada.
3. Configure o Roteamento Dinâmico: Adicione pastas com [slug] para criar páginas dinâmicas.
4. Desenvolva Componentes Reutilizáveis: Coloque componentes na pasta components/, criando uma estrutura limpa e reutilizável.

Esse novo modelo de estrutura em Next.js 14 permite um fluxo de desenvolvimento mais rápido e otimizado, especialmente em grandes aplicações onde a modularidade e a performance são prioridades.

´´´
import Greeting from './Greeting';

function App() {
  return (
    <div>
      <Greeting name="Alice" />
      <Greeting name="Bob" />
    </div>
  );
}

export default App;
´´´

