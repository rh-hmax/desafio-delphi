# CRUD de Produtos para Loja
## História
Fazendo o uso de classes e orientação à objeto, precisamos de uma aplicação para manter produtos categorizados de uma loja genérica.
### Requisitos funcionais
	- Como usuário gostaria de adicionar um novo produto ao catálogo da loja
	- Como usuário gostaria de editar um produto existente no catálogo
	- Como usuário gostaria de remover o produto do meu catálogo da loja
	- Como usuário gostaria de recuperar uma lista com os produtos disponíveis
	- Como usuário gostaria de buscar produtos pela sua descrição
	- Como usuário gostaria de filtrar os produtos por uma categoria específica
### Requisitos não funcionais
    - É preciso haver uma classe para produto
    - A inclusão de produto deve utilizar a classe de produto
    - Para conexão com o banco de dados, deve-se utilizar o Firedac ou DBExpress
    - Pode-se utilizar qualquer banco de dados compatível com Firedac ou DBExpress
### Entrega do desafio
	- Um repositório GitHub
### Critérios de avaliação
	- Entendimento dos requisitos
	- Organização e estrutura de arquivos
	- Padrão de escrita do código
	- Capacidade de aprender
# Mais detalhes
O desafio consiste em realizar um CRUD(Create, Read, Update e Delete) de produtos e filtrá-los conforme suas **categorias**.
## Tabelas
Para o desafio será preciso criar 2 tabelas:

Tabela: **PRODUTO**
| Campo | Tipo | Descrição |
|---|---|---|
| ID | Integer (Chave primária) | Código do produto |
| DESCRICAO | Varchar(50) | Nome/Descrição do produto |
| ID_CATEGORIA | Integer (Chave estrangeira) | Código da categoria na tabela **Categoria** |
| PRECO | Double | Preço do produto

Tabela: **CATEGORIA**
| Campo | Tipo | Descrição |
|---|---|---|
| ID | Integer (Chave primária) | Código da categoria do produto |
| DESCRICAO | Varchar(50) | Nome da categoria de produto. |
| VALOR | Double | Preço do produto |

## Classes
É muito importante desenvolver os métodos em classes apropriadas em vez de escrever direto nos formulários. Então segue a **sugestão** de classes para desenvolvimento:

### TProduto
#### Atributos
- Id: integer
- Descricao: string;
- Valor: Currency
- Categoria: TCategoria

#### Métodos
A classe TProduto deve ter ao menos o método abaixo:
- **Salvar**: Responsável por persistir ou acionar a persistência no banco de dados, as informações carregadas na classe.
### **TCategoria**
#### Atributos
- Id: integer
- Descricao: string;

#### Métodos
Não há método obrigatório para esta classe.

# Formulários/Telas
Fique a vontade para elaborar os formulários como lhe parecer melhor.
Abaixo seguem apenas sugestões visando facilitar a criação.

### Formulário Principal
    - Grid: Listando todos os produtos com ID do produto, Descrição do produto, Descrição da categoria e o valor do produto.
    - Botão Novo: para abrir o formulário de produto
    - Botão Editar: para abrir o formulário de produto, já com as informações do produto selecionado no grid.
    - Botão Deletar: para remover um produto selecionado no grid, mediante a confirmação do usuário.
### Formulário de Produto
    - Descrição : Campo para informar o nome do produto
    - Categoria : Campo TCombobox com a lista de categorias cadastradas.
    - Valor: Campo para informar o preço de venda do produto
    - Botão Salvar : Responsável por chamar o método da classe TProduto e persistir os dados no banco de dados

Para diminuir o desafio, os dados da tabela Categoria **não precisam** ser incluídos pela aplicação, mas podem ser inseridos direto no banco de dados.