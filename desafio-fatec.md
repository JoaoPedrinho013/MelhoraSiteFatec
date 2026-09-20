# Desafio de Design Thinking: melhorando a experiência dos alunos da FATEC

**Objeto de estudo:** SIGA (sistema acadêmico da FATEC)
**Método:** análise de 7 prints de tela + etapas de Design Thinking (problema, entrevista, persona, definição, ideias e solução)

> **Aviso sobre as fontes:** a pasta `prints/` não existia (ou estava vazia) no diretório, então a análise foi feita com as 7 imagens anexadas na conversa, numeradas de 1 a 7 na ordem em que foram enviadas. Tudo o que está aqui vem do que aparece nessas imagens. Quando eu suponho algo, escrevo **(suposição)**.
> Por privacidade, não reproduzi nome completo nem RA do aluno que aparecem nos prints.

---

## Passo 1 - Análise das telas

### 1.1 Print por print

| Print | Tela | O que o aluno consegue fazer (visível na imagem) |
|---|---|---|
| **1** | **Início / menu principal (seções abertas)** | Ver três blocos com atalhos: **Meu curso** (Notas, Faltas, Horário, Disciplinas, Histórico, Exame Final), **Solicitações** (Solicitar AE, Solicitar EP, Solicitar AC, Rev. Notas/Faltas, Regime Domiciliar, Rematrícula) e **Documentos** (Documentos). O bloco Solicitações tem um selo azul com o número **6**. Há uma barra inferior fixa com **Início, Meu Curso e Sair**, e um topo com ícones, "Olá, JOÃO" e foto. |
| **2** | **Consulta notas** | Ver a lista de disciplinas do semestre (7 cartões, cada um com código, nome e professor) e voltar pelo botão "Voltar". O subtítulo diz "Consulta de notas do semestre". **Nenhuma nota aparece nessa tela**; **(suposição)** é preciso clicar em uma disciplina para vê-las. |
| **3** | **Não é uma tela do SIGA** | É o enunciado do desafio (grupos de 3 a 5, 8 etapas). Não entra na análise do sistema. |
| **4** | **Avaliações** | Só aparece o título "Avaliações" e o texto "lista de avaliações agendadas neste mês". **A lista está vazia**. **(Suposição):** a tela está incompleta ou não havia provas no mês. A barra inferior tem só **Meu Curso** e **Sair** (sem "Início"). |
| **5** | **Início / menu principal (seções fechadas) + cartão do aluno** | Abrir ou fechar os três blocos (Meu curso, Solicitações, Documentos). Abaixo, um cartão com dados do aluno: iniciais, nome, RA, **Status** (Em Curso), **Curso** (Tecnologia em Desenvolvimento de Software Multiplataforma), **Turno** (Tarde) e **Unidade** (Faculdade de Tecnologia de Praia Grande). Há um link "Ver índices e prazos". |
| **6** | **Faltas** ("Faltas no semestre") | Ver, para cada disciplina, o professor, **Aulas, Presença, Ausencia e Frequência (%)**. Cinco das seis disciplinas visíveis mostram um **ícone de alerta (triângulo)** ao lado da frequência (66.7, 71.4, 42.9, 50.0 e 57.1). Só a que está em 100.0 não tem o ícone. A tela está cortada embaixo. |
| **7** | **Horário das aulas** | Ver a grade da semana, de segunda a sexta, com um bloco por aula contendo código, nome da disciplina, professor e horário (ex.: 15:00-15:50). A imagem está cortada na sexta-feira. |

### 1.2 O que o SIGA oferece ao aluno (resumo)

Pelos prints, o SIGA permite:

- **Acompanhar o semestre:** notas (print 2), faltas e frequência (print 6), horário (print 7) e avaliações do mês (print 4).
- **Fazer pedidos:** o menu Solicitações lista AE, EP, AC, revisão de notas/faltas, regime domiciliar e rematrícula (print 1). Só vemos os botões, não os formulários.
- **Consultar documentos:** o menu tem "Documentos" (print 1). O subtítulo diz "Declarações e outros cursos" (print 5).
- **Ver dados acadêmicos:** cartão com status, curso, turno e unidade (print 5).
- Os itens **Disciplinas, Histórico e Exame Final** aparecem no menu (print 1), mas **não sabemos o que há dentro deles**.

### 1.3 Pontos fracos de usabilidade e experiência

**Navegação**

1. **Barra inferior inconsistente:** nos prints 1, 2, 5, 6 e 7 ela tem 3 itens (Início, Meu Curso, Sair). No print 4 (Avaliações) o "Início" some. O aluno perde o caminho de volta.
2. **"Início" e "Meu Curso" parecem a mesma coisa.** O nome "Meu curso" aparece na barra de baixo e também como bloco no menu (prints 1 e 5). **(Suposição):** os dois levam ao mesmo menu, mas isso não fica claro.
3. **A tela de Avaliações não aparece no menu.** No print 1 os atalhos de Meu curso são Notas, Faltas, Horário, Disciplinas, Histórico e Exame Final. Não vi como o aluno chega em Avaliações. **(Suposição):** pode ser por algum ícone do topo, mas nada indica isso.
4. **O botão "Voltar" fica na ponta esquerda e o título na ponta direita** (prints 2 e 6). Em tela larga os dois ficam muito distantes.
5. **Tudo é separado por telas.** Para saber "como estou no semestre" é preciso abrir Notas, Faltas, Horário e Avaliações, um de cada vez (prints 2, 4, 6 e 7).

**Organização das informações**

6. **Notas exigem um clique extra e não mostram nenhuma nota** na lista (print 2). Já Faltas mostra os números direto no cartão (print 6). As duas telas usam o mesmo tipo de cartão, mas se comportam de forma diferente.
7. **Cartões com muito espaço vazio:** nos prints 2 e 6 metade de cada cartão é uma área cinza sem conteúdo. Isso ocupa espaço e obriga a rolar a tela (o print 6 mostra só 6 disciplinas, e o print 2 mostra 7).
8. **O horário repete informação:** no print 7, cada aula de 50 minutos repete código, nome e professor. Uma disciplina de 4 aulas seguidas vira 4 blocos iguais (ex.: IAL011 na segunda-feira).
9. **O horário não destaca o dia de hoje nem a próxima aula** (print 7), e não mostra sala ou local. **(Suposição):** pode existir em outra tela, mas nesta imagem não aparece.
10. **O cartão do aluno fica escondido embaixo** dos menus (print 5) e, com os menus abertos, é preciso rolar para chegar nele (print 1).
11. **A tela Avaliações vazia** (print 4) não explica por que está vazia nem oferece um próximo passo.

**Clareza dos textos**

12. **Siglas sem explicação:** "AE, EP, AC" (prints 1 e 5). Um aluno novo pode não saber o que são. **(Suposição):** veteranos provavelmente sabem.
13. **Selo "6" em Solicitações sem explicação** (prints 1 e 5). Não dá para saber se são pedidos abertos, respondidos ou novidades.
14. **Alerta de frequência sem explicação** (print 6): o triângulo aparece em 5 disciplinas, sem legenda, sem dizer qual é o limite e sem indicar quantas faltas ainda podem ser feitas. O mesmo triângulo aparece em 71.4 e em 42.9, então o aluno não distingue "atenção" de "reprovado por falta". **(Suposição):** o alerta indica frequência abaixo do mínimo, que costuma ser 75% no ensino superior. Isso precisa ser confirmado.
15. **Termos inconsistentes:** o menu diz "Faltas", mas a tela usa "Ausencia" (sem acento) e "Presença" (print 6). O texto da tela de Avaliações está em minúsculas, como texto provisório (print 4). "Ver índices e prazos" (print 5) é vago.
16. **Nos números de Aulas** (ex.: 24 aulas, 16 presenças), não fica claro se é o total do semestre ou só o que já aconteceu (print 6). **(Suposição):** as aulas dadas até agora.

