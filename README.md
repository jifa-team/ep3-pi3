# Projeto JIFA - Repositório de Documentação de Requisitos

Este repositório tem como **objetivo exclusivo** apresentar a documentação de requisitos do sistema da clínica odontológica **JIFA**, desenvolvida na disciplina **Projeto Integrado III - Entregável Parcial 3** (ADS - UFCA).

📌 **Escopo deste repositório:**
- Histórias de Usuário (HUs)
- Casos de Teste

---

## 🧩 Histórias de Usuário

As histórias de usuário foram elaboradas com base nas necessidades identificadas para diferentes perfis (visitantes, clientes, administradores). Elas foram estruturadas no formato:

> COMO [persona]  
> POSSO [ação]  
> PARA [objetivo]

Cada história está acompanhada de **critérios de aceitação** que auxiliam na validação das funcionalidades propostas.

### 📄 Lista de Histórias de Usuário

| ID | Como | Posso | Para | Critérios de Aceitação |
|----|------|--------|------|-------------------------|
| HU01 | Cliente cadastrado | fazer login no sistema | acessar minha área restrita e informações personalizadas | - O sistema deve validar credenciais válidas<br>- O acesso deve redirecionar para a área do cliente<br>- Mensagens de erro devem ser exibidas em caso de falha |
| HU02 | Visitante | me cadastrar no sistema | criar uma conta e acessar os serviços oferecidos | - Formulário com campos obrigatórios (nome, e-mail, senha)<br>- Validação de dados em tempo real<br>- Confirmação de cadastro com mensagem de sucesso |
| HU03 | Visitante | visualizar informações sobre a clínica | conhecer a estrutura e os serviços oferecidos | - Página com descrição clara da clínica<br>- Disponibilização de imagens e seções bem definidas<br>- Conteúdo responsivo em diferentes dispositivos |
| HU04 | Visitante | visualizar a página 'Quem Somos' | saber mais sobre a empresa e sua história | - Exibir descrição institucional da empresa<br>- Mostrar missão, visão e valores<br>- Apresentar histórico e equipe (se aplicável) |
| HU05 | Visitante | realizar um agendamento de avaliação gratuita | conhecer os serviços oferecidos pela clínica sem a contratação imediata | - Formulário de agendamento com data e horário<br>- Confirmação por e-mail ou tela de sucesso<br>- Validação de campos obrigatórios |
| HU06 | Visitante | acessar perguntas frequentes | esclarecer dúvidas comuns sem precisar entrar em contato direto com a clínica | - Listar perguntas e respostas organizadas por tópicos<br>- Sistema de busca simples<br>- Disponível na navegação principal |
| HU07 | Cliente logado | acessar o painel do cliente | visualizar minhas informações e serviços contratados | - Painel deve conter informações de planos, agendamentos e dados pessoais<br>- Interface clara e responsiva<br>- Permitir atualização de informações básicas |
| HU08 | Cliente logado | avaliar o atendimento | contribuir com feedbacks e ajudar em melhorias | - Sistema de avaliação com estrelas ou notas<br>- Campo opcional para comentário<br>- Confirmação de envio do feedback |
| HU09 | Visitante | visualizar os diferentes tipos de planos de saúde | comparar benefícios e carências e escolher o mais adequado | - Listagem dos tipos de plano com descrição clara<br>- Opção de comparar planos<br>- Link para detalhes e aquisição |
| HU10 | Visitante | visualizar detalhes específicos de cada plano | entender melhor as coberturas e vantagens de cada um | - Página dedicada a cada tipo de plano<br>- Listagem de coberturas, carência, valores<br>- Design responsivo e informativo |
| HU11 | Cliente (logado ou não) | adquirir um plano de saúde | contratar o serviço desejado | - Botão de aquisição nos planos<br>- Etapas guiadas da contratação<br>- Confirmação visual da compra |
| HU12 | Cliente | escolher a forma de pagamento durante a aquisição do plano | finalizar a contratação de acordo com minhas preferências | - Opções de pagamento (cartão, boleto)<br>- Resumo do pedido antes de pagar<br>- Confirmação clara após o pagamento |

---

## ✅ Casos de Teste

👉  Os **Casos de Teste**, que derivam diretamente das histórias e critérios de aceitação, permitindo a validação do sistema conforme os requisitos definidos.

