# Sistema de Gestão das Olimpíadas (SGO)

Sistema desenvolvido para coordenar os diferentes aspectos das Olimpíadas, permitindo o gerenciamento de competições, inscrições de atletas, alocação de locais para as provas e controle de resultados.

---

## Alunos

- Erick Guedes de Carvalho
- Luiz Gustavo Fagundes

---

## Histórias de Usuário
 
---
 
### US01 — Cadastrar Competição
 
**Como** administrador do sistema,  
**Quero** cadastrar novas competições informando nome da modalidade, data, horário e local,  
**Para que** os atletas possam visualizar e se inscrever nas provas disponíveis, garantindo que o evento seja organizado com todas as informações necessárias.
 
**Contexto:**  
Durante o período de preparação das Olimpíadas, a equipe organizadora precisa registrar centenas de competições em diferentes modalidades. Cada competição possui características únicas como data, horário de início, duração prevista e o local onde será realizada. Sem esse cadastro centralizado, seria impossível coordenar inscrições, alocar locais e registrar resultados de forma eficiente.
 
**Critérios de Aceitação:**
- O sistema deve exigir o preenchimento obrigatório de: nome da modalidade, data, horário e local
- Não deve ser possível cadastrar duas competições com o mesmo nome, data e horário no mesmo local
- O sistema deve confirmar o cadastro com uma mensagem de sucesso
- A competição cadastrada deve aparecer imediatamente na lista de competições disponíveis
---
 
### US02 — Inscrever Atleta
 
**Como** atleta participante das Olimpíadas,  
**Quero** me inscrever em competições específicas representando o meu país,  
**Para que** eu possa participar oficialmente das modalidades desejadas, respeitando as regras do comitê olímpico.
 
**Contexto:**  
Atletas do mundo inteiro chegam às Olimpíadas representando suas nações. Cada atleta pode competir em várias modalidades, mas sempre sob a bandeira de um único país por modalidade. Um atleta de natação, por exemplo, pode se inscrever nos 100m livre e nos 200m borboleta, mas sempre representando o mesmo país em ambas. O sistema precisa garantir essa regra para manter a integridade da competição.
 
**Critérios de Aceitação:**
- O atleta deve estar previamente cadastrado no sistema com nome, país e modalidades de atuação
- Um atleta só pode representar um país por modalidade
- O sistema deve impedir a inscrição duplicada do mesmo atleta na mesma competição
- Após a inscrição, o atleta deve aparecer na lista de participantes da competição
- O sistema deve notificar o atleta em caso de inscrição bem-sucedida ou de erro
---
 
### US03 — Alocar Local
 
**Como** administrador do sistema,  
**Quero** alocar locais para as competições verificando automaticamente conflitos de horário,  
**Para que** nenhum local seja utilizado por duas competições simultaneamente, garantindo a logística do evento.
 
**Contexto:**  
As Olimpíadas utilizam dezenas de locais espalhados pela cidade sede — estádios, arenas, piscinas, pistas e ginásios. Cada local tem capacidade limitada e só pode abrigar uma competição por vez. O administrador precisa de uma forma eficiente de verificar se um local está disponível em determinado horário antes de alocá-lo, evitando conflitos que comprometeriam toda a organização do evento.
 
**Critérios de Aceitação:**
- O sistema deve exibir a agenda de cada local com os horários já ocupados
- Não deve ser possível alocar um local que já possui competição agendada no mesmo horário
- O sistema deve alertar o administrador em caso de conflito de horário
- A alocação confirmada deve bloquear automaticamente o horário no calendário do local
- O administrador deve poder consultar todos os locais disponíveis para uma data e horário específicos
---
 
### US04 — Registrar Resultados
 
**Como** administrador do sistema,  
**Quero** registrar os resultados das competições após sua realização, indicando os atletas classificados em primeiro, segundo e terceiro lugar,  
**Para que** o desempenho dos atletas seja documentado oficialmente e as medalhas sejam contabilizadas corretamente.
 
