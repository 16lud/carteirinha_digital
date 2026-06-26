# Modelo de Formalizacao de Requisitos de Software

**Sistema exemplo:** Carteirinha Escolar Digital com validacao por QR Code e consulta de horarios de onibus escolares  
**Finalidade do documento:** orientar o aluno na formalizacao dos requisitos de software, ajudando-o a pensar como engenheiro de software.  
**Observacao pedagogica:** os exemplos deste documento nao devem ser copiados como resposta final sem analise. Eles servem como ponto de partida para que o aluno refine o escopo, valide regras, defina prioridades, identifique riscos e transforme a ideia inicial em especificacoes claras e verificaveis.

---

## Checklist de fases para avancar no projeto

Use este checklist como acompanhamento macro do andamento do TCC e do desenvolvimento do sistema.

- [ ] Levantamento de requisitos
- [ ] Analise dos usuarios e partes interessadas
- [ ] Definicao do escopo da primeira versao
- [ ] Modelagem dos casos de uso
- [ ] Definicao das regras de negocio
- [ ] Definicao do banco de dados
- [ ] Prototipacao das telas principais
- [ ] Implementacao do back-end + testes
- [ ] Implementacao do front-end + testes
- [ ] Integracao entre front-end, back-end e banco de dados
- [ ] Implementacao dos testes integrados e correcoes
- [ ] Validacao com usuarios ou avaliadores
- [ ] Escrita do TCC
- [ ] Publicacao dos resultados para divulgacao do projeto
- [ ] Planejamento de deploy na Vercel
- [ ] Preparacao da apresentacao
- [ ] Apresentacao final

### Possibilidades importantes do projeto

- **Publicar os resultados para divulgacao:** criar uma pagina, repositorio, artigo, video demonstrativo ou apresentacao publica mostrando o problema, a solucao proposta, os resultados obtidos e os aprendizados do desenvolvimento.
- **Planejar publicacao na Vercel:** avaliar a possibilidade de publicar o front-end do sistema na Vercel. Caso o sistema use back-end Node.js e banco MySQL, o aluno deve verificar como hospedar tambem a API e o banco de dados, pois o deploy pode exigir mais de um servico.

---

# 1. Identificacao do sistema

## 1.1 Nome do sistema

**Modelo:**  
`Carteirinha escolar digital`

**Exemplo orientador:**  
`Carteirinha Escolar Digital`

## 1.2 Tipo de sistema

**Modelo:**  
`Sistema web responsivo, desenvolvido para funcionar em computadores, tablets e smartphones, permitindo acesso por meio de qualquer navegador conectado à internet.`

**Exemplo orientador:**  
Sistema web responsivo, acessivel por navegadores em computadores, tablets e celulares. O projeto tambem pode ser planejado para futura adaptacao como aplicativo.

## 1.3 Descricao resumida

**Modelo:**  
`O sistema foi desenvolvido com o objetivo de  facilitar o gerenciamento do transporte escolar, oferecendo aos estudantes uma identificação digital com QR Code e disponibilizando informações sobre linhas, horários e pontos de embarque. Além disso, auxilia os responsáveis pela administração do serviço no controle dos usuários cadastrados.`

**Exemplo orientador:**  
O sistema tem como objetivo permitir que estudantes solicitem ou acessem uma carteirinha escolar digital, que podera ser validada por motoristas ou responsaveis por meio de QR Code. O sistema tambem devera exibir horarios e localidades dos onibus escolares de acordo com a instituicao vinculada ao estudante.

## 1.4 Problema principal

**Modelo:**  
`Atualmente, a identificação dos estudantes que utilizam o transporte escolar ainda é feita por meio de carteirinhas físicas. Esse processo causar alguns problemas, como perda ou danos na carteirinha, demora na verificação e até o uso do transporte por pessoas que não têm autorização gerando superlotação. Além disso, muitos estudantes acabam tendo dificuldade para encontrar informações atualizadas sobre os horários, rotas e pontos de embarque dos ônibus. `

**Exemplo orientador:**  
Atualmente, estudantes podem enfrentar dificuldade para emitir, portar ou validar a carteirinha escolar fisica. Alem disso, motoristas e gestores podem ter pouco controle sobre a quantidade de estudantes utilizando o transporte, o que pode contribuir para superlotacao, uso indevido do servico e falta de informacoes claras sobre horarios e rotas.

## 1.5 Objetivo geral do sistema

**Modelo:**  
` O objetivo principal deste sistema é criar uma plataforma digital simples e funcional que ajude a organizar o transporte escolar. A ideia é que os estudantes consigam acessar sua carteirinha digital de forma rápida, sem depender de documento físico, além de terem um QR Code que possa ser usado para validação no momento do embarque.

Além disso, o sistema também busca facilitar a vida dos usuários ao reunir em um só lugar informações importantes como horários, rotas e pontos de parada dos ônibus escolares. Com isso, tanto os alunos quanto os motoristas e responsáveis pelo transporte conseguem ter mais clareza e controle sobre o funcionamento do serviço. `

**Exemplo orientador:**  
Disponibilizar uma plataforma digital para cadastro de estudantes, geracao de carteirinha escolar, validacao por QR Code e consulta de horarios do transporte escolar, melhorando o acesso a informacao e o controle de utilizacao do servico.

---

# 2. Contexto do problema

Nesta secao, o aluno deve explicar o cenario atual antes da existencia do sistema.

## 2.1 Perguntas orientadoras

- Como o processo funciona atualmente?
- Quem sofre com o problema?
- Quais dificuldades existem?
- Que consequencias o problema causa?
- O problema envolve tempo, custo, seguranca, organizacao, acesso a informacao ou controle?
- Como o sistema proposto pode melhorar esse cenario?

## 2.2 Descricao do contexto