**Fluxos confusos**

17. **Solicitações reúne muitos pedidos diferentes** (rematrícula, regime domiciliar, revisão de notas...) com o mesmo peso visual (print 1). Não há indicação do que é urgente ou de prazo.
18. **"Rev. Notas/Faltas" (revisar notas e faltas) está longe das telas de notas e faltas** (print 1 versus prints 2 e 6). Quem vê uma falta errada precisa voltar ao menu e procurar a solicitação. **(Suposição):** não existe atalho na tela de Faltas, pois nada aparece nela.

**Acessibilidade**

19. **Textos pequenos e cinza claro** sobre fundo branco: subtítulos dos menus, "Docente", rótulos do cartão do aluno (prints 1 e 5). Podem ter baixo contraste para quem tem baixa visão.
20. **Ícones do topo sem texto** (documento e sino, prints 1 a 7). Não dá para saber o que fazem sem clicar.
21. **Um cartão preto no meio dos cartões cinza** (ING086 no print 2). **(Suposição):** é o efeito de passar o mouse. Se for isso, a cor muda muito, e em telas de toque esse estado pode não existir.
22. **Ponto positivo:** o alerta de frequência usa **ícone e não só cor** (print 6), o que ajuda quem não distingue cores. Falta o texto explicativo.
23. **Ponto positivo:** o texto branco na barra escura de baixo tem bom contraste (todos os prints).

**Visual**

24. **A tela inicial é limpa e organizada em blocos** (prints 1 e 5), com ícones que ajudam a reconhecer cada item. Esse é um ponto forte.
25. **Aparência pouco consistente entre telas:** a tela inicial usa cartões brancos com ícones azuis (print 1); Notas e Faltas usam cartões cinza-azulados escuros (prints 2 e 6); Horário usa uma tabela (print 7); Avaliações é uma página em branco (print 4).
26. **Na tela de Horário, o título "Horário" aparece sobreposto pela barra do topo** (print 7). **(Suposição):** é um efeito de rolagem ou barra fixa. Se for um defeito do site, atrapalha a leitura.
27. **No desktop, o menu fica em uma coluna estreita no meio** e a barra inferior espalha os itens nas pontas (prints 1, 5 e 6). Sobra muito espaço em branco dos lados.

**Uso no celular**

Todos os prints parecem ser de **computador (tela larga)**. Sobre o celular, só posso fazer suposições:

28. **(Suposição)** A barra inferior e os menus em cartões parecem pensados para celular, o que é bom (todos os prints).
29. **(Suposição)** A tabela de horário tem até 6 colunas por dia (print 7). Em uma tela pequena isso provavelmente forçaria rolagem para o lado ou deixaria o texto minúsculo.
30. **(Suposição)** As listas de cartões de Notas e Faltas (prints 2 e 6) ficariam muito longas em uma coluna só, por causa da área cinza vazia de cada cartão.
31. **(Suposição)** Para saber a situação do semestre pelo celular (ex.: no ônibus), o aluno teria que fazer vários toques por tela. **Isso deve ser testado com alunos reais.**

---

## Passo 2 - Problema real

### 2.1 Três problemas que afetam os alunos

**Problema A - O aluno não consegue saber, de forma rápida e clara, se está em risco por faltas.**
Na tela de Faltas, 5 das 6 disciplinas visíveis têm um alerta, mas sem legenda, sem o limite e sem dizer quantas faltas ainda restam (print 6). Para ver a situação geral, ele ainda precisa abrir outras telas (prints 2, 4 e 7).

**Problema B - O aluno não entende as solicitações (siglas, selo "6" e prazos) e não sabe qual pedido fazer.**
"AE, EP, AC" não são explicados, o selo 6 não tem significado claro, e não aparecem prazos nem status na tela (prints 1 e 5).

