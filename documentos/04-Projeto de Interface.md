# Projeto de Interface


## User Flow

O fluxograma apresentado na figura 1 mostra o fluxo de interação do usuário pelas telas do sistema. Cada uma das telas deste fluxo é detalhada na seção de Protótipo de baixa fidelidade que se segue.

<figure>
  <img src="img/userflow-fulldev.png" alt="Fluxo de telas do usuário">
  <figcaption>Figura 1 - Fluxo de telas do usuário</figcaption>
</figure>


## Protótipo de baixa fidelidade

As telas do sistema apresentam uma estrutura comum que é apresentada na figura 2. Nesta estrutura existem 3 grandes blocos, descritos a seguir. São eles:
<ul>
  <li>Cabeçalho - local onde estão dispostos o logotipo da plataforma FullDev Online, a barra de busca global e o menu de navegação principal (Feed, Marcas, Notificações, Perfil);</li>
  <li>Conteúdo - apresenta o conteúdo da tela em questão, variando conforme a funcionalidade acessada;</li>
  <li>Rodapé - apresenta informações sobre os direitos autorais e links institucionais.</li>
</ul>

<figure>
  <img src="img/estrutura-padrao.png" alt="Estrutura padrão do site">
  <figcaption>Figura 2 - Estrutura padrão do site</figcaption>
</figure>
<hr>

<h3><b>Tela - Home Page / Feed</b></h3>
<p>A tela principal exibe o feed de publicações ordenado por score (hype, likes, comentários, recência e afinidade de stack). Apresenta seção de "Destaques", filtros laterais por stack e senioridade, e um botão de "Nova Avaliação" para usuários autenticados.</p>

<figure>
  <img src="img/tela-feed.png" alt="Tela do Feed">
  <figcaption>Figura 3 - Tela de Feed / Home Page</figcaption>
</figure>
<hr>

<h3><b>Tela - Detalhe da Publicação</b></h3>
<p>A tela de detalhe apresenta o header da publicação (imagem, título, nota geral, autor com link para LinkedIn), o corpo completo da avaliação (dificuldade, didática, usabilidade, custo-benefício, tempo de uso, stack), os indicadores de interação (likes, dislikes, hype), o bloco de resposta oficial da marca (quando existente) e a seção de comentários.</p>

<figure>
  <img src="img/tela-detalhe.png" alt="Tela de Detalhe da Publicação">
  <figcaption>Figura 4 - Tela de Detalhe da Publicação</figcaption>
</figure>
<hr>

<h3><b>Tela - Nova Avaliação</b></h3>
<p>A tela de criação de avaliação apresenta os seguintes campos: Título, Curso/Plataforma, Imagem, Senioridade (radio), Dificuldade (1–5), Didática (texto), Usabilidade (texto), Custo-Benefício (texto), Facilidade de Pagamento (rating 1–5), Tempo de Uso (texto), Nota Geral (1–5), Stack (select) e Justificativa (texto). Acessível apenas a usuários autenticados com CPF e LinkedIn validados.</p>

<figure>
  <img src="img/tela-nova-avaliacao.png" alt="Tela de Nova Avaliação">
  <figcaption>Figura 5 - Tela de criação de nova avaliação</figcaption>
</figure>
<hr>

<h3><b>Tela – Cadastro</b></h3>
<p>A tela de cadastro apresenta os seguintes campos: Nome Completo, E-mail, CPF, Senha e Confirmação de Senha. Após o cadastro, o usuário é redirecionado para o onboarding de perfil (LinkedIn, stack e senioridade).</p>

<figure>
  <img src="img/tela-cadastro.png" alt="Tela de Cadastro">
  <figcaption>Figura 6 - Tela de cadastro de usuários</figcaption>
</figure>
<hr>

<h3><b>Tela – Login</b></h3>
<p>A tela de login apresenta campos para inserção de e-mail e senha, com link para recuperação de senha e opção de manter-se logado.</p>

<figure>
  <img src="img/tela-login.png" alt="Tela de Login">
  <figcaption>Figura 7 - Tela de acesso à conta do usuário</figcaption>
</figure>
<hr>

<h3><b>Tela – Perfil do Usuário</b></h3>
<p>A tela de perfil apresenta as informações públicas do usuário (avatar, nome, @username, bio, localidade, stack, senioridade, LinkedIn), suas publicações e estatísticas de interação, além de opções de edição e configurações de privacidade.</p>

<figure>
  <img src="img/tela-perfil.png" alt="Tela de Perfil do Usuário">
  <figcaption>Figura 8 - Tela de Perfil do usuário</figcaption>
</figure>
<hr>

<h3><b>Tela – Painel da Marca</b></h3>
<p>A tela de painel da marca apresenta a listagem de publicações que mencionam a marca, métricas de desempenho (volume de avaliações, média de notas, hype por período), opção de responder oficialmente às avaliações e botão de exportação em CSV.</p>

<figure>
  <img src="img/tela-painel-marca.png" alt="Tela do Painel da Marca">
  <figcaption>Figura 9 - Tela do Painel da Marca</figcaption>
</figure>
<hr>

<h3><b>Tela – Painel do Moderador</b></h3>
<p>A tela do moderador apresenta contadores de publicações pendentes (últimos 7 e 30 dias), fila de publicações aguardando revisão (título, autor, stack, data, flags), ações de Aprovar/Recusar/Editar/Visualizar, aprovação em lote, fila de denúncias, gestão de vínculos de marca e logs de auditoria.</p>

<figure>
  <img src="img/tela-moderador.png" alt="Tela do Painel do Moderador">
  <figcaption>Figura 10 - Tela do Painel do Moderador</figcaption>
</figure>
