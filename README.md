# Equipe Empresta Ai!

<img width="218" height="278" alt="image" src="https://github.com/user-attachments/assets/3cc12390-3f9a-4003-8ce9-976826ad8fe1" />


## Nome do Projeto
Empresta Ai! - Gestão de Empréstimo de Ferramentas

## Contexto
O projeto **Empresta Aí!** nasceu para solucionar uma necessidade frequente em condomínios: oferecer aos moradores um espaço organizado para o empréstimo de ferramentas e itens de uso compartilhado.

Nosso objetivo é criar um banco de dados relacional que servirá de base para o aplicativo "Empresta Ai!", onde os moradores possam ver a disponibilidade dos itens e registrar empréstimos. Para a administração do condomínio, o sistema fornecerá um controle claro sobre o inventário, o histórico de empréstimos, a aplicação de multas por atraso e a identificação dos itens mais utilizados.

## Integrantes da Equipe
- Alessandro Hallisson Alves de Lima
- Elaine Cristina dos Santos Oliveira Holanda
- Lucas Kamel Souza Silva
- Rodrigo Costa Monteiro

## SGBD Escolhido
[SQLite](https://sqliteonline.com "Optional Title")
    
## Link para o Repositório
[DB](https://github.com/hallslima/equipe-empresta-ai/tree/main/db "Optional Title")

---

## Estrutura do Banco de Dados

### Modelo Lógico (Refinado)

<img width="924" height="626" alt="image" src="https://github.com/user-attachments/assets/fcdd9b17-9c52-4fe5-b015-4aef3c70028a" />

* **Entidades:**
    * `CONDOMINIO`: Armazena os dados cadastrais de cada condomínio.
    * `MORADOR`: Mantém o cadastro dos moradores, vinculados a um condomínio.
    * `ITEM`: Catálogo de ferramentas e itens disponíveis para empréstimo, com seu valor de perda e status de disponibilidade. Cada item pertence a um condomínio.
    * `EMPRESTIMO`: Registra a transação de empréstimo, vinculando um `morador`, um `item`, e as datas de retirada e devolução.

* **Relacionamentos Principais:**
    * Um `CONDOMINIO` possui vários `MORADORES`.
    * Um `CONDOMINIO` possui vários `ITENS`.
    * Um `MORADOR` pode realizar vários `EMPRESTIMOS`.
    * Um `ITEM` pode estar em vários `EMPRESTIMOS` (em momentos diferentes).

*(A imagem do diagrama ER atualizado, refletindo os refinamentos, seria inserida aqui.)*

### Scripts SQL

O projeto é composto pelos seguintes scripts:

1.  **`01_criacao_tabelas.sql`**: Comandos `CREATE TABLE` para o modelo refinado, com tipos de dados específicos do SQLite, chaves e constraints.
2.  **`02_insercao_dados.sql`**: Comandos `INSERT INTO` para popular o banco com dados de exemplo, permitindo a execução de consultas realistas.
3.  **`03_consultas.sql`**: Consultas SQL que extraem informações estratégicas para a gestão do condomínio.
