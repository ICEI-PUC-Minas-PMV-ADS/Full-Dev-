# Especificações do Projeto

## Perfis de Usuários

<table>
<tbody>
<tr>
<th colspan="2">Perfil 1: Usuário Autenticado</th>
</tr>
<tr>
<td width="150px"><b>Descrição</b></td>
<td width="600px">
Estudante ou profissional da área de Tecnologia da Informação, cadastrado na plataforma com CPF e LinkedIn verificados.
</td>
</tr>
<tr>
<td><b>Necessidades</b></td>
<td>
1. Acessar avaliações confiáveis e verificadas de cursos, faculdades e plataformas de ensino;<br>
2. Publicar avaliações com critérios padronizados (didática, dificuldade, custo-benefício, aplicabilidade prática);<br>
3. Filtrar cursos por stack tecnológica, senioridade e nota;<br>
4. Interagir com publicações por meio de likes, dislikes, hype e comentários;<br>
5. Salvar e favoritar cursos de interesse para consulta posterior;<br>
6. Realizar questionário vocacional para identificar áreas de interesse.
</td>
</tr>
</tbody>
</table>

<table>
<tbody>
<tr>
<th colspan="2">Perfil 2: Marca (Atendente / Administrador)</th>
</tr>
<tr>
<td width="150px"><b>Descrição</b></td>
<td width="600px">
Representante oficial de uma instituição de ensino ou plataforma de cursos, vinculado à marca por CNPJ verificado.
</td>
</tr>
<tr>
<td><b>Necessidades</b></td>
<td>
1. Responder oficialmente às avaliações publicadas sobre sua instituição;<br>
2. Monitorar métricas da marca (volume de publicações, média de notas, hype por período);<br>
3. Exportar relatórios de desempenho em CSV;<br>
4. Identificar tendências nas avaliações para melhoria contínua dos serviços.
</td>
</tr>
</tbody>
</table>

<table>
<tbody>
<tr>
<th colspan="2">Perfil 3: Moderador</th>
</tr>
<tr>
<td width="150px"><b>Descrição</b></td>
<td width="600px">
Usuário interno da plataforma responsável por garantir a integridade e qualidade do conteúdo publicado.
</td>
</tr>
<tr>
<td><b>Necessidades</b></td>
<td>
1. Aprovar ou recusar publicações com motivo obrigatório;<br>
2. Remover conteúdo denunciado (posts, comentários e respostas de marca);<br>
3. Gerenciar vínculos entre usuários e marcas;<br>
4. Acessar logs de auditoria e fila de denúncias.
</td>
</tr>
</tbody>
</table>


## Histórias de Usuários

Com base na análise dos perfis de usuários, foram identificadas as seguintes histórias de usuários:

|EU COMO... `PERSONA`| QUERO/PRECISO ... `FUNCIONALIDADE` |PARA ... `MOTIVO/VALOR` |
|--------------------|-------------------------------------|------------------------|
|Usuário autenticado | criar uma conta na plataforma com CPF verificado | garantir que minha identidade seja validada e que minhas avaliações sejam confiáveis. |
|Usuário autenticado | publicar uma avaliação de um curso com critérios padronizados (didática, dificuldade, custo-benefício) | ajudar outros profissionais de TI a tomarem decisões mais informadas sobre sua formação. |
|Usuário autenticado | filtrar cursos por stack tecnológica e nível de senioridade | encontrar rapidamente avaliações relevantes para meu perfil e momento de carreira. |
|Usuário autenticado | dar like, dislike e hype em publicações | expressar minha concordância com avaliações e aumentar a visibilidade de conteúdos relevantes. |
|Usuário autenticado | comentar em publicações de outros usuários | trocar experiências e complementar informações sobre cursos avaliados. |
|Usuário autenticado | salvar/favoritar cursos de interesse | acessar rapidamente as informações que desejo consultar futuramente. |
|Usuário autenticado | responder um questionário vocacional | identificar áreas de tecnologia mais alinhadas ao meu perfil e interesses. |
|Usuário autenticado | solicitar a exclusão permanente da minha conta | exercer meus direitos previstos na LGPD e remover meus dados da plataforma. |
|Marca (Atendente) | responder oficialmente às avaliações que mencionam nossa instituição | dialogar com alunos de forma transparente e responsável, com selo de verificação. |
|Marca (Administrador) | visualizar métricas de desempenho da minha marca | monitorar a reputação da instituição e identificar pontos de melhoria. |
|Moderador | aprovar ou recusar publicações com motivo registrado | garantir a qualidade e integridade do conteúdo publicado na plataforma. |
|Moderador | gerenciar a fila de denúncias | agir rapidamente sobre conteúdo inapropriado e proteger a comunidade. |


## Requisitos

### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-------------------------|------------|
|RF-01| A aplicação deve permitir ao usuário criar uma conta fornecendo e-mail, senha e CPF. | ALTA |
|RF-02| A aplicação deve validar o CPF do usuário, garantindo unicidade e imutabilidade após confirmação. | ALTA |
|RF-03| A aplicação deve exigir vinculação de perfil do LinkedIn para que o usuário possa publicar avaliações. | ALTA |
|RF-04| A aplicação deve implementar controle de acesso por papéis (RBAC): Usuário, Marca e Moderador. | ALTA |
|RF-05| A aplicação deve permitir ao usuário editar seu perfil (avatar, nome, @username, bio, localidade, stack, senioridade). | MÉDIA |
|RF-06| A aplicação deve oferecer um questionário vocacional para identificar áreas de interesse do usuário. | MÉDIA |
|RF-07| A aplicação deve exibir um banner de onboarding até que o perfil esteja completo (CPF + LinkedIn + stack + senioridade). | BAIXA |
|RF-08| A aplicação deve permitir que instituições solicitem cadastro de marca (CNPJ, razão social, site, e-mail corporativo). | ALTA |
|RF-09| A aplicação deve exibir selo de verificação no perfil de marcas aprovadas e em suas respostas oficiais. | MÉDIA |
|RF-10| A aplicação deve permitir vínculo entre usuário e marca, sujeito à aprovação do moderador. | MÉDIA |
|RF-11| A aplicação deve permitir ao usuário publicar avaliações de cursos com campos padronizados (título, curso, dificuldade, didática, nota geral, stack, entre outros). | ALTA |
|RF-12| A aplicação deve submeter publicações a um fluxo de moderação com filtro automático e revisão humana. | ALTA |
|RF-13| A aplicação deve permitir ao autor editar sua publicação enquanto ela estiver em status "Em revisão". | MÉDIA |
|RF-14| A aplicação deve exibir um feed de publicações ordenado por score, com seção de destaques e filtro por stack. | ALTA |
|RF-15| A aplicação deve permitir ao usuário comentar e dar likes/dislikes em publicações. | ALTA |
|RF-16| A aplicação deve permitir ao usuário dar "hype" em publicações, aumentando o score do post. | MÉDIA |
|RF-17| A aplicação deve oferecer busca global por título, curso, instituição e stack, com paginação. | ALTA |
|RF-18| A aplicação deve permitir filtros combináveis (stack, senioridade, nota, hype, recência, com/sem resposta de marca). | ALTA |
|RF-19| A aplicação deve disponibilizar um centro de notificações (interações, status de publicação, moderação). | MÉDIA |
|RF-20| A aplicação deve oferecer painel para marcas visualizarem menções, responderem oficialmente e exportarem métricas em CSV. | ALTA |
|RF-21| A aplicação deve oferecer painel ao moderador com fila de publicações, fila de denúncias, aprovação em lote e logs de auditoria. | ALTA |
|RF-22| A aplicação deve permitir ao usuário denunciar posts, comentários e respostas de marca. | ALTA |
|RF-23| A aplicação deve registrar trilha de auditoria de todas as ações relevantes (aprovações, remoções, alterações de papéis). | ALTA |
|RF-24| A aplicação deve exibir recomendações e avaliações personalizadas com base no perfil do usuário. | MÉDIA |
|RF-25| A aplicação deve permitir ao usuário salvar/favoritar cursos para acesso rápido posterior. | MÉDIA |
|RF-26| A aplicação deve oferecer visualização completa e detalhada de cada curso (conteúdo, nota, avaliações, resposta da marca). | ALTA |
|RF-27| A aplicação deve permitir ao usuário solicitar a exclusão permanente de sua conta e dados. | ALTA |

**Prioridade: Alta / Média / Baixa.

### Requisitos Não Funcionais

|ID     | Descrição do Requisito  | Prioridade |
|-------|-------------------------|------------|
|RNF-01| O site deve estar disponível para acesso na internet. | ALTA |
|RNF-02| O site deve funcionar bem em celulares, tablets e computadores. | ALTA |
|RNF-03| O site deve ter cores com bom contraste, facilitando a leitura. | MÉDIA |
|RNF-04| O site deve funcionar nos principais navegadores: Chrome, Firefox, Edge e Safari. | ALTA |
|RNF-05| As páginas do site devem carregar de forma rápida. | ALTA |
|RNF-06| O site deve estar disponível quase o tempo todo, sem longos períodos fora do ar. | ALTA |
|RNF-07| O site deve carregar imagens com agilidade e processar ações em segundo plano sem travar. | MÉDIA |
|RNF-08| O código deve ser testado antes de ser publicado. | MÉDIA |
|RNF-09| O site deve estar em português do Brasil, com possibilidade de outros idiomas no futuro. | BAIXA |
|RNF-10| Quando algo der errado, o site deve exibir uma mensagem clara e amigável para o usuário. | MÉDIA |

**Prioridade: Alta / Média / Baixa.
