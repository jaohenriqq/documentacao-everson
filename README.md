# documentacao-everson



SISTEMA DE FREQUÊNCIA DA SALA DE INFORMÁTICA
1. INTRODUÇÃO
1.1 Objetivo
Este documento tem como finalidade descrever o projeto de um sistema de registro de frequência para a sala de informática, com base na plataforma WordPress. A proposta contempla a concepção, os componentes, as tecnologias e o fluxo funcional de uma das principais funcionalidades do sistema.

1.2 Escopo
O sistema permitirá que os usuários (alunos) registrem sua presença ao informarem nome, sala e motivo. Esses dados serão apresentados em uma lista em tempo real, permitindo visualização por professores e coordenadores.

1.3 Público-Alvo
Este documento é destinado a desenvolvedores, analistas de sistemas, gerentes de projeto e demais interessados na arquitetura e funcionamento do sistema.

2. VISÃO GERAL DO SISTEMA
O sistema tem como objetivo principal registrar as presenças na sala de informática de forma digital, eliminando registros em papel e facilitando o controle por parte dos responsáveis. Ele será disponibilizado como uma aplicação WordPress, podendo ser acessado por qualquer dispositivo conectado à internet.

Principais Recursos:
Formulário de preenchimento com os campos: nome, sala e motivo.

Armazenamento em banco de dados.

Exibição dos registros em lista ordenada.

Acesso fácil e interface intuitiva.

3. COMPONENTES DO SISTEMA
3.1 Arquitetura em Camadas
Camada	Função	Exemplo de Elementos
Interface (Frontend)	Interação com o usuário	Formulário HTML, Lista de Presenças, CSS, JS
Lógica de Negócio	Processamento dos dados e aplicação das regras de negócio	Funções PHP no tema/plugin WordPress
Persistência (Banco de Dados)	Armazenamento das informações registradas	Tabela personalizada no MySQL via wpdb

4. TECNOLOGIAS ENVOLVIDAS
Camada	Tecnologias Sugeridas
Frontend	HTML5, CSS3, JavaScript (jQuery), Bootstrap
Backend	PHP 8+, WordPress (tema ou plugin personalizado)
Banco de Dados	MySQL (utilizando a infraestrutura do WordPress)

5. FLUXO DE FUNCIONALIDADE: REGISTRAR FREQUÊNCIA
A funcionalidade escolhida para descrição é o registro de presença.

Etapas do Processo:
Acesso à página de registro:
O usuário acessa a interface web onde é apresentado um formulário com os campos obrigatórios (nome, sala, motivo).

Preenchimento do formulário:
O usuário insere os dados e envia a requisição.

Validação de dados:
O sistema realiza uma validação no frontend (JavaScript) e no backend (PHP) para garantir integridade dos dados.

Processamento pelo backend:
Após a validação, o PHP utiliza a API do WordPress ($wpdb) para registrar os dados na base de dados.

Atualização da interface:
O sistema atualiza a lista de presenças automaticamente, exibindo os dados mais recentes para todos os usuários.

6. DIAGRAMA FUNCIONAL (Fluxo de Dados)
plaintext
Copiar
Editar
+--------------------+
|   Usuário (Aluno)  |
+--------------------+
          |
          v
+-----------------------------+
| Formulário (Nome, Sala,...)|
+-----------------------------+
          |
          v
+-----------------------------+
| Validação (JS e PHP)       |
+-----------------------------+
          |
          v
+-----------------------------+
| Inserção no Banco de Dados |
+-----------------------------+
          |
          v
+-----------------------------+
| Lista de Frequência Atual  |
+-----------------------------+
7. CONSIDERAÇÕES FINAIS
O sistema de frequência proposto oferece uma solução prática, segura e acessível para o controle de presença em ambientes de informática educacional. A utilização da plataforma WordPress viabiliza a rápida implementação e manutenção, com base em tecnologias amplamente conhecidas.

8. REFERÊNCIAS
ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR 14724:2023 – Apresentação de trabalhos acadêmicos.

ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR ISO/IEC 12207:2009 – Engenharia de software – Processo de ciclo de vida de software.

WordPress Developer Handbook: https://developer.wordpress.org

W3Schools: HTML, CSS, JS, PHP Documentation