**Contexto:**  
Após cada prova, os juízes e cronometristas apuram os resultados oficiais. Esses resultados precisam ser inseridos no sistema rapidamente para que o quadro de medalhas seja atualizado em tempo real e os relatórios possam ser gerados. O registro deve ser preciso, pois é com base nele que o histórico de desempenho dos atletas e das nações será construído ao longo dos jogos.
 
**Critérios de Aceitação:**
- O sistema deve permitir registrar os três primeiros colocados de cada competição
- Somente atletas inscritos naquela competição podem ser registrados como classificados
- Após o registro, o quadro de medalhas dos países envolvidos deve ser atualizado automaticamente
- O resultado registrado deve ficar vinculado à competição correspondente
- Não deve ser possível alterar um resultado já registrado sem permissão de administrador
---
 
### US05 — Gerar Relatório de Medalhas
 
**Como** administrador do sistema,  
**Quero** gerar relatórios completos do quadro de medalhas por país,  
**Para que** o desempenho de cada delegação possa ser acompanhado durante toda a duração dos jogos olímpicos.
 
**Contexto:**  
O quadro de medalhas é um dos elementos mais acompanhados durante as Olimpíadas, tanto pela mídia quanto pelo público e pelos próprios comitês olímpicos. O sistema precisa consolidar todos os resultados registrados e apresentar de forma clara quantas medalhas de ouro, prata e bronze cada país conquistou, permitindo ordenar e filtrar esse ranking de diferentes formas.
 
**Critérios de Aceitação:**
- O relatório deve exibir ouro, prata e bronze separadamente para cada país
- O ranking deve ser ordenado por padrão pelo número de medalhas de ouro
- Deve ser possível filtrar o relatório por país, modalidade ou período
- O relatório deve ser atualizado automaticamente sempre que um novo resultado for registrado
- O sistema deve permitir exportar o relatório
---
 
### US06 — Consultar Competições Disponíveis
 
**Como** atleta participante,  
**Quero** consultar a lista completa de competições disponíveis com datas, horários e locais,  
**Para que** eu possa planejar minhas inscrições com antecedência e não perder nenhuma prova da minha modalidade.
 
**Contexto:**  
Com centenas de competições acontecendo ao longo dos jogos, os atletas precisam de uma forma prática de visualizar o calendário completo. Um atleta de atletismo, por exemplo, precisa saber exatamente quando e onde acontecem as eliminatórias e finais das suas provas para organizar sua preparação física e logística de deslocamento entre os locais.
 
**Critérios de Aceitação:**
- A listagem deve exibir nome da modalidade, data, horário, local e vagas disponíveis
- Deve ser possível filtrar competições por modalidade, data ou local
- Competições já encerradas devem ser identificadas visualmente
- A lista deve ser atualizada em tempo real conforme novas competições forem cadastradas
---
 
### US07 — Consultar Classificação de Atleta
 
**Como** administrador ou atleta,  
**Quero** consultar a classificação de um atleta específico em uma ou mais competições,  
**Para que** o desempenho individual possa ser acompanhado e analisado ao longo dos jogos.
 
**Contexto:**  
Comissões técnicas, jornalistas e os próprios atletas precisam acompanhar o histórico de resultados de cada competidor. Saber em quais competições um atleta participou, quais foram seus resultados e quantas medalhas conquistou é essencial para análises de desempenho e para a cobertura jornalística dos jogos.
 
**Critérios de Aceitação:**
- A consulta deve retornar todas as competições em que o atleta participou
- Deve exibir o resultado obtido em cada competição (1º, 2º, 3º ou sem classificação)
- Deve mostrar o total de medalhas conquistadas pelo atleta
- A consulta deve poder ser feita pelo nome do atleta ou pelo país que representa
---
 
### US08 — Verificar Disponibilidade de Local
 
**Como** administrador do sistema,  
**Quero** verificar a disponibilidade de um local em uma data e horário específicos antes de realizar a alocação,  
**Para que** conflitos de agenda sejam identificados previamente e a logística do evento não seja comprometida.
 
**Contexto:**  
Antes de confirmar a alocação de um local para uma competição, o administrador precisa checar se aquele espaço realmente está livre. Em eventos de grande porte como as Olimpíadas, um erro de alocação pode gerar situações caóticas, como duas competições tentando usar o mesmo estádio ao mesmo tempo. A verificação prévia é um passo obrigatório no processo de organização.
 