**Problema C - O aluno tem dificuldade de consultar a rotina do semestre (horário e avaliações) de forma rápida, principalmente pelo celular.**
O horário repete informações e usa tabela larga (print 7), e a tela de Avaliações está vazia (print 4). **(Suposição):** no celular a situação é pior, mas não há print de celular para confirmar.

### 2.2 Problema escolhido: **A**

**Justificativa:**
- **É o que tem mais consequência:** faltas em excesso podem levar à reprovação (**suposição:** pelo limite de frequência mínima), e é algo que o aluno não consegue desfazer depois.
- **Tem evidência direta nos prints:** o alerta sem explicação aparece na maioria das disciplinas (print 6).
- **Envolve várias telas**, então a solução também melhora a navegação (Início, Faltas, Notas) sem precisar mexer em tudo.
- **É viável de prototipar**, porque usa dados que o SIGA já mostra (aulas, presenças, ausências, frequência).

---

## Passo 3 - 5 perguntas de entrevista

Perguntas abertas, sem induzir resposta, sobre o problema escolhido (acompanhar faltas e a situação no semestre):

1. **Me conta como foi a última vez que você abriu o SIGA. O que você queria ver e o que fez até conseguir?**
2. **Como você acompanha quantas faltas você tem em cada disciplina? Que ferramentas ou hábitos você usa?**
3. **Pense em um momento em que você ficou em dúvida sobre sua situação em alguma matéria. O que aconteceu e o que você fez depois?**
4. **Quando você vê as informações de frequência no SIGA, o que você entende delas e o que você faz com essas informações?**
5. **Se você pudesse mudar qualquer coisa na forma como recebe informações sobre suas faltas e notas, o que seria e por quê?**

> **Dica de aplicação:** deixar o aluno falar, pedir "pode me dar um exemplo?" e "por que isso foi importante?", e não sugerir soluções durante a entrevista.

---

## Passo 4 - Persona

> **Atenção: esta persona é hipotética.** Foi criada a partir dos prints e de suposições, não de entrevistas reais. Ela deve ser **ajustada depois das entrevistas com alunos reais**.

**Nome:** Larissa Menezes
**Idade:** 21 anos
**Curso:** Tecnologia em Desenvolvimento de Software Multiplataforma (3º semestre, turno da tarde)
**Unidade:** FATEC (baseada no cartão do print 5, mas hipotética)

**Rotina:**
De manhã faz estágio em uma empresa de tecnologia. Almoça rápido e vai de ônibus para a faculdade, onde tem aula das 13h10 às 18h30. À noite faz os trabalhos em grupo pelo celular e pelo notebook. Aos fins de semana estuda e descansa.

**Objetivos:**
- Ser aprovada em todas as disciplinas do semestre sem precisar de recuperação.
- Continuar no estágio sem prejudicar a faculdade.
- Saber sua situação sem depender de perguntar aos professores.

**Frustrações:**
- Precisa entrar em várias telas do SIGA para saber como está.
- Vê um alerta na frequência, mas não sabe o que ele significa nem quantas faltas ainda pode ter.
- Faltou algumas vezes por causa do estágio e só percebeu o problema quando já estava difícil de corrigir.
- Já ficou em dúvida sobre qual solicitação fazer para corrigir uma falta.

**Comportamento com tecnologia:**
Usa o celular para quase tudo (apps de banco, transporte, mensagens). Tem o hábito de usar aplicativos com notificações e resumos rápidos. Tem paciência baixa para sistemas que exigem muitos cliques. Usa o notebook para trabalhos, mas o SIGA quase sempre é acessado no celular, entre uma tarefa e outra.

**Frase que a representa:**
> "Eu só quero abrir o SIGA e saber, em cinco segundos, se está tudo bem ou se eu preciso me preocupar."

---

## Passo 5 - Definição do problema

**Frase-problema:**

