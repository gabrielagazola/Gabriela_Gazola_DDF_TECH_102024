# Coleção Criada

![Captura de Tela (401)](https://github.com/user-attachments/assets/d2e85379-07c5-4123-8b6b-0e107df624ee)

# Queries SQL

## Perguntas

**5 Clientes com mais Gastos**
```sql
SELECT c.CUSTOMER_ID AS cliente_id,
       SUM(oi.PRICE) AS total_gasto
FROM TB__RR5ITM__OLIST_CUSTOMERS_DATASET c

INNER JOIN TB__G5XZTE__OLIST_ORDERS_DATASET o ON c.CUSTOMER_ID = o.CUSTOMER_ID
INNER JOIN TB__F9IDKT__OLIST_ORDER_ITEMS_DATASET oi ON o.ORDER_ID = oi.ORDER_ID
GROUP BY c.CUSTOMER_ID
ORDER BY total_gasto DESC
LIMIT 5;
```

![5 Clientes com mais Gastos-17_10_2024, 18_52_05](https://github.com/user-attachments/assets/9ee24ea6-b0a1-4f30-8a08-60f53384d6c5)

**Número de clientes por estado**

```sql
SELECT customer_state, COUNT(customer_id) AS number_of_customers
FROM TB__RR5ITM__OLIST_CUSTOMERS_DATASET
GROUP BY customer_state
ORDER BY number_of_customers DESC;
```
![Número de clientes por estado-17_10_2024, 18_55_39](https://github.com/user-attachments/assets/7afa96c9-c47e-4d01-8dba-2493c55f33e1)

**Total Vendas Produto**

```sql
SELECT product_id, SUM(price) AS total_sales
FROM TB__F9IDKT__OLIST_ORDER_ITEMS_DATASET
GROUP BY product_id
ORDER BY total_sales DESC;
```

![Captura de Tela (398)](https://github.com/user-attachments/assets/a017793c-dec2-4311-bc42-f8294d2079e0)

**Valor Médio do Frete por Estado**

```sql
SELECT 
    c.customer_state, 
    AVG(oi.freight_value) AS average_freight
FROM 
    TB__F9IDKT__OLIST_ORDER_ITEMS_DATASET AS oi
JOIN 
    TB__G5XZTE__OLIST_ORDERS_DATASET AS o 
ON 
    oi.order_id = o.order_id
JOIN 
    TB__RR5ITM__OLIST_CUSTOMERS_DATASET AS c 
ON 
    o.customer_id = c.customer_id
GROUP BY 
    c.customer_state
ORDER BY 
    average_freight DESC;
```

![Valor Médio do Frete por Estado-17_10_2024, 19_00_04](https://github.com/user-attachments/assets/eaf23927-d937-4d3b-aca8-94b57c2f590f)

**Vendas Por Período (Mensal)**

```sql
**SELECT DATE_TRUNC('month', CAST(shipping_limit_date AS DATE)) AS month, SUM(price) AS total_sales
FROM TB__F9IDKT__OLIST_ORDER_ITEMS_DATASET
GROUP BY month
ORDER BY month;
```

![Vendas Por Período (Mensal)-17_10_2024, 19_01_24](https://github.com/user-attachments/assets/a4658e0c-578b-4087-8061-192fd6a54ac4)


## DashBoard

![Captura de Tela (399)](https://github.com/user-attachments/assets/6873f870-c935-42bf-bcbb-faf2e5679c9b)
![Captura de Tela (400)](https://github.com/user-attachments/assets/02821ffb-a2fa-4e57-b216-cecd15f510a2)



