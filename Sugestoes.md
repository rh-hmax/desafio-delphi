## Classes
É muito importante desenvolver os métodos em classes apropriadas em vez de escrever direto nos formulários. 
Então segue a **sugestão** de classes para desenvolvimento:

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