**Modelo:**  
`Atualmente, o processo de controle do transporte escolar ainda é feito de forma bem tradicional, dependendo de carteirinhas físicas, listas impressas ou até conferências feitas manualmente pelos motoristas. Isso significa que, na prática, não existe um sistema centralizado que organize todas as informações de forma rápida e atualizada. Quem mais acaba sentindo os impactos são os estudantes, os motoristas e também os gestores do transporte escolar. Os alunos, por exemplo, enfrentam dificuldades para comprovar que realmente têm direito ao transporte, principalmente quando esquecem ou perdem a carteirinha física. Já os motoristas precisam fazer verificações rápidas e, muitas vezes, acabam dependendo apenas da identificação visual ou de listas, o que nem sempre é eficiente. As principais dificuldades envolvem justamente a falta de organização e de atualização das informações. Mudanças de horários, rotas ou pontos de parada podem demorar para serem comunicadas, causando confusão e atrasos. Além disso, o controle de quem realmente está utilizando o transporte pode ficar limitado, o que pode gerar problemas como superlotação ou uso indevido do serviço. Essas situações acabam afetando diretamente o tempo, a organização e até a segurança do sistema de transporte escolar. Também existe um impacto na comunicação entre escola, motoristas e alunos, já que as informações não ficam centralizadas em um único lugar.
Aparti disso, o sistema proposto surge como uma forma de melhorar esse cenário, trazendo mais controle. Com uma plataforma digital, as informações ficam reunidas e atualizadas em tempo real, facilitando o acesso dos estudantes, a verificação por parte dos motoristas e a gestão por parte dos responsáveis.`

**Exemplo orientador:**  
O processo de identificacao dos estudantes que utilizam transporte escolar depende, em muitos casos, de documentos fisicos, conferencias manuais ou conhecimento previo dos motoristas. Isso pode dificultar a verificacao da validade da carteirinha, permitir falsificacoes ou uso por pessoas nao autorizadas e gerar falta de controle sobre a lotacao dos onibus. Alem disso, os estudantes nem sempre possuem acesso facil aos horarios, pontos de saida e localidades dos onibus escolares. Um sistema digital pode centralizar essas informacoes, facilitar a validacao e melhorar a comunicacao entre estudantes, escolas, motoristas e prefeitura.

---

# 3. Publico-alvo e partes interessadas

Liste os grupos de pessoas ou instituicoes que terao interesse no sistema.

| Parte interessada | Papel no sistema | Interesse ou necessidade | Exemplo relacionado ao contexto |
|---|---|---|---|
| Estudante | Usuario que acessa a carteirinha digital e consulta horarios | Ter acesso rapido a carteirinha e informacoes do transporte | O estudante acessa o sistema pelo celular para apresentar o QR Code ao motorista |
| Motorista | Usuario que valida carteirinhas e consulta rota/horario | Confirmar se o estudante pode utilizar o transporte | O motorista escaneia o QR Code antes do embarque |
| Escola | Instituicao que pode validar ou manter dados dos estudantes | Garantir que apenas alunos vinculados sejam cadastrados | A escola confirma se o estudante esta matriculado |
| Prefeitura | Orgao responsavel pela gestao do transporte escolar | Controlar uso, rotas, usuarios e possiveis irregularidades | A prefeitura acompanha a quantidade de alunos por rota |
| Administrador do sistema | Usuario com permissoes de configuracao e manutencao | Gerenciar cadastros, rotas, escolas e usuarios | O administrador cadastra uma nova escola ou altera um horario |

---

# 4. Atores do sistema

Um ator e alguem ou algo que interage diretamente com o sistema.

| Ator | Descricao | Permissoes esperadas | Exemplo orientador |
|---|---|---|---|
| Estudante | Pessoa matriculada em uma instituicao de ensino e usuaria do transporte escolar | Cadastrar-se, acessar perfil, visualizar carteirinha, consultar horarios | Maria cria sua conta e visualiza sua carteirinha digital |
| Motorista | Responsavel pela condução ou verificacao dos estudantes no transporte | Fazer login, ler QR Code, consultar rota e horario | Joao escaneia o QR Code do estudante no embarque |
| Escola | Instituicao vinculada aos estudantes | Validar vinculo do estudante, consultar alunos cadastrados | A escola confirma se Pedro esta regularmente matriculado |
| Prefeitura | Gestora do servico de transporte escolar | Consultar dados gerais, rotas, horarios e relatorios | A prefeitura verifica a quantidade de estudantes por linha |
| Administrador | Usuario tecnico ou gestor com acesso ampliado | Gerenciar usuarios, escolas, rotas, horarios e permissoes | O administrador corrige o horario de uma rota |

## Perguntas orientadoras

- Quem acessa o sistema?
- Quem cadastra informacoes?
- Quem consulta informacoes?
- Quem valida dados?
- Existe algum administrador?
- Existem diferentes niveis de acesso?

---

# 5. Escopo do sistema

Esta secao define claramente o que faz parte e o que nao faz parte do sistema.

## 5.1 O sistema devera contemplar

**Modelo:**

- `[Funcionalidade ou area que faz parte do sistema]`
- `[Funcionalidade ou area que faz parte do sistema]`

**Exemplo orientador:**

- Cadastro e login de estudantes.
- Cadastro e login de motoristas ou usuarios responsaveis pela validacao.
- Geracao de carteirinha digital para estudantes cadastrados.
- Geracao ou exibicao de QR Code associado a carteirinha.
- Leitura e validacao do QR Code pelo motorista.
- Consulta de horarios e localidades dos onibus escolares.
- Area administrativa para gestao basica de escolas, usuarios, rotas e horarios.

## 5.2 O sistema nao contemplara neste momento

**Modelo:**

- `[Funcionalidade que nao sera desenvolvida nesta versao]`
- `[Limitacao consciente do projeto]`

**Exemplo orientador:**

- Pagamento de tarifas ou gestao financeira do transporte.
- Rastreamento em tempo real dos onibus por GPS.
- Aplicativo nativo para Android ou iOS na primeira versao.
- Integracao automatica com sistemas oficiais da prefeitura ou da escola, caso nao haja acesso a essas bases.
- Reconhecimento facial ou biometria.

## 5.3 Pergunta importante