**Critérios de Aceitação:**
- O sistema deve exibir a agenda completa do local consultado
- Deve indicar claramente quais horários estão livres e quais estão ocupados
- Em caso de indisponibilidade, deve sugerir o próximo horário livre naquele local
- A consulta deve ser possível para qualquer data futura cadastrada no sistema
---
 
### US09 — Listar Atletas de uma Competição
 
**Como** administrador do sistema,  
**Quero** listar todos os atletas inscritos em uma competição específica,  
**Para que** eu possa gerenciar as inscrições, verificar o preenchimento de vagas e garantir que todas as exigências de participação sejam atendidas.
 
**Contexto:**  
Cada competição tem um número máximo de participantes e exige que todos os atletas inscritos atendam aos critérios de elegibilidade. O administrador precisa visualizar facilmente quem está inscrito, de qual país cada atleta vem e se há vagas restantes, para tomar decisões sobre abertura ou encerramento das inscrições.
 
**Critérios de Aceitação:**
- A listagem deve exibir nome do atleta, país que representa e data de inscrição
- Deve indicar o número de vagas preenchidas e o total disponível
- Deve ser possível remover um atleta da competição em casos de desistência ou inelegibilidade
- A lista deve ser exportável para uso pela equipe organizadora
---
 
### US10 — Consultar Medalhas de um País
 
**Como** administrador, atleta ou visitante,  
**Quero** consultar o quadro de medalhas de um país específico com detalhamento por modalidade,  
**Para que** o desempenho individual de cada delegação possa ser analisado com profundidade durante os jogos.
 
**Contexto:**  
Além do quadro geral de medalhas, comitês olímpicos nacionais, jornalistas e torcedores querem acompanhar em detalhes o desempenho do seu país — em quais modalidades conquistou medalhas, quais atletas foram responsáveis pelas conquistas e como isso evoluiu ao longo dos dias de competição. Essa consulta detalhada é fundamental para análises estratégicas e para a cobertura da imprensa nacional.
 
**Critérios de Aceitação:**
- A consulta deve exibir o total de ouros, pratas e bronzes do país selecionado
- Deve detalhar cada medalha com a modalidade, nome do atleta e data da conquista
- Deve ser possível comparar o desempenho de dois países lado a lado
- O histórico deve ser atualizado automaticamente após cada resultado registrado
---
 
## Diagramas UML
 
### Diagrama de Caso de Uso
 
<img width="700px" src="https://github.com/Erickguedesc/Sistema-Gestao-Olimpiadas/blob/main/imagens/diagrama-de-caso-de-uso.png?raw=true"/>
---
 
### Diagrama de Classes
 
<img width="700px" src="https://github.com/Erickguedesc/Sistema-Gestao-Olimpiadas/blob/main/imagens/class_diagram.png?raw=true"/>
---
 
### Diagrama de Pacotes
 
<img width="700px" src="https://github.com/Erickguedesc/Sistema-Gestao-Olimpiadas/blob/main/imagens/diagrama-de-pacotes.png?raw=true"/>
---
 
### Diagrama de Componentes
 
<img width="700px" src="https://github.com/Erickguedesc/Sistema-Gestao-Olimpiadas/blob/main/imagens/diagrama-de-componentes.png?raw=true"/>
---
 
### Diagrama de Implantação
 
<img width="700px" src="https://github.com/Erickguedesc/Sistema-Gestao-Olimpiadas/blob/main/imagens/diagrama-de-implantação.png?raw=true"/>
---
 
## Tecnologias
 
- [PlantUML](https://plantuml.com/) — utilizado para modelagem dos diagramas UML por meio de código PUML.
- [Draw.io / Diagrams.net](https://app.diagrams.net/) — utilizado para modelagem visual do Diagrama de Caso de Uso.
- Projeto PlantUML API em Python — ferramenta desenvolvida para automatizar a geração de diagramas UML a partir de códigos PlantUML, com suporte à leitura de arquivos `.puml`, requisições à API do PlantUML e salvamento dos diagramas gerados.
