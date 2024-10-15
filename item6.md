# Modelagem de Dados

Será utilizado o **Modelo Dimensional de Kimball**, que é muito comum para ambientes de Data Warehouse e focado em facilitar a consulta e a análise de dados. A modelagem será composta por **Fatos** e **Dimensões**, permitindo uma visão clara e acessível dos dados.

## Modelagem Proposta 

### 1. Tabela de Fatos: `olist_orders`

A tabela de fatos irá conter as métricas de vendas. Os principais atributos desta tabela são:

- `order_id` (Primary Key)
- `customer_id` (Foreign Key)
- `product_id` (Foreign Key)
- `order_purchase_timestamp` (Foreign Key)
- `order_status`
- `payment_value`
- `freight_value`
- `total_order_value`

### 2. Tabelas de Dimensões

#### Dimension: `olist_customers`

- `customer_id` (Primary Key)
- `customer_unique_id`
- `customer_city`
- `customer_state`
- `customer_zip_code_prefix`
- `customer_address`
- `customer_email`
- `customer_phone`

#### Dimension: `olist_products`

- `product_id` (Primary Key)
- `product_category_name`
- `product_name`
- `product_description`
- `product_weight`
- `product_length`
- `product_height`
- `product_width`
- `product_price`

#### Dimension: `olist_order_dates`

- `order_purchase_timestamp` (Primary Key)
- `order_year`
- `order_month`
- `order_day`
- `order_weekday`

#### Dimension: `olist_order_status`

- `order_status_id` (Primary Key)
- `order_status_description` (e.g., 'Aguardando Pagamento', 'Enviado', 'Entregue', 'Cancelado')

## 1 - Visões Finais dos Dados
 
### Visão de Vendas por Cliente

**Objetivo**: Permitir que os gestores analisem o desempenho de vendas de acordo com diferentes clientes.

**Atributos**: 
- `customer_unique_id`
- `customer_email`
- `total_orders`
- `total_payment_value`
- `last_order_date`

### 2 - Visão de Vendas Mensais por Produto

**Objetivo**: Analisar o desempenho de vendas mensais de produtos para entender quais são mais populares em diferentes meses.

**Atributos**: 
- `product_name`
- `order_month`
- `order_year`
- `total_sold`
- `total_quantity`

As visões finais propostas permitem uma análise aprofundada do desempenho de vendas, tanto em relação aos clientes quanto aos produtos, facilitando a tomada de decisões estratégicas para o negócio.