> O que sera entregue na versao inicial do sistema e o que ficara fora do projeto?

**Exemplo de resposta orientadora:**  
A primeira versao deve priorizar cadastro, login, carteirinha digital, QR Code, validacao e consulta de horarios. Funcionalidades mais avancadas, como GPS, relatorios complexos ou app nativo, podem ser indicadas como trabalhos futuros.

---

# 6. Requisitos funcionais

Requisitos funcionais descrevem **o que o sistema deve fazer**.

## 6.1 Modelo de requisito funcional ampliado

Use o padrao abaixo para cada requisito.

| Campo | Descricao | Exemplo orientador |
|---|---|---|
| Codigo | Identificador unico do requisito | RF-001 |
| Nome | Nome curto do requisito | Cadastro de estudante |
| Tipo | Funcional | Funcional |
| Ator principal | Quem utiliza a funcionalidade | Estudante |
| Descricao | O que o sistema deve permitir | O sistema deve permitir que o estudante realize seu cadastro informando seus dados pessoais e escolares |
| Entrada de dados | Dados informados pelo usuario | Nome, CPF ou matricula, escola, turno, serie, e-mail, senha |
| Processamento | O que o sistema faz com os dados | Valida campos obrigatorios, verifica duplicidade e cria registro do estudante |
| Saida esperada | Resultado apresentado pelo sistema | Conta criada e mensagem de confirmacao exibida |
| Prioridade | Alta, media ou baixa | Alta |
| Responsavel | Pessoa ou equipe responsavel pela implementacao | Aluno desenvolvedor / equipe back-end |
| Previsao de inicio | Data planejada para iniciar | 10/06/2026 |
| Previsao de conclusao | Data planejada para concluir | 17/06/2026 |
| Status | Situacao atual | Nao iniciado / Em andamento / Concluido / Em revisao |
| Dependencias | Requisitos ou recursos necessarios antes | Definicao do banco de dados e tela de cadastro |
| Riscos | Problemas que podem dificultar | Dados obrigatorios mal definidos ou falta de validacao |
| Criterio de aceitacao | Como saber que foi atendido | Dado um estudante com dados validos, quando preencher o formulario, entao o sistema deve criar sua conta e permitir login |
| Evidencia de validacao | Como comprovar que foi testado | Print da tela, registro no banco, resultado de teste ou video demonstrativo |
| Observacoes | Informacoes adicionais | Verificar se sera usado CPF, matricula ou ambos |

## 6.2 Tabela resumida para preenchimento dos requisitos funcionais

| Codigo | Nome do requisito | Ator | Descricao | Prioridade | Responsavel | Previsao de conclusao | Status |
|---|---|---|---|---|---|---|---|
| RF-001 | Cadastro de estudante | Estudante | O sistema deve permitir o cadastro de estudantes com dados pessoais e escolares | Alta | Equipe back-end/front-end | 17/06/2026 | Nao iniciado |
| RF-002 | Login de usuarios | Estudante, motorista, administrador | O sistema deve permitir autenticacao de usuarios com perfil de acesso | Alta | Equipe back-end | 21/06/2026 | Nao iniciado |
| RF-003 | Geracao da carteirinha digital | Sistema | O sistema deve gerar uma carteirinha digital apos cadastro aprovado | Alta | Equipe back-end/front-end | 28/06/2026 | Nao iniciado |
| RF-004 | Geracao de QR Code | Sistema | O sistema deve gerar um QR Code vinculado a carteirinha do estudante | Alta | Equipe back-end | 02/07/2026 | Nao iniciado |
| RF-005 | Validacao por QR Code | Motorista | O sistema deve permitir que o motorista valide a carteirinha por leitura de QR Code | Alta | Equipe front-end/back-end | 10/07/2026 | Nao iniciado |
| RF-006 | Consulta de horarios | Estudante, motorista | O sistema deve exibir horarios e locais dos onibus conforme instituicao ou rota | Media | Equipe front-end | 15/07/2026 | Nao iniciado |
| RF-007 | Gestao administrativa | Administrador | O sistema deve permitir o cadastro e edicao de escolas, rotas, horarios e usuarios | Media | Equipe full stack | 25/07/2026 | Nao iniciado |

## 6.3 Perguntas orientadoras

- O que o estudante precisa fazer no sistema?
- O que o motorista precisa fazer?
- O que a escola ou administracao precisa gerenciar?
- Quais informacoes precisam ser cadastradas?
- Quais informacoes precisam ser consultadas?
- O sistema gera algum documento, codigo, comprovante ou registro?
- Existe validacao de dados?
- Existe autenticacao?
- Ha diferentes telas para diferentes usuarios?

---

# 7. Requisitos nao funcionais

Requisitos nao funcionais descrevem **como o sistema deve se comportar**.

Eles tratam de qualidade, seguranca, desempenho, usabilidade, acessibilidade, compatibilidade e confiabilidade.

## 7.1 Modelo de requisito nao funcional ampliado

| Campo | Descricao | Exemplo orientador |
|---|---|---|
| Codigo | Identificador unico | RNF-001 |
| Categoria | Seguranca, usabilidade, desempenho etc. | Seguranca |
| Descricao | Caracteristica de qualidade esperada | O sistema deve exigir autenticacao para acessar funcionalidades restritas |
| Justificativa | Por que esse requisito e importante | Evita acesso indevido a dados dos estudantes |
| Criterio de verificacao | Como verificar se foi cumprido | Tentar acessar a tela administrativa sem login e confirmar bloqueio |
| Responsavel | Pessoa ou equipe responsavel | Equipe back-end |
| Previsao de conclusao | Data planejada | 22/06/2026 |
| Status | Situacao atual | Nao iniciado |
| Risco associado | O que pode dar errado | Rotas protegidas incorretamente |
| Evidencia de validacao | Prova de teste | Print da mensagem de acesso negado ou teste automatizado |

## 7.2 Tabela para preenchimento dos requisitos nao funcionais

