# AgroRota Inteligente

Plataforma web colaborativa para monitorar as condições das estradas vicinais de Ariquemes/RO. O sistema reúne relatos da comunidade, localização geográfica, alertas e o **AgroScore**, indicador de 0 a 100 que representa a trafegabilidade das estradas.

## Links do projeto

- **MVP funcional:** [Acessar o AgroRota Inteligente](https://agrorota-dgxaabk9.manus.space/)
- **Protótipo e apresentação:** [Visualizar no Canva](https://canva.link/z1ue2dg3q7pntn3)
- **Pitch:** [Assistir no YouTube](https://youtu.be/OhdQqMau4H8)

## Equipe

- **Equipe:** AgroRota Inteligente
- **Integrantes:** Ane Ludmila, Julia Kristine, Kevin Eugenio e Luan Gabriel
- **Curso:** Tecnologia em Análise e Desenvolvimento de Sistemas — ADS
- **Instituição:** IFRO Campus Ariquemes
- **Categoria:** Desafio Empresa e Comunidade
- **Evento:** Hackathon Extensionista IFRO Ariquemes 2026/1

## Problema

Durante o período chuvoso, estradas rurais podem apresentar lama, alagamentos, buracos, erosões e bloqueios. A falta de informações atualizadas dificulta o planejamento de rotas, o escoamento da produção e a priorização da manutenção.

## Solução proposta

O AgroRota centraliza informações sobre as estradas vicinais e permite:

- consultar a condição das estradas;
- registrar ocorrências com localização, descrição, severidade e foto;
- visualizar relatos e alertas em um mapa;
- acompanhar o AgroScore de cada estrada;
- apoiar produtores, motoristas e gestores públicos na tomada de decisão.

## Principais funcionalidades

- consulta pública de trafegabilidade;
- cadastro e histórico de relatos;
- mapa interativo;
- autenticação e perfis de acesso;
- dashboard com indicadores;
- alertas de risco;
- cálculo do AgroScore;
- interface responsiva para computador e celular.

## AgroScore

O AgroScore varia de **0 a 100**:

| Pontuação | Situação |
|---|---|
| 70 a 100 | Trafegável |
| 40 a 69 | Atenção |
| 0 a 39 | Intransitável |

Na implementação atual, o cálculo considera:

- **60%:** relatos recentes;
- **30%:** dados climáticos;
- **10%:** tendência histórica.

## Como usar

1. Acesse o [MVP online](https://agrorota-dgxaabk9.manus.space/).
2. Utilize a consulta pública para pesquisar uma estrada.
3. Verifique o AgroScore, o status e os alertas disponíveis.
4. Para registrar um relato, faça login e selecione o perfil **Produtor Rural**.
5. Gestores podem acessar o dashboard para acompanhar ocorrências e trechos críticos.

## Como executar localmente

### Pré-requisitos

- Node.js 20 ou superior;
- pnpm;
- banco de dados MySQL ou compatível;
- credenciais dos serviços utilizados pelo projeto.

### Instalação

```bash
pnpm install
pnpm db:push
pnpm dev
```

A aplicação ficará disponível, normalmente, em:

```text
http://localhost:3000
```

As variáveis de ambiente devem ser configuradas em um arquivo `.env`. Senhas, tokens e chaves de API não devem ser publicados no GitHub.

## Testes

```bash
pnpm check
pnpm test
```

Também devem ser verificados manualmente:

- consulta de uma estrada existente e inexistente;
- cadastro de relato com campos válidos e inválidos;
- acesso às páginas protegidas;
- permissões dos diferentes perfis;
- funcionamento em computador e celular.

## Testes e Validação

Foram realizados testes funcionais nas principais funcionalidades do AgroRota Inteligente, verificando o correto funcionamento dos fluxos essenciais do sistema.

### Funcionalidades testadas

- Consulta pública de trafegabilidade;
- Cadastro de relatos comunitários;
- Autenticação e controle de acesso;
- MFA (autenticação em dois fatores) com envio simulado de código por SMS;
- Dashboard e visualização de indicadores;
- Cálculo do AgroScore.

### Cenários verificados

- Consulta de estrada existente e inexistente;
- Cadastro de relato com dados válidos e inválidos;
- Login com credenciais válidas e inválidas;
- Validação do código MFA enviado por SMS simulado;
- Acesso às páginas protegidas;
- Permissões dos diferentes perfis de usuário;
- Funcionamento em computador e dispositivos móveis.

### Evidências

As evidências dos testes são registradas por meio de capturas de tela, vídeos demonstrativos e registros das funcionalidades avaliadas.

### Validação com usuários

A validação formal com usuários finais ainda não foi realizada. Como etapa futura, o sistema será apresentado a produtores rurais, motoristas e gestores públicos para coleta de feedback e identificação de melhorias.

## Tecnologias utilizadas

### Frontend

- React;
- TypeScript;
- Vite;
- Tailwind CSS;
- shadcn/ui;
- TanStack React Query.

### Backend e banco de dados

- Node.js;
- Express;
- tRPC;
- MySQL ou TiDB;
- Drizzle ORM;
- Zod.

### Serviços e ferramentas

- Google Maps;
- Manus OAuth;
- armazenamento compatível com S3;
- Vitest;
- Git e GitHub;
- Canva.

## Inteligência artificial

### Manus AI

Utilizada na criação da estrutura inicial da aplicação, geração de componentes, integrações, prototipação e apoio à implementação.

### ChatGPT

Utilizado na revisão da documentação, organização do README, descrição do problema e da solução e apoio na elaboração de testes.

A inteligência artificial foi usada como ferramenta de apoio. As informações e decisões do sistema devem ser revisadas por pessoas responsáveis.

## Estado atual

O MVP possui autenticação, consulta de estradas, cadastro de relatos, dashboard, mapa, alertas e cálculo do AgroScore.

Algumas funcionalidades ainda podem ser ampliadas, como:

- integração com dados meteorológicos reais;
- upload definitivo de fotos;
- notificações automáticas;
- moderação dos relatos;
- ampliação dos testes automatizados.

## Licença e uso do código

O projeto utiliza a licença **MIT**, permitindo estudo, modificação e distribuição conforme os termos da licença.

O AgroRota foi desenvolvido para fins acadêmicos. Antes de um uso oficial, devem ser revisados segurança, privacidade, qualidade dos dados, disponibilidade dos serviços e conformidade com a LGPD.

---

Desenvolvido para apoiar a mobilidade rural, o escoamento da produção e o planejamento da manutenção das estradas vicinais de Ariquemes/RO.
