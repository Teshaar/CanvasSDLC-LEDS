# CanvasSDLC-LEDS
Atividade #1 do LedsAcademy no tema SDLC.


CANVAS SDLC INICIAL: SISTEMA DE CATÁLOGO E GESTÃO DE MATERIAIS - LEDS

1. PROBLEMA A RESOLVER
A equipe do LEDS (composta exclusivamente por funcionários e estagiários) compartilha diversos equipamentos de hardware, dispositivos de teste e ativos de software no dia a dia do laboratório. Atualmente, não há um rastreio sistêmico centralizado que indique o status de conservação e com qual membro da equipe um determinado item está alocado. Isso gera perda de tempo na localização de recursos críticos para o desenvolvimento e homologação de sistemas para a internet, além de dificultar o controle e a auditoria do patrimônio interno do laboratório.

2. USUÁRIOS PRINCIPAIS
- Administradores/Coordenadores do Laboratório: Funcionários responsáveis pela gestão geral, auditoria de patrimônio, emissão de relatórios e cadastro/baixa de novos materiais e equipamentos.
- Membros da Equipe Técnica (Estagiários e Pesquisadores): Desenvolvedores do LEDS que consultam a disponibilidade de recursos de hardware (como smartphones para testes, monitores extras, cabos, placas de desenvolvimento) e realizam a retirada/devolução temporária de itens para uso nas atividades internas do laboratório.

3. REQUISITOS FUNCIONAIS INICIAIS
- RF01 (Cadastro de Ativos): O sistema deve permitir que os administradores cadastrem e editem equipamentos com dados de patrimônio (número de tombamento, especificações técnicas, categoria e estado de conservação).
- RF02 (Controle de Posse/Empréstimo): O sistema deve permitir que um membro da equipe (Estagiário ou funcionário) registre de forma simples quando assume a posse temporária de um item (check-out) e quando o devolve à bancada comum (check-in).
- RF03 (Visualização de Status): O sistema deve exibir um painel interno atualizado em tempo real mostrando o status de cada item ("Disponível na Bancada", "Em Manutenção" ou "Em Uso por [Nome do Estagiário/Funcionário]").

4. REQUISITOS NÃO FUNCIONAIS INICIAIS
- RNF01 (Segurança e Restrição de Acesso): O sistema deve ser de acesso estritamente restrito. Somente usuários autenticados com credenciais válidas do LEDS podem visualizar ou interagir com o catálogo (sem acesso público ou para o público universitário geral).
- RNF02 (Usabilidade/Responsividade): A interface deve ser simples, limpa e responsiva, permitindo que os membros da equipe realizem o check-in/check-out rapidamente por desktops ou dispositivos móveis dentro do laboratório.
- RNF03 (Desempenho): A atualização de status dos equipamentos no painel principal deve ocorrer de forma quase instantânea para evitar conflitos de reserva simultânea.

5. MODELO DE SDLC ESCOLHIDO
Ágil (com práticas baseadas em Scrum/Kanban).

6. JUSTIFICATIVA DA ESCOLHA DO MODELO
O modelo ágil foi escolhido porque permite entregas incrementais rápidas (MVPs) e foca na colaboração contínua. Como o LEDS é um laboratório de desenvolvimento de software, a própria equipe interna que construirá o sistema é a usuária final do produto. Isso facilita ciclos de feedback extremamente curtos e adaptações ágeis nos requisitos à medida que o sistema começa a rodar nos turnos diários de trabalho, ajustando a ferramenta organicamente à rotina da equipe.

7. PRIMEIRA ENTREGA OU PRIMEIRO INCREMENTO PLANEJADO
Inventário Digital Restrito (MVP 1):
O foco desta primeira entrega será a consolidação do banco de dados e a visibilidade interna segura, englobando:
- Tela de login restrita para autenticação estrita da equipe interna do LEDS.
- Painel de administração (CRUD) básico para que os funcionários cadastrem o patrimônio físico existente.
- Tela de listagem interna simples com busca, onde os membros da equipe podem verificar quais itens existem no laboratório e visualizar uma anotação manual indicando quem está em posse do item no momento.

8. RISCOS INICIAIS DO PROJETO
- Baixo engajamento no inventário inicial: Resistência ou atraso por parte da equipe para cadastrar e etiquetar todos os itens legados no novo sistema.
- Esquecimento de registro: Membros da equipe retirarem equipamentos da bancada sem atualizar o status no sistema, mantendo dados defasados.
- Fragilidade na segurança de acesso: Risco de vazamento ou acesso de usuários externos ao catálogo se as permissões de login não forem devidamente validadas e integradas de forma segura.

9. ESTRATÉGIA DE VALIDAÇÃO COM O USUÁRIO
Após a implementação do MVP 1, será realizado um Teste de Usabilidade Controlado no próprio ambiente de trabalho do LEDS:
1. Um funcionário administrador será solicitado a cadastrar 5 itens reais do laboratório (ex: 2 monitores e 3 smartphones de teste).
2. Dois Estagiários de turnos diferentes tentarão simular a busca por esses itens e farão uma atualização manual de posse no painel.
3. Coleta de feedback rápido em uma breve reunião interna para avaliar a usabilidade da interface e ajustar possíveis gargalos antes do desenvolvimento do módulo automatizado de check-in/check-out.