| Codigo | Categoria | Descricao | Criterio de verificacao | Prioridade | Previsao de conclusao | Status |
|---|---|---|---|---|---|---|
| RNF-001 | Seguranca | O sistema deve exigir login para acessar carteirinha, area do motorista e area administrativa | Usuario nao autenticado deve ser redirecionado para login | Alta | 22/06/2026 | Nao iniciado |
| RNF-002 | Responsividade | O sistema deve ser utilizavel em celular, tablet e computador | Testar telas em diferentes tamanhos de tela | Alta | 12/07/2026 | Nao iniciado |
| RNF-003 | Usabilidade | O estudante deve conseguir localizar sua carteirinha em poucos passos apos login | Avaliar se a carteirinha aparece em tela principal ou menu claro | Media | 14/07/2026 | Nao iniciado |
| RNF-004 | Desempenho | O QR Code deve ser exibido e validado em tempo adequado durante o embarque | Validacao deve ocorrer sem demora perceptivel em condicoes normais | Media | 18/07/2026 | Nao iniciado |
| RNF-005 | Privacidade | O sistema deve coletar somente dados necessarios para emissao e validacao da carteirinha | Revisar formularios e banco de dados | Alta | 25/06/2026 | Nao iniciado |
| RNF-006 | Disponibilidade | O sistema deve estar disponivel para consulta nos periodos de uso do transporte escolar | Simular acesso em horarios de entrada e saida | Media | 30/07/2026 | Nao iniciado |

## 7.3 Categorias sugeridas para este sistema

- Seguranca
- Controle de acesso
- Protecao de dados pessoais
- Responsividade
- Usabilidade
- Acessibilidade
- Desempenho
- Disponibilidade
- Compatibilidade com dispositivos moveis
- Manutenibilidade

---

# 8. Regras de negocio

Regras de negocio sao condicoes ou normas que o sistema deve respeitar.

Elas nao sao exatamente telas ou botoes, mas regras que orientam o funcionamento do sistema.

## 8.1 Modelo de regra de negocio ampliado

| Campo | Descricao | Exemplo orientador |
|---|---|---|
| Codigo | Identificador unico | RN-001 |
| Nome da regra | Nome curto | Estudante deve estar vinculado a uma escola |
| Descricao | Condicao que deve ser respeitada | Toda carteirinha deve estar associada a um estudante e a uma escola cadastrada |
| Aplicada a | Funcionalidade relacionada | Cadastro de estudante e geracao da carteirinha |
| Responsavel pela validacao | Quem confirma a regra | Escola ou administrador |
| Previsao de definicao | Data para concluir a regra | 08/06/2026 |
| Status | Situacao atual | Em analise |
| Observacoes | Duvidas ou restricoes | Definir se a escola aprova manualmente ou se o sistema aceita autodeclaracao |

## 8.2 Tabela para preenchimento das regras de negocio

| Codigo | Nome da regra | Descricao | Funcionalidade relacionada | Previsao de definicao | Status |
|---|---|---|---|---|---|
| RN-001 | Vinculo com escola | Uma carteirinha so deve ser gerada para estudante vinculado a uma escola cadastrada | RF-001, RF-003 | 08/06/2026 | Em analise |
| RN-002 | QR Code unico | Cada carteirinha deve possuir um QR Code unico associado ao estudante | RF-004, RF-005 | 12/06/2026 | Nao iniciado |
| RN-003 | Perfil do motorista | O motorista so deve acessar a tela de validacao e informacoes de sua rota | RF-005, RF-006 | 15/06/2026 | Nao iniciado |
| RN-004 | Carteirinha ativa | Apenas carteirinhas ativas devem ser consideradas validas no momento da leitura | RF-005 | 18/06/2026 | Nao iniciado |
| RN-005 | Dados obrigatorios | O cadastro do estudante deve exigir os dados minimos definidos pelo projeto | RF-001 | 10/06/2026 | Em analise |

## 8.3 Perguntas orientadoras

- Quem pode criar uma carteirinha?
- Quais dados sao obrigatorios?
- Uma carteirinha pode ser alterada depois de criada?
- Quem pode validar uma carteirinha?
- Uma carteirinha pode expirar?
- Como o sistema identifica se uma validacao e valida?
- Existe vinculo entre estudante, escola e transporte?
- O motorista pode visualizar todos os alunos ou apenas os relacionados a sua rota?

---

# 9. Requisitos de dados

Nesta secao, o aluno deve identificar quais dados o sistema precisa armazenar.

## 9.1 Modelo de entidade de dados

| Entidade | Dados necessarios | Observacoes | Exemplo orientador |
|---|---|---|---|
| `[Nome da entidade]` | `[Campos necessarios]` | `[Restricoes ou detalhes]` | `[Exemplo de como essa entidade aparece no sistema]` |

## 9.2 Entidades sugeridas para analise

| Entidade | Dados necessarios | Observacoes | Exemplo orientador |
|---|---|---|---|
| Usuario | id, nome, e-mail, senha criptografada, perfil, status | Pode representar estudante, motorista ou administrador | Um usuario com perfil estudante acessa a carteirinha; um usuario motorista acessa o leitor de QR Code |
| Estudante | id, usuario_id, nome, matricula, escola_id, turma, turno, status | Evitar coletar dados desnecessarios | Ana, estudante da Escola Municipal X, periodo da manha |
| Motorista | id, usuario_id, nome, rota_id, status | Pode estar vinculado a uma ou mais rotas | Carlos, motorista da rota Bairro Centro - Escola X |
| Escola | id, nome, endereco, contato, status | Necessaria para vincular estudantes e horarios | Escola Municipal Joao da Silva |
| Carteirinha | id, estudante_id, codigo, data_emissao, validade, status | Deve estar associada a um estudante | Carteirinha ativa do estudante Ana |
| QR Code | id, carteirinha_id, token, data_geracao, status | Nao deve expor dados sensiveis diretamente | QR Code que aponta para uma verificacao segura da carteirinha |
| Rota | id, nome, origem, destino, escola_id, status | Pode agrupar horarios e localidades | Rota Bairro Novo para Escola X |
| Horario de onibus | id, rota_id, horario_saida, ponto_saida, dias_semana | Deve ser consultado por estudante e motorista | Saida as 06:30 do ponto Praca Central |
| Validacao | id, carteirinha_id, motorista_id, data_hora, resultado | Registra tentativa de validacao | Validacao aprovada em 15/07/2026 as 06:28 |