> **Larissa precisa de uma visão rápida e clara da sua frequência, mostrando o risco e quantas faltas ainda pode ter, porque hoje ela tem que abrir várias telas e os alertas do SIGA não explicam o que significam nem o que fazer.**

**Pergunta "Como podemos...?":**

> **Como podemos ajudar a Larissa a entender, logo que abre o SIGA, se está em risco por faltas e o que fazer a respeito, sem precisar navegar por várias telas?**

---

## Passo 6 - 10 ideias de solução

**Ideias simples**

1. **Legenda no alerta de frequência:** ao tocar no triângulo, aparece um texto dizendo o que ele significa e qual é o limite mínimo.
2. **Cores de semáforo com texto:** verde, amarelo e vermelho, sempre acompanhados de uma palavra ("Seguro", "Atenção", "Risco"), para não depender só de cor.
3. **Barra de progresso de frequência:** uma barra por disciplina com a marca do limite mínimo, substituindo o número solto.
4. **Correção de textos na tela de Faltas:** padronizar "Ausência", explicar "Aulas" (total ou já dadas) e remover a área cinza vazia dos cartões.

**Ideias intermediárias**

5. **Calculadora "quantas faltas ainda posso ter":** em cada disciplina, mostra o número de faltas restantes até o limite.
6. **Resumo "Meu semestre" na tela inicial:** um cartão no topo com as disciplinas em risco, a próxima aula e a próxima avaliação.
7. **Atalho para "Rev. Notas/Faltas" dentro da tela de Faltas:** um botão "Achei um erro nesta falta" que leva direto à solicitação.
8. **Simulador "e se eu faltar?":** o aluno escolhe uma disciplina e um número de faltas e vê como ficaria a frequência.

**Ideias ousadas**

9. **Alertas por notificação ou e-mail:** aviso quando a frequência de uma disciplina chegar perto do limite, ou antes de uma semana com muitas aulas.
10. **Assistente de conversa dentro do SIGA:** o aluno pergunta "posso faltar na sexta?" e recebe a resposta com base nas faltas e no horário dele, sugerindo o que fazer se estiver em risco.

---

## Passo 7 - Solução escolhida

### Ideia escolhida

**Painel de frequência com calculadora de faltas** (junção das ideias 2, 5 e 6): um resumo na tela inicial que mostra, com cores e palavras, quais disciplinas estão em risco e quantas faltas ainda restam em cada uma.

### Justificativa

- **Impacto:** responde direto ao problema (o aluno saber em segundos se está em risco). Também transforma um alerta sem explicação (print 6) em uma informação que dá para agir.
- **Viabilidade:** usa dados que o SIGA já mostra (aulas, presença, ausência, frequência no print 6). A calculadora é uma conta simples. Não precisa de tecnologia nova. **(Suposição):** o limite mínimo de frequência precisa ser confirmado com a FATEC.
- **Adequação ao SIGA:** encaixa na estrutura atual. O resumo entra na tela inicial (prints 1 e 5), os detalhes ficam em Faltas (print 6), e o atalho leva à solicitação já existente "Rev. Notas/Faltas" (print 1). Mantém o mesmo visual de cartões e a barra inferior.

### As 3 telas necessárias

1. **Início com resumo "Meu semestre":** a tela inicial ganha, no topo, um cartão com as disciplinas em risco de frequência e a próxima aula.
2. **Faltas com semáforo e faltas restantes:** a tela de Faltas passa a mostrar, para cada disciplina, uma barra de frequência, a palavra de situação e quantas faltas ainda pode ter.
3. **Detalhe da disciplina com simulador:** ao tocar em uma disciplina, mostra o histórico de faltas, o simulador "e se eu faltar?" e um botão para pedir revisão de faltas.

> **Próximos passos (fora deste documento):** validar a persona com entrevistas reais, confirmar o limite de frequência com a FATEC, e só depois desenhar e testar o protótipo com outro grupo.
