# SIB — Summit Internacional de Branding

## Visão geral

O **SIB — Summit Internacional de Branding** é um evento internacional voltado a branding, posicionamento, negócios, comportamento e conexões profissionais.

O projeto consistiu na reconstrução completa do site oficial, substituindo uma instalação anterior por uma aplicação moderna, responsiva e preparada para as edições do SIB em diferentes países. O site está publicado em produção e atende participantes, palestrantes, organizadores e pessoas interessadas nas próximas edições.

🌐 [Acessar o site oficial do SIB](https://siboficial.com/japan/)

---

## Objetivo

Modernizar a presença digital do SIB sem reproduzir visualmente o site anterior, criando uma experiência editorial compatível com um evento internacional e, ao mesmo tempo, melhorando desempenho, acessibilidade, indexação e manutenção.

O visitante precisa compreender rapidamente:

- o que é o SIB;
- qual é a próxima edição;
- onde e quando ela acontece;
- quem participa;
- quais ingressos estão disponíveis;
- como realizar a inscrição.

---

## Solução desenvolvida

A aplicação pública foi construída em **Angular**, com uma estrutura orientada ao conceito de edição do evento. Japão e São Paulo não são tratados como páginas isoladas: palestrantes, organizadores, ingressos, patrocinadores e conteúdo são associados às respectivas edições.

O projeto inclui:

- páginas específicas para SIB Japão e SIB São Paulo;
- apresentação institucional e histórico de edições;
- palestrantes e organizadores por edição;
- planos de ingresso em moedas diferentes;
- programação em documento público;
- patrocinadores, depoimentos, galeria e FAQ;
- ações solidárias realizadas nas edições anteriores;
- conteúdo em português, inglês, francês, espanhol e japonês;
- navegação responsiva para mobile, tablet, notebook e desktop.

---

## SEO e renderização

Como o SIB depende de descoberta orgânica, SEO foi tratado como parte da arquitetura, não apenas como preenchimento de palavras-chave.

As páginas são prerenderizadas com HTML completo e possuem:

- título e descrição por rota;
- URL canônica;
- Open Graph e Twitter Cards;
- sitemap e `robots.txt`;
- dados estruturados de organização e evento;
- palestrantes representados como participantes do evento;
- ingressos representados como ofertas;
- datas, local e situação do evento;
- respostas HTTP corretas para páginas, redirecionamentos e URLs inexistentes.

Também foi iniciado o trabalho de migração SEO para que o Google substitua gradualmente URLs residuais da versão antiga do site pelas páginas atuais.

---

## Performance

O site possui forte presença fotográfica, exigindo atenção especial à entrega de imagens e ao caminho crítico de carregamento.

Foram implementados:

- imagens WebP em tamanhos responsivos;
- `srcset` e `sizes` para evitar downloads maiores que a tela;
- prioridade para a imagem principal;
- carregamento tardio de imagens abaixo da dobra;
- dimensões explícitas para reduzir deslocamentos de layout;
- carregamento dos carrosséis somente quando próximos da área visível;
- cache prolongado para arquivos versionados;
- divisão de código para dependências carregadas sob demanda.

Em uma validação mobile realizada durante a entrega, o PageSpeed Insights apresentou:

| Categoria | Resultado observado |
|---|---:|
| Desempenho | 98 |
| Acessibilidade | 96 |
| Práticas recomendadas | 100 |
| SEO | 100 |

Os resultados de ferramentas como PageSpeed podem variar conforme rede, dispositivo, conteúdo e momento do teste.

---

## Analytics e privacidade

O Google Analytics 4 foi integrado respeitando consentimento prévio.

O site apresenta uma escolha clara entre aceitar e recusar. A coleta é habilitada apenas após autorização, e as políticas de segurança do navegador foram ajustadas para permitir somente os endpoints necessários ao funcionamento da medição.

Esse trabalho envolveu:

- carregamento condicional do GA4;
- persistência da preferência do visitante;
- eventos de navegação por página;
- revisão de Content Security Policy;
- validação pelo modo de teste do Google Analytics;
- preservação do desempenho mesmo com a ferramenta ativa.

---

## Infraestrutura e publicação

A entrega em produção utiliza containers e Nginx, com configuração preparada para domínio oficial e HTTPS.

Principais pontos:

- build reproduzível com Docker;
- Nginx servindo páginas prerenderizadas por rota;
- redirecionamento de HTTP para HTTPS;
- domínio canônico sem duplicação entre `www` e endereço principal;
- certificados TLS emitidos e renováveis com Certbot;
- cabeçalhos de segurança;
- política de cache separada para documentos e assets versionados;
- página `404` real para endereços inexistentes.

---

## Stack técnica

- Angular
- TypeScript
- Angular SSR e prerender
- HTML e CSS responsivos
- ngx-translate
- Swiper com carregamento sob demanda
- Vitest
- ESLint
- Docker e Docker Compose
- Nginx
- Certbot e Let's Encrypt
- Google Analytics 4
- Google Search Console

---

## Desafios resolvidos

### Migração de um site anterior

O domínio já possuía histórico no Google. A reconstrução exigiu preservar o endereço oficial enquanto o mecanismo de busca reaprende a nova estrutura, evitando redirecionamentos indiscriminados e páginas falsas.

### SEO em uma aplicação Angular

Uma página exclusivamente renderizada no navegador não seria suficiente para a estratégia do evento. A solução passou a gerar HTML por rota com metadados e conteúdo próprios.

### Imagens editoriais de grande porte

As imagens originais somavam vários megabytes. Foram criadas variantes modernas e responsivas, reduzindo de forma significativa a transferência necessária, especialmente no mobile.

### Eventos internacionais

Datas, localidades, idiomas, moedas, palestrantes e ingressos variam por edição. A interface foi organizada para suportar essas diferenças sem misturar dados de eventos distintos.

### Privacidade e segurança

A integração analítica precisou funcionar apenas após consentimento e dentro de uma Content Security Policy restritiva, sem abrir permissões desnecessárias no navegador.

---

## Competências demonstradas

- Desenvolvimento frontend com Angular e TypeScript
- Renderização no servidor e geração estática
- SEO técnico e dados estruturados
- Migração de domínio e tratamento de URLs legadas
- Otimização de imagens e desempenho web
- Responsividade em diferentes tamanhos de tela
- Acessibilidade e HTML semântico
- Internacionalização
- Analytics orientado a consentimento
- Configuração de Nginx e cabeçalhos de segurança
- Dockerização e publicação em produção
- Certificados HTTPS com Certbot
- Modelagem de conteúdo por edição
- Validação com Lighthouse, PageSpeed e Search Console
- Evolução de um produto real em colaboração com cliente

---

## Evolução planejada

A estrutura atual utiliza dados locais desacoplados dos componentes. Isso prepara o projeto para uma fase futura com API e painel administrativo.

Essa evolução permitirá que a equipe do SIB:

- crie novas edições;
- publique novas rotas;
- cadastre palestrantes e organizadores;
- gerencie ingressos e programação;
- atualize mídia e patrocinadores;
- arquive eventos antigos sem perder seu valor histórico;
- controle redirecionamentos e metadados de SEO.

O painel será uma evolução do produto, não um page builder: o conteúdo poderá ser administrado sem comprometer a identidade visual e a estrutura técnica do site.

---

## Resultado

O SIB passou a ter uma presença digital contemporânea, rápida e preparada para busca orgânica, edições internacionais e evolução administrativa.

O projeto demonstra uma entrega completa: concepção visual, desenvolvimento frontend, SEO técnico, analytics, infraestrutura, segurança, publicação e acompanhamento em produção.

## Link do projeto

🌐 [siboficial.com](https://siboficial.com/japan/)