## 9.3 Cuidado pedagogico

> O aluno deve decidir quais dados sao realmente necessarios, evitando coletar informacoes desnecessarias. Em sistemas que lidam com estudantes, dados pessoais devem ser tratados com cuidado, justificativa e controle de acesso.

---

# 10. Casos de uso

Casos de uso descrevem interacoes entre atores e o sistema.

## 10.1 Modelo de caso de uso ampliado

| Campo | Descricao | Exemplo orientador |
|---|---|---|
| Codigo | Identificador unico | UC-001 |
| Nome | Nome do caso de uso | Cadastrar estudante |
| Ator principal | Quem inicia a acao | Estudante |
| Objetivo | O que o ator deseja alcancar | Criar conta para acessar a carteirinha digital |
| Pre-condicoes | O que precisa existir antes | Escola cadastrada no sistema |
| Fluxo principal | Passos normais da interacao | Usuario acessa cadastro, informa dados, sistema valida e cria conta |
| Fluxos alternativos | Situacoes diferentes do fluxo principal | E-mail ja cadastrado, dados obrigatorios ausentes |
| Pos-condicoes | Estado do sistema apos a acao | Estudante cadastrado com perfil ativo ou pendente |
| Requisitos relacionados | Codigos de RF associados | RF-001, RN-001 |
| Previsao de implementacao | Data prevista | 17/06/2026 |
| Status | Situacao atual | Nao iniciado |

## 10.2 Exemplo de caso de uso preenchido

### UC-001 - Cadastrar estudante

**Ator principal:** Estudante

**Objetivo:**  
Permitir que um estudante crie uma conta no sistema para posteriormente acessar sua carteirinha digital.

**Pre-condicoes:**

1. A escola do estudante deve estar cadastrada no sistema.
2. O estudante deve possuir os dados obrigatorios definidos pelo projeto.
3. O sistema deve estar disponivel para cadastro.

**Fluxo principal:**

1. O estudante acessa a tela de cadastro.
2. O sistema apresenta o formulario de cadastro.
3. O estudante informa nome, e-mail, senha, escola, turma ou matricula.
4. O sistema valida se os campos obrigatorios foram preenchidos.
5. O sistema verifica se ja existe usuario com o mesmo e-mail ou identificador.
6. O sistema cria o cadastro do estudante.
7. O sistema exibe uma mensagem de confirmacao.

**Fluxos alternativos:**

- **FA-01 - Dados obrigatorios ausentes:** o sistema informa quais campos precisam ser preenchidos.
- **FA-02 - E-mail ja cadastrado:** o sistema informa que ja existe uma conta associada ao e-mail.
- **FA-03 - Escola nao encontrada:** o sistema orienta o estudante a selecionar uma escola valida ou procurar a administracao.

**Pos-condicoes:**  
O estudante fica cadastrado no sistema e pode acessar o login, conforme as regras definidas para ativacao da conta.

**Requisitos relacionados:** RF-001, RF-002, RN-001  
**Previsao de implementacao:** 17/06/2026  
**Status:** Nao iniciado

## 10.3 Outros casos de uso que o aluno pode modelar

| Codigo | Nome | Ator principal | Exemplo de objetivo | Requisitos relacionados |
|---|---|---|---|---|
| UC-002 | Fazer login | Estudante, motorista, administrador | Acessar funcionalidades conforme perfil | RF-002 |
| UC-003 | Visualizar carteirinha digital | Estudante | Exibir a carteirinha no celular | RF-003 |
| UC-004 | Validar carteirinha por QR Code | Motorista | Confirmar se a carteirinha e valida | RF-005 |
| UC-005 | Consultar horarios de onibus | Estudante | Ver horario e local de saida | RF-006 |
| UC-006 | Gerenciar rotas e horarios | Administrador | Cadastrar ou atualizar horarios | RF-007 |

---

# 11. Historias de usuario

As historias de usuario ajudam a pensar do ponto de vista de quem usa o sistema.

## 11.1 Modelo

> Como `[tipo de usuario]`,  
> quero `[realizar uma acao]`,  
> para `[obter um beneficio ou resolver um problema]`.

## 11.2 Tabela para preenchimento

| Codigo | Historia de usuario | Criterios de aceitacao | Previsao de conclusao | Status |
|---|---|---|---|---|
| HU-001 | Como estudante, quero fazer meu cadastro no sistema, para acessar minha carteirinha escolar digital | O estudante deve conseguir preencher o formulario, enviar os dados e receber confirmacao de cadastro | 17/06/2026 | Nao iniciado |
| HU-002 | Como estudante, quero visualizar minha carteirinha digital, para apresenta-la quando solicitado no transporte escolar | A carteirinha deve exibir dados basicos e QR Code associado | 28/06/2026 | Nao iniciado |
| HU-003 | Como motorista, quero escanear o QR Code da carteirinha, para confirmar se o estudante pode embarcar | O sistema deve informar se a carteirinha esta valida, invalida ou expirada | 10/07/2026 | Nao iniciado |
| HU-004 | Como estudante, quero consultar os horarios dos onibus escolares, para saber onde e quando embarcar | O sistema deve exibir horarios relacionados a escola ou rota do estudante | 15/07/2026 | Nao iniciado |
| HU-005 | Como administrador, quero cadastrar rotas e horarios, para manter as informacoes do transporte atualizadas | O sistema deve permitir criar, editar e desativar horarios | 25/07/2026 | Nao iniciado |

---

# 12. Criterios de aceitacao

Criterios de aceitacao indicam como verificar se uma funcionalidade foi implementada corretamente.

