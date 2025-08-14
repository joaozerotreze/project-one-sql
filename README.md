Esquema Conceitual de E-commerce
Este repositório apresenta o modelo conceitual para um sistema de e-commerce, desenvolvido com base no modelo Entidade-Relacionamento Estendido (EER). O modelo contempla os principais requisitos para um ambiente de vendas online, incluindo os conceitos de clientes (Pessoa Física e Jurídica), produtos, vendedores externos, estoque, fornecedores, pedidos, pagamentos e entregas.

📦 Contexto do Projeto
O objetivo deste esquema é representar as regras, entidades e relacionamentos essenciais para o desenvolvimento de sistemas de comércio eletrônico, permitindo o armazenamento estruturado e seguro das informações relacionadas às operações comerciais.

Principais destaques do modelo:

Cliente pode ser Pessoa Física ou Pessoa Jurídica, garantido por especialização exclusiva.

Produtos são cadastrados, relacionados a fornecedores, vendedores e controle de estoque.

Pedidos podem conter diversos produtos e registram dados de entrega, pagamento e situação.

Pagamentos e formas de pagamento permitem múltiplas opções e cadastro vinculado ao cliente.

O sistema contempla entrega com status e rastreamento, integrando todo o ciclo da venda.

Entidades como Fornecedor, Vendedor Externo, Estoque e Categoria estruturam os dados do produto.

🗂 Principais Entidades
Cliente: idCliente, nome, endereço, tipo (PF/PJ)

Pessoa Física: CPF

Pessoa Jurídica: CNPJ

Empresa: dados cadastrais vinculados ao Cliente

Produto: idProduto, categoria, preço

Fornecedor/Supplier: idSupplier, razão social, CNPJ

Estoque: localização, quantidade

Pedido: status, descrição, shipping, relação com Cliente, Pessoa, Empresa

Item Pedido (Order_has_Product): produtos por pedido, quantidade

Pagamento: tipo, dados de cartão, Pix, etc.

Entrega: status, tracking, relação com pedido

🔗 Relacionamentos Principais
Cliente pode ser PF ou PJ, nunca ambos.

Cliente pode ter múltiplas formas de pagamento.

Pedido vinculado ao Cliente (PF, PJ ou Empresa); pedido contém produtos.

Produto está vinculado a fornecedores, vendedores e estoque.

Pedido gera entrega, que tem status e rastreamento associado.

Pagamentos podem ter diferentes formas vinculadas ao Cliente.

Outros Vendedores podem ofertar produtos (marketplace).

🔐 Regras de Negócio Modeladas
Conta do cliente: exclusiva para PF ou PJ.

Controle de estoque por localização.

Produtos podem ser vendidos por diferentes vendedores ou fornecedores.

Pagamento flexível: cartão, pix, boleto.

Entrega sempre tem status e código de rastreio.

Pedido pode ter diferentes tipos de clientes (individual ou empresa).

📝 Observações de Modelagem
Chaves primárias e estrangeiras (PK/FK) foram representadas para facilitar futuras implementações, conforme exigido por ferramentas como MySQL Workbench ou DBDesigner.

O diagrama segue o padrão EER e pode ser facilmente adaptado para modelagem física ou implementação em SGBDs relacionais.

📎 Estrutura do Repositório
ecommerce.mwb ou arquivo do diagrama (se disponível)

Exportação do diagrama em .png ou .pdf

Este README com explicações e contexto