| ID  | HISTÓRIA DE USUÁRIO ASSOCIADA | CENÁRIO DE TESTE | CASO DE TESTE | PRÉ-CONDIÇÕES | DADOS DE ENTRADA | SAÍDA ESPERADA |
|-----|-------------------------------|------------------|---------------|---------------|------------------|----------------|
| 1.1 | 1.1 (Login) | Cliente cadastrado faz login com credenciais válidas | Login de Cliente Cadastrado | Usuário possui conta ativa | E-mail: usuario@exemplo.com<br>Senha: Senha123! | Redirecionamento para Painel do Cliente<br>Mensagem: "Bem-vindo, [Nome]!" |
| 1.2 | 1.1 (Login) | Cliente tenta login com credenciais inválidas | Login com Credenciais Inválidas | Usuário possui conta mas insere dados errados | E-mail: usuario@exemplo.com<br>Senha: SenhaErrada! | Mensagem: "E-mail ou senha inválidos"<br>Permanência na página de login |
| 2.1 | 2.1 (Informações Institucionais) | Visitante acessa página "Clínica" | Visualizar Informações sobre a Clínica | Acessar site e navegar até "CLÍNICA" | Clicar em "CLÍNICA" no menu | Exibição de: mapa, mensagem institucional, instalações, contatos e botão "AGENDAR AGORA" |
| 2.2 | 2.2 (Quem Somos) | Visitante acessa página "Quem Somos" | Visualizar Página "Quem Somos" | Acessar site | Clicar em "QUEM SOMOS" no menu | Exibição de: imagem institucional, texto, especialidades e botões interativos (Missão/Visão/Valores) |
| 2.3 | 2.3 (Agendamento) | Visitante agenda avaliação gratuita | Agendamento de avaliação gratuita | Estar na página inicial | Preencher: Nome, e-mail, telefone | Mensagem: "Sua avaliação foi agendada"<br>E-mail de confirmação enviado |
| 2.4 | 2.4 (FAQ) | Visitante busca pergunta frequente | Acessar respostas de perguntas frequentes | Estar na página inicial | Clicar em pergunta específica | Exibição da resposta expandida |
| 3.1 | 3.1 (Área do Cliente) | Cliente logado acessa painel | Acessar o Painel do Cliente | Usuário logado | Navegar até "PAINEL DO CLIENTE" | Exibição de: últimas atividades, atalhos de serviços e conteúdo do blog |
| 3.2 | 3.2 (Avaliação) | Cliente avalia serviços | Avaliar os serviços oferecidos | Usuário logado na página inicial | Nota: 5 estrelas<br>Comentário: "Ótimo atendimento..." | Mensagem: "Obrigada pelo feedback"<br>Dados armazenados |
| 4.1 | 4.1 (Planos de Saúde) | Visitante visualiza planos | Visualização de tipos de planos | Estar na tela inicial de planos | Navegação até "Planos de Saúde" | Exibição dos planos: individual, familiar e coletivo |
| 4.2 | 4.2 (Detalhes de Planos) | Visitante visualiza detalhes do plano individual | Visualização dos detalhes dos planos | Estar na página de tipos de plano | Clicar em "Plano Individual" | Exibição de: coberturas, carências e vantagens |
| 5.1 | 5.1 (Aquisição) | Cliente adquire plano | Cliente adquire um plano | Visualizar detalhes do plano | Clicar em "Adquira seu plano"<br>Preencher formulário | Mensagem de sucesso e início do processo |
| 5.2 | 5.2 (Pagamento) | Cliente escolhe forma de pagamento | Cliente escolhe forma de pagamento | Estar na etapa de pagamento | Selecionar "Cartão de Crédito"<br>Preencher dados | Confirmação da compra com cartão |
| NF1 | Usabilidade | Confirmação pós-compra | Sistema exibe confirmação clara | Operação realizada com sucesso | Tipo de plano, valor, forma de pagamento | Mensagem: "Compra realizada com sucesso!" + comprovante |
| NF2 | Segurança | Proteção de dados no login | Proteção de Dados no Login | Sistema usa HTTPS/criptografia | E-mail: usuario@exemplo.com<br>Senha: Senha123! | Conexão segura (cadeado)<br>Dados sensíveis não expostos |

---

## 👥 Equipe

- Gustavo Ferreira Reinaldo  
- Sayonara Arcanjo da Silva  
- Alexandra Silva de Paula  
- Carlos Eduardo de Lima Lira Santana

---

📚 Projeto desenvolvido para a disciplina **Projeto Integrado III** — Curso de Análise e Desenvolvimento de Sistemas  
**Universidade Federal do Cariri - UFCA**