## 12.1 Modelo

| Requisito relacionado | Criterio de aceitacao |
|---|---|
| `RF-XXX` | Dado que `[contexto]`, quando `[acao]`, entao `[resultado esperado]`. |

## 12.2 Estrutura recomendada

> **Dado que** `[situacao inicial]`  
> **Quando** `[acao realizada]`  
> **Entao** `[resultado esperado]`

## 12.3 Exemplos orientadores

| Requisito relacionado | Criterio de aceitacao | Evidencia esperada |
|---|---|---|
| RF-001 | Dado que o estudante possui dados validos, quando preencher o cadastro e enviar, entao o sistema deve criar sua conta | Print da mensagem de sucesso e registro no banco |
| RF-002 | Dado que o usuario ja possui conta, quando informar e-mail e senha corretos, entao o sistema deve permitir acesso ao perfil correspondente | Print da tela inicial apos login |
| RF-003 | Dado que o estudante esta cadastrado, quando acessar seu perfil, entao o sistema deve exibir sua carteirinha digital | Print da carteirinha exibida |
| RF-004 | Dado que uma carteirinha foi criada, quando o sistema gerar o QR Code, entao o codigo deve estar vinculado a carteirinha correta | Teste de leitura do QR Code |
| RF-005 | Dado que o motorista esta autenticado, quando escanear um QR Code valido, entao o sistema deve exibir confirmacao de carteirinha valida | Print da validacao aprovada |
| RF-006 | Dado que o estudante esta vinculado a uma escola, quando acessar horarios, entao o sistema deve listar horarios correspondentes a sua instituicao ou rota | Print da tela de horarios |

---

# 13. Prototipos ou esbocos de tela

Nesta secao, o aluno pode anexar desenhos, wireframes ou imagens das telas planejadas.

## 13.1 Telas previstas

| Codigo da tela | Nome da tela | Usuario que acessa | Objetivo | Exemplo de elementos na tela | Previsao de prototipo |
|---|---|---|---|---|---|
| T-001 | Tela de login | Todos os usuarios | Permitir acesso ao sistema | Campo de e-mail, campo de senha, botao entrar, link de cadastro | 05/06/2026 |
| T-002 | Cadastro de estudante | Estudante | Coletar dados para criacao da conta | Nome, escola, matricula, turma, e-mail, senha | 07/06/2026 |
| T-003 | Perfil do estudante | Estudante | Exibir dados e acesso a carteirinha | Nome, escola, botao ver carteirinha, botao horarios | 10/06/2026 |
| T-004 | Carteirinha digital | Estudante | Exibir identificacao e QR Code | Nome, escola, foto opcional, QR Code, status | 12/06/2026 |
| T-005 | Leitor de QR Code | Motorista | Validar carteirinha no embarque | Camera/leitor, resultado da validacao, informacoes basicas | 15/06/2026 |
| T-006 | Horarios e localidades | Estudante, motorista | Consultar horarios e pontos de saida | Lista de horarios, rota, ponto, escola | 18/06/2026 |
| T-007 | Painel administrativo | Administrador | Gerenciar dados do sistema | Menus para usuarios, escolas, rotas, horarios | 22/06/2026 |

## 13.2 Perguntas orientadoras

- Quais telas o sistema tera?
- Quais informacoes aparecem em cada tela?
- Que acoes o usuario pode realizar?
- As telas serao diferentes para estudante, motorista e administrador?
- Como sera o acesso pelo celular?

---

# 14. Restricoes do sistema

Restricoes sao limitacoes tecnicas, legais, academicas ou operacionais.

| Codigo | Restricao | Impacto no projeto | Exemplo orientador |
|---|---|---|---|
| RE-001 | Uso das tecnologias definidas no TCC | O desenvolvimento deve considerar HTML5, CSS, Bootstrap, JavaScript, Node.js, Angular e MySQL | A equipe deve verificar se todos conhecem essas tecnologias |
| RE-002 | Prazo academico | O escopo precisa ser limitado para ser concluido dentro do periodo do TCC | Funcionalidades como GPS podem ficar para trabalhos futuros |
| RE-003 | Acesso a internet | O sistema depende de conexao para validar QR Code e consultar horarios | Em locais com internet instavel, a validacao pode ser prejudicada |
| RE-004 | Protecao de dados pessoais | O sistema manipula dados de estudantes | O projeto deve evitar dados desnecessarios e restringir acesso |
| RE-005 | Deploy na Vercel | A publicacao pode exigir separacao entre front-end, back-end e banco de dados | O front-end pode ir para a Vercel, mas API e MySQL podem precisar de outro servico |

## 14.1 Exemplos de tipos de restricao

- Tecnologias escolhidas
- Prazo do TCC
- Conhecimento da equipe
- Disponibilidade de internet
- Dispositivos utilizados pelos usuarios
- Seguranca dos dados
- Legislacao sobre dados pessoais

---

# 15. Matriz de rastreabilidade

A matriz de rastreabilidade ajuda a relacionar objetivos, requisitos, casos de uso e testes.

| Objetivo especifico | Requisito funcional | Caso de uso | Criterio de aceitacao | Teste relacionado | Status |
|---|---|---|---|---|---|
| Criar sistema de cadastro | RF-001 | UC-001 | Cadastro criado com dados validos | CT-001 - Testar cadastro de estudante | Nao iniciado |
| Implementar login | RF-002 | UC-002 | Usuario autenticado acessa perfil correto | CT-002 - Testar login por perfil | Nao iniciado |
| Gerar carteirinha digital | RF-003 | UC-003 | Carteirinha exibida no perfil do estudante | CT-003 - Testar visualizacao da carteirinha | Nao iniciado |
| Implementar QR Code | RF-004 | UC-004 | QR Code gerado e associado a carteirinha | CT-004 - Testar leitura do QR Code | Nao iniciado |
| Validar carteirinha | RF-005 | UC-004 | Motorista recebe resultado da validacao | CT-005 - Testar validacao aprovada e rejeitada | Nao iniciado |
| Mostrar horario de onibus | RF-006 | UC-005 | Horarios aparecem conforme escola ou rota | CT-006 - Testar consulta de horarios | Nao iniciado |
| Criar area administrativa | RF-007 | UC-006 | Administrador gerencia rotas, horarios e usuarios | CT-007 - Testar cadastro de rota e horario | Nao iniciado |

