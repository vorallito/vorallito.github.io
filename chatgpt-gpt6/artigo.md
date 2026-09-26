# GPT-6 Astra, GPT-6 Sol e GPT-6 Luna chegaram. Seu ChatGPT já sabe como você trabalha?

**A família GPT-6 amplia o que a IA faz no trabalho. Este roteiro mostra como escolher o modelo e transformar seu processo em uma receita reutilizável.**

Você entrega ao ChatGPT uma proposta comercial, uma planilha e as notas da reunião. Pede um resumo executivo. Ele devolve um texto elegante, mas mistura o que foi decidido com o que ainda depende de aprovação.

Na segunda tentativa, você escreve: “Não invente decisões. Cite a origem de cada número. Siga o formato usado pela equipe.” Na terceira, cola tudo outra vez.

Agora temos três modelos da mesma geração. **GPT-6 Astra** foi apresentado para os trabalhos mais exigentes, com avanços em tarefas de várias etapas, uso do computador e criação de documentos, planilhas e apresentações. **GPT-6 Sol e GPT-6 Luna, lançados em 22 de setembro**, levam parte desses avanços a opções mais rápidas e com menor preço na API. A pergunta útil não é qual nome parece mais poderoso. É **qual parte do seu trabalho pede mais capacidade e qual parte precisa de um processo claro e repetível**. [Fontes: OpenAI sobre GPT-6 Astra](https://openai.com/index/gpt-6-astra/) e [sobre GPT-6 Sol e GPT-6 Luna](https://openai.com/index/introducing-gpt-6-sol-and-luna/).

No [guia anterior](https://vorallito.substack.com/p/pare-de-colar-o-mesmo-contexto-no), mostrei como pensar nisso com Claude Skills. Esta é a edição para quem trabalha com **ChatGPT**.

## Uma família, três ritmos de trabalho

**GPT-6 Astra:** eu o escolheria para uma decisão difícil que atravessa vários arquivos e ferramentas. Pense em reconciliar três versões de uma proposta, comentários do jurídico e uma planilha de preços antes de produzir o documento final. É a opção de maior capacidade da família segundo a OpenAI. [Fonte](https://openai.com/index/gpt-6-astra/).

**GPT-6 Sol:** eu testaria em análises, pesquisas e redações profissionais que se repetem, especialmente quando preciso revisar a resposta algumas vezes. A OpenAI o apresenta como uma opção forte para trabalho difícil, com mais margem para iterar; na API, seu preço por token é menor que o de GPT-6 Astra. [Fontes: GPT-6 Sol](https://openai.com/index/introducing-gpt-6-sol-and-luna/) e [GPT-6 Astra](https://openai.com/index/gpt-6-astra/).

**GPT-6 Luna:** eu começaria por triagens, classificações e primeiros rascunhos com critérios claros, conferindo se o resultado atende ao padrão antes de ampliar o uso. Entre os três, tem o menor preço por token na API. [Fontes: GPT-6 Sol e GPT-6 Luna](https://openai.com/index/introducing-gpt-6-sol-and-luna/) e [GPT-6 Astra](https://openai.com/index/gpt-6-astra/).

Esses são **critérios editoriais para escolher o primeiro teste**, não resultados de uma comparação que executei. GPT-6 Sol e GPT-6 Luna estão disponíveis em **ChatGPT Work e Codex** para contas elegíveis; a OpenAI informa que eles ainda não aparecem nas conversas comuns de Chat. O acesso a GPT-6 Astra, os limites de uso e as opções mostradas no seletor dependem do plano e das configurações do workspace. [Fontes: lançamento](https://openai.com/index/introducing-gpt-6-sol-and-luna/) e [Central de Ajuda](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex).

## Quatro peças, quatro funções

Antes de baixar qualquer coleção de prompts, separe as peças do trabalho:

- **Projeto** guarda conversas, arquivos e instruções de um assunto contínuo. Exemplo: “Propostas comerciais”, com modelo aprovado e glossário da equipe.
- **Skill** define um procedimento reutilizável para uma tarefa específica. Exemplo: revisar uma proposta, separando fatos de hipóteses e conferindo números.
- **Work** executa trabalho de várias etapas e produz entregáveis. Exemplo: ler os materiais, montar um documento e revisar o arquivo final.
- **Modelo** determina a capacidade usada na execução. Exemplo: GPT-6 Astra para reconciliar fontes conflitantes; GPT-6 Sol para revisar uma análise; GPT-6 Luna para uma triagem bem definida.

[Projetos](https://help.openai.com/en/articles/10169521-projects-in-chatgpt) estão disponíveis para usuários conectados, conforme plano e configuração. As [Skills nativas do ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt) são oferecidas a contas elegíveis Business, Enterprise, Healthcare e Edu e podem depender de liberação pelo administrador. O [modo Work](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex) atende tarefas mais longas e produz arquivos; seu acesso também depende do plano.

**A distinção prática:** o Projeto reúne o contexto; a Skill descreve a receita; Work executa a tarefa; o modelo fornece a capacidade. Você pode começar pelo Projeto e pelo procedimento abaixo mesmo que o botão **Skills** ainda não apareça na sua conta.

## A primeira receita: uma proposta que não inventa aprovações

Escolha uma tarefa que retorna à sua mesa toda semana. Para este exemplo, vamos usar a revisão de uma proposta antes de enviá-la ao cliente.

Crie um Projeto chamado **Propostas**. Adicione somente os materiais que você tem autorização para usar: um modelo de documento, regras comerciais atuais e um exemplo aprovado. Nas instruções do Projeto, escreva como a equipe distingue preço aprovado, estimativa e decisão pendente. As instruções de Projeto valem dentro daquele Projeto e podem aproveitar seus arquivos como contexto. [Fonte: OpenAI](https://help.openai.com/en/articles/10169521-projects-in-chatgpt).

Agora copie este pedido para uma conversa nesse Projeto. Se Work estiver disponível, use-o para gerar e conferir o documento:

> Revise a proposta anexada para envio ao cliente. Compare-a com o modelo e as regras deste Projeto. Entregue: (1) pontos consistentes; (2) divergências, com trecho e fonte; (3) números que exigem conferência; (4) decisões ainda pendentes; (5) perguntas objetivas ao responsável. Não transforme estimativa em preço aprovado nem preencha lacunas por inferência. Antes de concluir, abra o arquivo final e confira se tabelas, valores e títulos correspondem ao material de origem. Se não conseguir verificar algo, marque “não verificado”.

É um procedimento pequeno, mas já tem uma propriedade essencial: **define o que fazer quando falta informação**. Uma resposta bonita deixa de ser suficiente; ela precisa preservar o estado real da proposta.

Faça um teste com uma proposta fictícia contendo um preço sem aprovação. A saída correta deve manter esse preço como pendência. Depois teste com uma proposta aprovada e veja se o procedimento deixa de gerar alarmes desnecessários. Se os dois casos funcionarem, você tem o começo de uma Skill útil.

Deixei a receita pronta para adaptar: **[baixe a Skill Revisar Proposta em ZIP](https://vorallito.github.io/chatgpt-gpt6/revisar-proposta.zip)**. Em contas elegíveis, você pode revisar o arquivo e carregá-lo em *Plugins → Skills → Create → Upload*. Se sua conta não mostrar Skills, abra o `SKILL.md` dentro do ZIP e aproveite o procedimento nas instruções de um Projeto. Também preparei a **[versão em PDF deste artigo](https://vorallito.github.io/chatgpt-gpt6/Guia_GPT6_Vorallito.pdf)** para consulta offline. [Como funcionam as Skills no ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt).

**Quer mais receitas assim, aplicadas a tarefas reais de trabalho? [Assine o VORALLITO gratuitamente](https://vorallito.substack.com/subscribe).**

## Quando transformar a receita em Skill

O ChatGPT permite criar uma Skill por conversa, editor ou upload nos ambientes elegíveis. Depois de instalada, ela pode ser acionada quando o sistema reconhecer que ajuda naquela tarefa. [Fonte: OpenAI](https://help.openai.com/en/articles/20001066-skills-in-chatgpt).

Para a revisão de propostas, a Skill deveria conter quatro coisas: **quando usar**, **quais entradas solicitar**, **quais passos seguir** e **qual saída entregar**. Escreva também quando *não* deve entrar em ação. Uma menção casual a “proposta” numa conversa não deveria iniciar uma auditoria completa.

O teste mais importante não é “a Skill rodou?”. É: **ela preservou o que estava pendente, apontou a fonte dos números e entregou o formato esperado?** Guarde um caso bem resolvido e um caso em que faltam dados. Compare os resultados sempre que mudar a receita.

Se o recurso de Skills não estiver disponível, mantenha o procedimento nas instruções do Projeto ou em um documento de referência do próprio Projeto. Você ainda terá um fluxo repetível, embora a forma de ativação seja diferente.

## Uma tarefa, três formas de aproveitar a família

Na revisão da proposta, eu começaria com **GPT-6 Luna** para identificar campos ausentes e classificar trechos como fato, estimativa ou pendência. Pediria a **GPT-6 Sol** uma primeira comparação entre proposta, regras comerciais e modelo aprovado. Levaria a **GPT-6 Astra** a etapa mais difícil: resolver divergências entre versões, produzir o arquivo final e conferir sua consistência. Se uma etapa simples falhar no seu teste, suba a capacidade; se o resultado estiver correto, guarde o procedimento.

Você não precisa trocar de modelo três vezes em toda proposta. O exemplo mostra **como decidir onde investir mais capacidade**. Em qualquer um deles, o resultado melhora quando o contexto, a tarefa e os critérios de conferência estão explícitos. GPT-6 Astra pode consumir sua franquia de Work mais rapidamente, conforme o tipo e tamanho da tarefa. [Fonte: OpenAI](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex).

## Três usos que eu montaria em seguida

**1. Reuniões → decisões verificáveis.** Entregue notas e peça três blocos: decisões tomadas, ações confirmadas e pontos a confirmar. Responsável e prazo só entram quando constarem da fonte. A Skill pode exigir esse formato sempre que você pedir uma ata ou plano de ação.

**2. Pesquisa → síntese com trilha de fontes.** Defina a pergunta, os documentos permitidos e uma tabela com afirmação, evidência, divergência e data. Work e GPT-6 Astra podem ajudar quando a pesquisa atravessa muitos documentos; a revisão humana deve conseguir voltar de cada conclusão à origem.

**3. Planilhas → números auditáveis.** Dê o arquivo, o cálculo esperado e dois exemplos conferidos manualmente. Peça que a saída identifique células alteradas, fórmulas, unidades e valores sem fonte. Abra a planilha final antes de encaminhá-la.

Essas três receitas atendem a gestão, marketing, vendas, operações e finanças. A ferramenta pode mudar; o ponto de partida continua sendo uma tarefa reconhecível e um resultado que você sabe verificar.

## Uma escolha que poupa retrabalho

Talvez você tenha criado um GPT personalizado para isso no passado. Hoje, a própria OpenAI informa que planeja descontinuar os GPTs personalizados e orienta a migração de fluxos reutilizáveis para Plugins. **Novos GPTs já não podem ser criados em contas pessoais Free, Go, Plus e Pro**; ambientes Business, Enterprise e Edu ainda têm opções sujeitas a permissões. Por isso, eu começaria um fluxo novo com Projeto e, quando disponível, Skill ou Plugin. [Fonte: OpenAI](https://help.openai.com/en/articles/8554397-creating-and-editing-gpts).

O próximo passo cabe em 15 minutos: escolha uma tarefa semanal, escreva o procedimento, teste com um caso em que falte informação e confira a saída. Se o sistema inventar uma decisão, você encontrou uma regra que precisa ficar explícita. Se acertar, salve a receita e repita o teste na semana seguinte.

**[Assine gratuitamente o VORALLITO](https://vorallito.substack.com/subscribe)** para receber novas receitas de IA aplicada ao trabalho. E responda ao e-mail de boas-vindas com sua área e uma tarefa que você repetiu esta semana. Essa resposta ajuda a escolher o próximo exemplo publicado.

*Edição independente, sem vínculo com a OpenAI. Funcionalidades e disponibilidade conferidas em 25 de setembro de 2026 nas páginas oficiais citadas. Os exemplos são ilustrativos; esta edição não apresenta um teste comparativo executado entre modelos.*
