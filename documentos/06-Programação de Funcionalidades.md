# Programação de Funcionalidades

Nesta seção são apresentadas as funcionalidades implementadas que atendem aos requisitos funcionais do projeto FullDev Online — Indicador de Cursos. Para cada requisito, são indicados os artefatos da solução e as instruções de acesso.

## Tela de Cadastro e Login (RF-01, RF-02, RF-03, RF-04)

A tela de cadastro permite ao usuário criar sua conta informando nome, e-mail, CPF e senha. Após o cadastro, é realizada a verificação de e-mail e o onboarding para vinculação do LinkedIn e preenchimento do perfil.

**Requisitos atendidos:** RF-01, RF-02, RF-03, RF-04

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Página de Cadastro | [codigo-fonte/pagina-cadastro/](../codigo-fonte/) |
|02| Página de Login | [codigo-fonte/pagina-login/](../codigo-fonte/) |
|03| Script de Validação CPF | [codigo-fonte/scripts/validacao-cpf.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Abra o navegador e acesse a URL da plataforma;</li>
  <li>Clique em "Criar conta";</li>
  <li>Preencha os campos Nome, E-mail, CPF, Senha e Confirmação de Senha;</li>
  <li>Confirme o e-mail recebido na caixa de entrada;</li>
  <li>Complete o onboarding informando URL do LinkedIn, stack principal e senioridade.</li>
</ul>

---

## Feed de Publicações e Busca (RF-14, RF-17, RF-18)

O feed exibe as avaliações ordenadas por score (combinação de hype, likes, comentários, recência e afinidade de stack). A busca global permite localizar publicações por título, curso, instituição e stack.

**Requisitos atendidos:** RF-14, RF-17, RF-18

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Página do Feed | [codigo-fonte/pagina-feed/](../codigo-fonte/) |
|02| Componente de Filtros | [codigo-fonte/componentes/filtros.js](../codigo-fonte/) |
|03| Script de Busca | [codigo-fonte/scripts/busca-global.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Acesse a URL principal da plataforma;</li>
  <li>Visualize o feed de publicações na área central;</li>
  <li>Utilize a barra de busca no cabeçalho para buscar por palavra-chave;</li>
  <li>Aplique filtros pelo painel lateral (stack, senioridade, nota, hype, recência).</li>
</ul>

---

## Publicação de Avaliação (RF-11, RF-12, RF-13)

O formulário de avaliação permite ao usuário registrar sua experiência com um curso. Após o envio, a publicação passa pelo fluxo de moderação: filtro automático de palavras proibidas e revisão humana pelo moderador.

**Requisitos atendidos:** RF-11, RF-12, RF-13

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Formulário de Avaliação | [codigo-fonte/pagina-avaliacao/](../codigo-fonte/) |
|02| Filtro Automático | [codigo-fonte/scripts/filtro-moderacao.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Faça login com uma conta que possua CPF e LinkedIn validados;</li>
  <li>Clique em "Nova Avaliação";</li>
  <li>Preencha todos os campos obrigatórios do formulário;</li>
  <li>Clique em "Enviar para revisão";</li>
  <li>Acompanhe o status da publicação no seu perfil (Em revisão / Aprovado / Recusado).</li>
</ul>

---

## Interações: Likes, Dislikes, Hype e Comentários (RF-15, RF-16)

Os usuários autenticados podem interagir com as publicações aprovadas por meio de likes, dislikes, hype (foguinho) e comentários. Cada usuário tem direito a 1 voto por item e 1 hype por post por dia.

**Requisitos atendidos:** RF-15, RF-16

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Componente de Interações | [codigo-fonte/componentes/interacoes.js](../codigo-fonte/) |
|02| Componente de Comentários | [codigo-fonte/componentes/comentarios.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Acesse o detalhe de uma publicação;</li>
  <li>Clique em 👍 ou 👎 para registrar seu voto (clique novamente para alternar ou remover);</li>
  <li>Clique no foguinho 🔥 para dar Hype;</li>
  <li>Utilize o campo de texto abaixo da publicação para comentar.</li>
</ul>

---

## Painel da Marca (RF-08, RF-09, RF-10, RF-20)

O painel da marca permite que representantes verificados de instituições respondam oficialmente às avaliações, visualizem métricas de desempenho e exportem relatórios.

**Requisitos atendidos:** RF-08, RF-09, RF-10, RF-20

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Página do Painel da Marca | [codigo-fonte/painel-marca/](../codigo-fonte/) |
|02| Componente de Resposta Oficial | [codigo-fonte/componentes/resposta-marca.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Acesse a plataforma com uma conta vinculada e aprovada como Atendente ou Administrador de marca;</li>
  <li>Navegue até "Painel da Marca" no menu;</li>
  <li>Visualize as publicações que mencionam sua marca;</li>
  <li>Clique em "Responder oficialmente" para publicar uma resposta com selo de verificação;</li>
  <li>Acesse as métricas e exporte o relatório em CSV.</li>
</ul>

---

## Painel do Moderador (RF-21, RF-22, RF-23)

O painel do moderador fornece ferramentas para aprovação/recusa de publicações, gestão de denúncias, vínculos de marca e acesso a logs de auditoria.

**Requisitos atendidos:** RF-21, RF-22, RF-23

**Artefatos da funcionalidade:**

|ID | Artefato | Link |
|---|----------|------|
|01| Página do Painel do Moderador | [codigo-fonte/painel-moderador/](../codigo-fonte/) |
|02| Componente de Fila de Moderação | [codigo-fonte/componentes/fila-moderacao.js](../codigo-fonte/) |

**Instruções de acesso:**
<ul>
  <li>Acesse a plataforma com uma conta com perfil de Moderador;</li>
  <li>Navegue até "Painel do Moderador";</li>
  <li>Revise as publicações na fila (título, autor, stack, data, flags);</li>
  <li>Clique em "Aprovar" ou "Recusar" (com motivo obrigatório em caso de recusa);</li>
  <li>Gerencie a fila de denúncias e os logs de auditoria nas abas correspondentes.</li>
</ul>