## 15.1 Pergunta principal

> Cada requisito ajuda a cumprir algum objetivo do projeto?

**Exemplo de analise:**  
O requisito RF-006, consulta de horarios, esta diretamente ligado ao objetivo de mostrar os horarios dos onibus. Ja uma funcionalidade como reconhecimento facial, embora interessante, nao aparece nos objetivos iniciais e talvez deva ficar fora do escopo da primeira versao.

---

# 16. Priorizacao dos requisitos

Nem tudo precisa ser desenvolvido ao mesmo tempo. Classifique os requisitos por prioridade.

| Codigo | Requisito | Prioridade | Justificativa | Previsao de conclusao | Status |
|---|---|---|---|---|---|
| RF-001 | Cadastro de estudante | Alta | Sem cadastro, nao ha como gerar carteirinha | 17/06/2026 | Nao iniciado |
| RF-002 | Login de usuarios | Alta | Necessario para proteger dados e separar perfis | 21/06/2026 | Nao iniciado |
| RF-003 | Carteirinha digital | Alta | Funcionalidade central do sistema | 28/06/2026 | Nao iniciado |
| RF-004 | QR Code | Alta | Necessario para validacao digital | 02/07/2026 | Nao iniciado |
| RF-005 | Validacao por QR Code | Alta | Resolve o problema de verificacao no transporte | 10/07/2026 | Nao iniciado |
| RF-006 | Consulta de horarios | Media | Importante para orientar o estudante, mas pode ser implementada apos o fluxo principal | 15/07/2026 | Nao iniciado |
| RF-007 | Area administrativa completa | Media | Necessaria para gestao, mas pode comecar com funcoes basicas | 25/07/2026 | Nao iniciado |
| RF-008 | Relatorios avancados | Baixa | Pode ser melhoria futura | A definir | Fora da primeira versao |

## 16.1 Sugestao de classificacao

- **Alta:** sem isso, o sistema nao cumpre seu objetivo principal.
- **Media:** melhora o funcionamento, mas nao impede o uso basico.
- **Baixa:** recurso complementar ou melhoria futura.

---

# 17. Glossario

Liste termos importantes do dominio do sistema.

| Termo | Significado | Exemplo orientador |
|---|---|---|
| Carteirinha digital | Documento digital que identifica o estudante no sistema | A tela que mostra nome, escola, status e QR Code do estudante |
| QR Code | Codigo visual escaneavel usado para validar uma carteirinha | O motorista aponta a camera para o codigo e recebe o resultado |
| Validacao | Processo de confirmar se uma carteirinha e verdadeira, ativa e autorizada | Validacao aprovada quando o estudante esta cadastrado e ativo |
| Rota | Caminho ou linha de transporte escolar | Rota Bairro Novo - Escola Municipal X |
| Horario de onibus | Informacao sobre saida, local e periodo do transporte | Saida as 06:30 da Praca Central |
| Usuario administrador | Perfil com permissao para gerenciar dados do sistema | Pessoa que cadastra escolas, motoristas e horarios |
| Estudante ativo | Estudante autorizado a utilizar o servico naquele periodo | Aluno matriculado e com carteirinha ativa |
| Carteirinha expirada | Carteirinha cuja validade terminou | Carteirinha que deve aparecer como invalida na leitura |

## 17.1 Perguntas orientadoras

- O que significa "carteirinha digital" neste sistema?
- O que significa "validacao"?
- O que significa "rota"?
- O que significa "usuario administrador"?
- O que significa "QR Code valido"?

---

# 18. Checklist de qualidade dos requisitos

Antes de considerar o documento pronto, o aluno deve verificar:

| Pergunta | Sim/Nao | Exemplo de verificacao |
|---|---|---|
| Cada requisito esta escrito de forma clara? | [ ] | RF-001 explica exatamente quem cadastra e quais dados sao usados |
| Cada requisito pode ser testado? | [ ] | O requisito possui criterio de aceitacao verificavel |
| Os requisitos evitam palavras vagas como "rapido", "facil" ou "moderno" sem explicacao? | [ ] | Quando falar em desempenho, indicar uma forma de medir |
| Cada requisito possui um ator relacionado? | [ ] | RF-005 tem o motorista como ator principal |
| Cada requisito tem prioridade? | [ ] | Alta, media ou baixa |
| Cada requisito possui previsao de conclusao? | [ ] | Datas planejadas foram registradas |
| Os requisitos funcionais estao separados dos nao funcionais? | [ ] | RF e RNF estao em secoes diferentes |
| As regras de negocio estao identificadas? | [ ] | RN-001 explica vinculo com escola |
| Os dados necessarios foram analisados? | [ ] | Entidades como estudante, escola e carteirinha foram definidas |
| Ha criterios de aceitacao? | [ ] | Cada RF importante possui criterio no formato Dado/Quando/Entao |
| O escopo esta bem delimitado? | [ ] | GPS e app nativo foram definidos como fora da primeira versao |
| Os riscos foram registrados? | [ ] | Falta de internet, prazos e validacao de dados foram considerados |

---

# 19. Orientacoes para redacao dos requisitos

## 19.1 Evite requisitos vagos

**Evite:**  
> O sistema deve ser facil de usar.

**Prefira:**  
> O sistema deve permitir que o estudante acesse sua carteirinha em ate tres acoes apos realizar login.

## 19.2 Evite requisitos genericos de seguranca

**Evite:**  
> O sistema deve ser seguro.

**Prefira:**  
> O sistema deve exigir autenticacao para acesso as funcionalidades de estudante, motorista e administrador.

## 19.3 Evite requisitos de desempenho sem medida

**Evite:**  
> O sistema deve ser rapido.

