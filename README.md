# Vibe Coding: criando jogos com Inteligência Artificial

Oficina prática de introdução ao **Vibe Coding**, na qual os participantes experimentam utilizar inteligência artificial para criar, personalizar e modificar jogos digitais.

A proposta é explorar como ferramentas de IA podem tornar o desenvolvimento de software mais acessível, permitindo transformar ideias em aplicações interativas por meio de instruções em linguagem natural.

## Sobre a oficina

Durante a atividade, serão apresentados conceitos introdutórios de Inteligência Artificial, programação e Vibe Coding. Em seguida, os participantes utilizarão o **[Lovable](https://lovable.dev/invite/451VQGL)** para desenvolver seus próprios jogos.

A oficina não exige experiência prévia com programação. O objetivo é experimentar, criar, testar e compreender como as decisões humanas orientam o desenvolvimento com IA.

## Jogos disponíveis

Os participantes poderão escolher entre quatro modelos iniciais:

- **Jogo de vestir:** personalize personagens com roupas e acessórios -> **[vibe & veste](https://vibe-e-veste.lovable.app)**
- **Quiz interativo:** crie um jogo de perguntas e respostas com pontuação -> **[quizlab](https://curious-culture-challenge.lovable.app)** 
- **Bichinho virtual:** cuide de um animal virtual e acompanhe suas necessidades ->  **[my little pet](https://petal-paws-care-club.lovable.app)** 

Cada modelo funciona como ponto de partida para personalizações e novas funcionalidades.

## O que vamos explorar?

- Conceitos básicos de Inteligência Artificial Generativa.
- Introdução ao Vibe Coding.
- Criação de aplicações com instruções em linguagem natural.
- Personalização de interfaces e funcionalidades.
- Testes, identificação de problemas e correção de erros.
- Pensamento crítico e tomada de decisões durante o desenvolvimento.

## Ferramenta utilizada

**Lovable:** plataforma de desenvolvimento de aplicações web com auxílio de inteligência artificial.

- Site: https://lovable.dev/

## Uma ideia importante

A inteligência artificial pode ajudar a construir, mas é preciso saber o que queremos criar, avaliar os resultados, identificar problemas e decidir como melhorar aquilo que foi desenvolvido.

**Criar com IA também é aprender a fazer perguntas, testar possibilidades e tomar decisões.**

## PDR — PRODUCT REQUIREMENTS DOCUMENT 

## QuizLab — Desafio de Conhecimentos

1. Visão geral do produto

Desenvolver um jogo web de perguntas e respostas, no qual o usuário participa de uma sequência de questões, seleciona alternativas, recebe feedback e acompanha sua pontuação.

O jogo deve apresentar uma experiência dinâmica, semelhante a um programa de perguntas e respostas ou competição de conhecimentos.

A primeira versão deve conter perguntas sobre cultura digital, tecnologia e inteligência artificial. Entretanto, a estrutura deve permitir que o conteúdo seja substituído por outros temas sem exigir mudanças na lógica principal do jogo.

2. Objetivo principal

Criar uma experiência interativa de perguntas e respostas que permita ao usuário testar conhecimentos, acompanhar seu desempenho e compreender como regras e condições determinam o funcionamento de um jogo.

3. Público-alvo

Pessoas interessadas em jogos de perguntas e respostas, desafios, cultura digital e aprendizagem.

O jogo deve ser acessível a usuários com diferentes níveis de familiaridade com tecnologia.

4. Escopo funcional

4.1. Tela inicial

Apresentar:
- Nome do jogo: QuizLab.
- Identidade visual de competição ou programa de perguntas.
- Descrição breve da experiência.
- Botão "Iniciar desafio".
- Instruções básicas.
- Indicação da quantidade de perguntas.

4.2. Configuração da partida

Permitir que o usuário selecione uma das categorias disponíveis:
- Cultura digital.
- Inteligência artificial.
- Tecnologia.
- Conhecimentos gerais.

A primeira versão pode utilizar perguntas previamente cadastradas no próprio projeto.

O usuário deve poder iniciar uma partida sem realizar cadastro.

4.3. Tela de perguntas

Apresentar uma pergunta por vez, com:
- Número da pergunta.
- Enunciado.
- Quatro alternativas.
- Indicador de progresso.
- Pontuação atual.

O usuário deve conseguir selecionar apenas uma alternativa por pergunta.

Após selecionar uma alternativa, o sistema deve apresentar feedback indicando se a resposta está correta ou incorreta.

O feedback deve incluir uma explicação curta sobre a resposta correta.

O usuário não deve conseguir alterar a resposta depois de confirmá-la.

Um botão "Próxima pergunta" deve permitir avançar após a apresentação do feedback.

4.4. Sistema de pontuação

Cada resposta correta deve acrescentar pontos à pontuação total.

Respostas incorretas não devem acrescentar pontos.

A pontuação deve ser atualizada após cada resposta confirmada.

O sistema deve impedir que uma mesma pergunta seja contabilizada mais de uma vez.

4.5. Tela de resultado

Ao terminar a partida, apresentar:
- Pontuação total.
- Quantidade de respostas corretas.
- Quantidade de respostas incorretas.
- Percentual de acertos.
- Mensagem relacionada ao desempenho.

Disponibilizar as opções:
- Jogar novamente.
- Escolher outra categoria.
- Voltar à tela inicial.

Ao iniciar uma nova partida, reiniciar corretamente a pontuação, as respostas e o progresso.

5. Requisitos de interface e experiência

A interface deve possuir identidade visual própria, com aparência de jogo e não de formulário.

As perguntas e alternativas devem ter boa legibilidade.

As alternativas devem apresentar feedback visual quando selecionadas.

A resposta correta e a resposta incorreta devem possuir indicações visuais distintas, acompanhadas de texto, para não depender exclusivamente de cores.

O indicador de progresso deve ser atualizado a cada pergunta.

A aplicação deve funcionar em computadores, notebooks e dispositivos móveis.

6. Regras de negócio

1. Cada partida deve possuir uma sequência definida de perguntas.
2. Cada pergunta deve possuir quatro alternativas.
3. Cada pergunta deve ter apenas uma resposta correta.
4. O usuário pode confirmar apenas uma alternativa por pergunta.
5. A resposta não pode ser contabilizada mais de uma vez.
6. A pontuação deve ser atualizada somente após a confirmação.
7. O avanço para a próxima pergunta deve ocorrer após o feedback.
8. O resultado final deve considerar todas as perguntas respondidas.
9. O reinício deve limpar o estado da partida anterior.

7. Modelo de dados

Entidades:
- Categoria: identificador e nome.
- Pergunta: identificador, categoria, enunciado e explicação.
- Alternativa: identificador, texto e indicação de resposta correta.
- Partida: perguntas utilizadas, respostas selecionadas, progresso e pontuação.
- Resultado: acertos, erros, percentual e pontuação final.

As perguntas devem ser armazenadas em uma estrutura local, separada dos componentes de interface.

A lógica deve permitir adicionar novas perguntas e categorias sem reconstruir o jogo.

8. Requisitos técnicos

- Aplicação web responsiva.
- Execução no navegador.
- Gerenciamento de estado da partida.
- Estrutura de dados local para perguntas.
- Separação entre conteúdo, regras e componentes visuais.
- Cálculo de pontuação no frontend.
- Não utilizar autenticação.
- Não configurar banco de dados.
- Não conectar Supabase ou Firebase.
- Não depender de APIs externas.

9. Critérios de aceitação

O produto será considerado funcional quando:
1. O usuário conseguir iniciar uma partida.
2. Conseguir selecionar uma categoria.
3. Visualizar uma pergunta por vez.
4. Conseguir selecionar uma alternativa.
5. Receber feedback correto ou incorreto.
6. Conseguir avançar para a próxima pergunta.
7. A pontuação for calculada corretamente.
8. O resultado final apresentar os dados da partida.
9. O botão de reiniciar criar uma nova partida sem dados residuais.
10. A aplicação funcionar sem backend.

10. Fora do escopo da primeira versão

Não implementar:
- Login.
- Cadastro de usuários.
- Ranking global.
- Partidas multiplayer.
- Sincronização entre dispositivos.
- Painel administrativo de perguntas.
- Banco de dados remoto.
- Integração com APIs externas.

11. Diretriz de desenvolvimento

Desenvolva todas as telas e funcionalidades descritas.

Não entregue apenas perguntas estáticas com botões decorativos.

A seleção de respostas, validação, pontuação, progresso e reinício devem funcionar de verdade.

Teste também situações como tentar avançar sem responder, responder à mesma pergunta mais de uma vez e reiniciar uma partida.

## Meu Pet Digital Simulador de Bichinho Virtual

1. Visão geral do produto

Desenvolver um jogo web de bichinho virtual inspirado em simuladores de cuidado de animais e jogos digitais clássicos.

O usuário deve poder escolher um animal, definir seu nome, acompanhar suas necessidades e realizar ações para mantê-lo saudável e feliz.

O jogo deve apresentar um personagem visual central e indicadores que representem seu estado atual.

As ações realizadas pelo usuário devem modificar esses indicadores e produzir reações visuais e textuais coerentes.

2. Objetivo principal

Criar uma experiência interativa na qual as escolhas do usuário influenciem o estado e o comportamento de um personagem virtual.

O jogo deve demonstrar como variáveis, condições, regras e consequências podem ser combinadas para produzir comportamentos diferentes.

3. Público-alvo

Pessoas interessadas em animais, jogos de simulação, personagens virtuais e experiências interativas.

Não deve ser necessário possuir conhecimento prévio sobre programação ou jogos digitais.

4. Escopo funcional

4.1. Tela inicial

Apresentar:
- Nome do jogo: My Little Pet.
- Identidade visual relacionada a animais virtuais.
- Breve explicação sobre a experiência.
- Botão "Adotar meu pet".
- Instruções básicas.

4.2. Escolha do animal

Disponibilizar pelo menos três opções de animais virtuais, como gato, cachorro e coelho.

Cada animal deve possuir uma representação visual própria.

O usuário deve escolher um animal e definir seu nome antes de iniciar a experiência.

O personagem escolhido deve aparecer na área principal do jogo.

4.3. Painel de necessidades

Apresentar indicadores visuais para:
- Fome.
- Energia.
- Higiene.
- Felicidade.

Cada indicador deve possuir uma escala de 0 a 100.

Os indicadores devem ser atualizados conforme as ações realizadas.

A interface deve apresentar o estado do personagem de maneira clara, utilizando barras, ícones e mensagens.

4.4. Ações disponíveis

Implementar as seguintes ações:

Alimentar
- Reduzir o indicador de fome.
- Produzir uma reação visual ou textual do animal.
- Impedir que a alimentação ultrapasse o limite máximo do indicador.

Brincar
- Aumentar a felicidade.
- Reduzir a energia.
- Produzir uma reação visual ou textual.

Dormir
- Aumentar a energia.
- Alterar a representação visual do personagem para indicar descanso.

Dar banho
- Aumentar a higiene.
- Produzir uma reação visual ou textual.

Fazer carinho
- Aumentar a felicidade.
- Apresentar uma reação positiva do personagem.

Cada ação deve ter uma consequência coerente nos indicadores.

4.5. Estados do personagem

O jogo deve apresentar reações diferentes de acordo com as necessidades.

Exemplos:
- Fome elevada: o animal demonstra estar com fome.
- Energia baixa: o animal demonstra cansaço.
- Higiene baixa: o animal demonstra desconforto.
- Felicidade alta: o animal apresenta uma reação positiva.

As reações devem ser atualizadas de acordo com os indicadores.

4.6. Passagem do tempo

Implementar uma passagem simples de tempo durante a partida.

Com o passar do tempo, alguns indicadores devem diminuir gradualmente, representando as necessidades do animal.

A passagem do tempo deve ser controlada pela aplicação e não deve produzir alterações excessivamente rápidas.

Na primeira versão, a simulação pode ocorrer somente enquanto a aplicação estiver aberta.

4.7. Reinício

Disponibilizar uma opção para reiniciar a experiência.

Antes de reiniciar, apresentar uma confirmação para evitar perda acidental do progresso.

Após a confirmação, restaurar os indicadores e o estado inicial do animal.

5. Requisitos de interface e experiência

A interface deve apresentar:
- Personagem em destaque.
- Nome do animal.
- Indicadores de necessidades.
- Botões de ações.
- Mensagens de reação.
- Identidade visual coerente com o universo de bichinhos virtuais.

Os botões devem apresentar estados visuais de interação.

Quando uma ação não puder ser realizada, o sistema deve explicar o motivo.

A interface deve ser responsiva e adequada a computadores, notebooks e dispositivos móveis.

6. Regras de negócio

1. Todos os indicadores devem permanecer entre 0 e 100.
2. Alimentar reduz a fome.
3. Brincar aumenta a felicidade e reduz a energia.
4. Dormir aumenta a energia.
5. Dar banho aumenta a higiene.
6. Fazer carinho aumenta a felicidade.
7. A passagem do tempo reduz gradualmente algumas necessidades.
8. As ações devem produzir alterações nos indicadores.
9. O personagem deve reagir aos estados dos indicadores.
10. O reinício deve restaurar o estado inicial.
11. O sistema não deve permitir valores negativos ou superiores a 100.

Os valores e consequências das ações devem ser definidos em uma estrutura de dados centralizada, facilitando alterações futuras.

7. Modelo de dados

Entidades:
- Animal: identificador, nome, representação visual e características.
- Pet: animal escolhido, nome personalizado e estado atual.
- Indicador: fome, energia, higiene e felicidade.
- Ação: identificador, nome e efeitos nos indicadores.
- Estado: conjunto de valores que determina as reações do personagem.

O estado atual deve ser mantido no frontend.

Utilizar armazenamento local do navegador para preservar o progresso durante sessões futuras, se possível.

A passagem do tempo deve ser calculada com base em registros de tempo, evitando depender exclusivamente de um contador que deixe de funcionar quando a página for fechada.

Na primeira versão, não é necessário simular o comportamento do pet enquanto a aplicação estiver fechada.

8. Requisitos técnicos

- Aplicação web responsiva.
- Execução no navegador.
- Gerenciamento de estado do personagem e indicadores.
- Regras de comportamento centralizadas.
- Componentes reutilizáveis para indicadores e ações.
- Persistência local opcional.
- Controle dos limites dos indicadores.
- Não utilizar autenticação.
- Não configurar banco de dados.
- Não conectar Supabase ou Firebase.
- Não depender de APIs externas.

9. Critérios de aceitação

O produto será considerado funcional quando:
1. O usuário conseguir iniciar a experiência.
2. Conseguir escolher um animal.
3. Conseguir definir seu nome.
4. Visualizar os indicadores.
5. Executar as ações disponíveis.
6. Observar mudanças nos indicadores.
7. Observar reações coerentes do personagem.
8. A passagem do tempo modificar os indicadores conforme definido.
9. Os indicadores permanecerem entre 0 e 100.
10. O reinício restaurar corretamente o estado inicial.
11. O jogo funcionar sem backend.

10. Fora do escopo da primeira versão

Não implementar:
- Cadastro ou login.
- Interação entre diferentes usuários.
- Visitas de outros jogadores.
- Ranking.
- Loja de itens.
- Compras.
- Notificações externas.
- Sincronização entre dispositivos.
- Simulação do animal em servidor enquanto o usuário estiver offline.
- Banco de dados remoto.

11. Diretriz de desenvolvimento

Desenvolva uma aplicação funcional com estados, variáveis, condições e consequências reais.

Não utilize apenas mensagens simuladas para representar as necessidades do animal. As ações precisam modificar os indicadores e as reações devem depender dos valores atuais.

Teste diferentes combinações de indicadores, incluindo situações em que uma necessidade esteja muito baixa ou muito alta.

Verifique se os limites dos indicadores são respeitados e se as ações produzem os efeitos esperados.


## Meu Estilo — Jogo de Vestir

1. Visão geral do produto
Desenvolver um jogo web interativo de vestir personagens, inspirado em jogos digitais de moda, personalização de avatares e criação de looks.

O jogo deve permitir que a pessoa selecione uma personagem, experimente diferentes roupas e acessórios, combine peças e crie composições visuais próprias.

A experiência deve transmitir a sensação de estar utilizando um pequeno estúdio de moda digital. A interface precisa ser visualmente atraente, intuitiva e adequada tanto para pessoas sem experiência com jogos de personalização quanto para usuários familiarizados com esse tipo de aplicação.

O produto deve funcionar diretamente no navegador, sem necessidade de cadastro, autenticação ou conexão com serviços externos.

2. Objetivo principal
Permitir que o usuário crie e personalize um visual para uma personagem virtual por meio de seleções e combinações de elementos visuais.

O jogo deve demonstrar que uma aplicação pode apresentar diferentes estados e comportamentos a partir das escolhas realizadas pelo usuário.

3. Público-alvo
Pessoas interessadas em jogos de moda, personalização de personagens, criatividade e experiências interativas.

A interface deve ser simples de compreender, sem exigir conhecimentos prévios de programação ou design.

4. Escopo funcional
4.1. Tela inicial
A tela inicial deve apresentar:

Nome do jogo: Vibe & Veste.
Uma identidade visual relacionada à moda e à personalização traga elementos de jogos dos anos 2000 misturado a um aesthetic barbie.
Uma breve descrição da proposta.
Um botão "Começar a jogar".
Um botão ou opção para consultar as instruções.
Ao clicar em "Começar a jogar", o usuário deve ser direcionado à tela principal de personalização.

4.2. Seleção de personagem
O jogo deve disponibilizar pelo menos duas personagens ou avatares com aparências distintas. Deve ter a opção de selecionar vários tons de pele.

O usuário deve conseguir selecionar uma personagem antes de iniciar a personalização.

A personagem selecionada deve aparecer em destaque na área central da interface.

4.3. Área de personalização
A interface deve apresentar uma área principal contendo a personagem e um painel de opções organizado por categorias.

Categorias iniciais:

Cabelos (importante ter vários tipos de cabelo como: chacheados, crespos, lisos, ondulados e afins)
Partes superiores.
Partes inferiores.
Vestidos ou peças únicas.
Calçados.
Acessórios.
Cada categoria deve disponibilizar pelo menos seis opções visuais.

A seleção de uma opção deve atualizar imediatamente a aparência da personagem.

O usuário deve conseguir combinar itens de categorias diferentes.

Quando selecionar um novo item de uma categoria, o item anteriormente selecionado naquela mesma categoria deverá ser substituído.

A seleção de uma peça única, como um vestido, deverá respeitar a lógica de composição definida para evitar combinações visualmente incompatíveis com outras peças da mesma categoria.

4.4. Interações
Implementar as seguintes funcionalidades:

Selecionar e trocar peças.
Remover uma peça selecionada.
Desfazer a última alteração.
Reiniciar a composição.
Alternar entre categorias.
Visualizar o resultado final.
O botão de desfazer deve recuperar o estado imediatamente anterior da personalização.

O botão de reiniciar deve remover as escolhas realizadas e restaurar a aparência inicial da personagem, sem retornar o usuário obrigatoriamente à tela inicial.

4.5. Finalização do look
Criar uma opção "Finalizar look".

Ao acioná-la, o jogo deve apresentar uma tela ou modal com:

A personagem com a composição final.
O nome do look.
Uma mensagem de conclusão.
A opção de voltar à edição.
A opção de criar um novo look.
Também seria interessante se o personagem pudesse mostrar a roupa completa em uma espécie de desfile ou sessão de fotografia.
O nome do look deve poder ser definido pelo usuário.

5. Requisitos de interface e experiência
A interface deve:

Utilizar uma identidade visual própria, inspirada em estúdios de moda e jogos de vestir.
Apresentar a personagem em destaque.
Organizar as opções em categorias identificáveis.
Indicar visualmente qual item está selecionado.
Oferecer feedback imediato após cada interação.
Manter os controles acessíveis e fáceis de compreender.
Adaptar-se a diferentes tamanhos de tela, especialmente computadores e notebooks.
Não utilizar uma interface com aparência de painel administrativo.

As ilustrações devem manter consistência visual. Caso não existam imagens próprias para todas as peças, utilizar recursos gráficos locais, ilustrações simples ou elementos visuais coerentes. Não utilizar imagens externas que dependam de links instáveis.

6. Regras de negócio
Apenas um item pode estar selecionado por categoria, salvo quando uma categoria for explicitamente definida como cumulativa.
Itens de categorias diferentes podem ser combinados.
A troca de um item deve atualizar a personagem imediatamente.
Remover um item não deve afetar as demais categorias.
Desfazer deve restaurar a última alteração realizada.
Reiniciar deve restaurar o estado inicial da personagem.
A finalização deve apresentar a composição atual, e não uma versão anterior.
7. Modelo de dados
A aplicação deve organizar os dados de forma estruturada.

Entidades principais:

Personagem: identificador, nome e aparência inicial.
Categoria: identificador e nome.
Item: identificador, categoria, nome e representação visual.
Composição: personagem selecionada, itens escolhidos e nome do look.
O estado da composição deve ser gerenciado no frontend.

Caso seja necessário persistir temporariamente o trabalho, utilizar o armazenamento local do navegador.

8. Requisitos técnicos
Aplicação web responsiva.
Interface e lógica executadas no navegador.
Gerenciamento de estado para personagem, itens e categorias.
Componentes reutilizáveis para categorias e opções de personalização.
Separação entre dados dos itens e componentes visuais.
Código organizado para facilitar a inclusão de novos itens e categorias.
Não utilizar autenticação.
Não configurar banco de dados.
Não conectar Supabase ou Firebase.
Não depender de APIs externas.
9. Critérios de aceitação
O produto será considerado funcional quando:

O usuário conseguir iniciar o jogo.
Conseguir selecionar uma personagem.
Conseguir visualizar as categorias de personalização.
Conseguir selecionar diferentes itens.
A personagem for atualizada após cada seleção.
A troca de itens funcionar sem acumular elementos incompatíveis.
Os botões de remover, desfazer e reiniciar funcionarem corretamente.
A composição final for exibida corretamente.
O jogo funcionar sem conexão com serviços externos após carregar os recursos necessários.
A interface se adaptar a diferentes resoluções.
10. Fora do escopo da primeira versão
Não implementar:

Cadastro de usuários.
Login.
Galeria pública.
Compartilhamento entre usuários.
Ranking.
Compra de roupas ou acessórios.
Banco de dados remoto.
Sincronização entre dispositivos.
11. Diretriz de desenvolvimento
Construa a aplicação completa, incluindo interface, componentes, estados e interações.

Não entregue apenas um protótipo visual ou uma tela estática.

Antes de concluir, verifique o funcionamento de todas as interações descritas nos requisitos e corrija eventuais problemas encontrados.

Priorize a funcionalidade e a consistência do comportamento do jogo.
