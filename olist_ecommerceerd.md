| Tabela | PK | Tipo de PK |
| :--- | :--- | :--- |
| customers | customer_id | PK Simples
! orders | order_id | PK Simples
| products | product_id | PK Simples
| sellers | seller_id | PK Simples
| product_category_translation | product_category_name | PK Simples
| order_items | "(order_id, order_item_id)" | PK Composta
| payments | "(order_id, payment_sequential)" | PK Composta
| reviews | review_id | PK Simples
| geolocation | (Nenhuma) | Tabela de atributos geográficos (Sem PK estrita)

| Tabela Origem (FK) | Coluna FK | Tabela Destino (PK) | Coluna PK Destino
| :--- | :--- | :--- | :--- |
| orders | customer_id | customers | customer_id
| products | product_category_name | product_category_translation | product_category_name
| order_items | order_id | orders | order_id
| order_items | product_id | products | product_id
| order_items | seller_id |	sellers | seller_id
| payments | order_id |	orders | order_id
| reviews | order_id |	orders | order_id

 