**Prefira:**  
> O sistema deve validar o QR Code em tempo adequado para nao prejudicar o embarque, considerando condicoes normais de conexao. O aluno deve definir posteriormente uma metrica objetiva de tempo.

## 19.4 Exemplo de requisito melhorado

**Versao inicial fraca:**  
> O sistema deve mostrar a carteirinha.

**Versao melhorada:**  
> O sistema deve permitir que o estudante autenticado visualize sua carteirinha digital contendo nome, escola, status da carteirinha e QR Code de validacao.

---

# 20. Plano pedagogico de evolucao do projeto

Esta secao ajuda o aluno a organizar o projeto em etapas praticas.

## 20.1 Etapa 1 - Levantamento e analise

**Objetivo:** entender o problema e transformar a ideia em requisitos.

**Exemplo de atividades:**

- Entrevistar ou simular entrevistas com estudantes, motoristas e escola.
- Listar dificuldades atuais com carteirinha fisica e horarios de onibus.
- Identificar atores do sistema.
- Definir requisitos funcionais e nao funcionais.
- Separar o que sera feito agora e o que ficara para trabalhos futuros.

**Entregaveis esperados:**

- Documento de requisitos.
- Lista de atores.
- Lista inicial de requisitos.
- Regras de negocio.
- Escopo da primeira versao.

## 20.2 Etapa 2 - Banco de dados

**Objetivo:** definir como as informacoes serao armazenadas.

**Exemplo de atividades:**

- Criar modelo conceitual ou DER.
- Definir tabelas como usuario, estudante, escola, carteirinha, rota, horario e validacao.
- Identificar chaves primarias e estrangeiras.
- Definir campos obrigatorios.

**Entregaveis esperados:**

- Diagrama do banco.
- Script SQL inicial.
- Dicionario de dados.

## 20.3 Etapa 3 - Back-end + testes

**Objetivo:** implementar a API e as regras principais do sistema.

**Exemplo de atividades:**

- Criar endpoints de cadastro e login.
- Criar endpoints para carteirinha e QR Code.
- Criar endpoint de validacao de QR Code.
- Criar endpoints de horarios e rotas.
- Testar API com dados validos e invalidos.

**Entregaveis esperados:**

- API Node.js funcionando.
- Conexao com MySQL.
- Testes basicos dos endpoints.
- Evidencias dos testes.

## 20.4 Etapa 4 - Front-end + testes

**Objetivo:** implementar as telas que os usuarios utilizarao.

**Exemplo de atividades:**

- Criar tela de login.
- Criar tela de cadastro.
- Criar tela da carteirinha digital.
- Criar tela de leitor ou simulacao de leitura de QR Code.
- Criar tela de horarios.
- Testar responsividade com Bootstrap e Angular.

**Entregaveis esperados:**

- Telas principais funcionando.
- Navegacao entre paginas.
- Testes em celular e computador.
- Prints das telas.

## 20.5 Etapa 5 - Integracao, testes e correcoes

**Objetivo:** verificar se o sistema funciona como um todo.

**Exemplo de atividades:**

- Integrar front-end com back-end.
- Testar cadastro completo ate geracao da carteirinha.
- Testar validacao por QR Code.
- Testar consulta de horarios.
- Corrigir erros encontrados.

**Entregaveis esperados:**

- Sistema integrado.
- Lista de erros corrigidos.
- Evidencias de testes.
- Versao demonstravel.

## 20.6 Etapa 6 - Escrita do TCC

**Objetivo:** documentar o problema, a solucao, o desenvolvimento e os resultados.

**Exemplo de secoes:**

- Introducao.
- Problema.
- Objetivos.
- Fundamentacao teorica.
- Metodologia.
- Desenvolvimento do sistema.
- Resultados.
- Consideracoes finais.

**Entregaveis esperados:**

- Texto do TCC.
- Figuras do sistema.
- Diagramas.
- Resultados dos testes.

## 20.7 Etapa 7 - Publicacao e apresentacao

**Objetivo:** preparar o sistema e os resultados para demonstracao.

**Exemplo de atividades:**

- Criar uma versao de apresentacao do sistema.
- Planejar deploy do front-end na Vercel.
- Verificar onde a API e o banco de dados ficarao hospedados.
- Criar slides.
- Ensaiar a demonstracao.
- Publicar resultados em repositorio, pagina ou material de divulgacao.

**Entregaveis esperados:**

- Sistema demonstravel.
- Slides de apresentacao.
- Repositorio ou pagina de divulgacao, se aplicavel.
- Roteiro de apresentacao.

---

# 21. Estrutura final sugerida do documento de requisitos

1. Identificacao do sistema
2. Contexto do problema
3. Publico-alvo e partes interessadas
4. Atores do sistema
5. Escopo
6. Requisitos funcionais
7. Requisitos nao funcionais
8. Regras de negocio
9. Requisitos de dados
10. Casos de uso
11. Historias de usuario
12. Criterios de aceitacao
13. Prototipos ou esbocos de tela
14. Restricoes
15. Matriz de rastreabilidade
16. Priorizacao dos requisitos
17. Glossario
18. Checklist de qualidade
19. Orientacoes para redacao dos requisitos
20. Plano pedagogico de evolucao do projeto

---

# 22. Observacao final para o aluno

A formalizacao dos requisitos nao deve ser apenas uma lista de funcionalidades. Ela deve mostrar que o aluno compreendeu:

- quem sao os usuarios;
- qual problema sera resolvido;
- quais regras precisam ser respeitadas;
- quais dados serao manipulados;
- quais funcionalidades sao essenciais;
- quais riscos existem;
- como validar se o sistema realmente atende ao objetivo proposto;
- quais etapas devem ser concluidas ate a apresentacao final.

Um bom requisito deve ser **claro, necessario, verificavel, rastreavel e planejavel**. Por isso, alem da descricao, este modelo inclui campos como prioridade, responsavel, previsao de conclusao, status, dependencias, riscos e evidencias de validacao.
