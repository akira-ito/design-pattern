# Outbox Pattern

Garante atomicidade em sistema distribuido. Ao utilizar o padrão SAGA ou Event Domain, pode haver uma indisponibilidade por parte do borken ou falha no sistema durante a comunicação com outros microserviços após os dados serem persistido.

Neste cenário, os dados e o(s) evento(s) são persistidos no banco na mesma transação(assim garantindo Atomicidade) porem em tabelas distintas(é recomendado que se tenha uma tabela especifica com seu payload para o Outbox Pattern), e um CRON/POLLING ou CGC(Change Data Capture) para que envie o evento ao broken.

## Related

- SAGA pattern

## Change Data Capture

Processo para identificar as alterações de Banco de dados.

**WAL (Write-Ahead Log)**: PostgreSQL, Cassandra, etc

- [Debezium](https://debezium.io/): Projeto open source que faz o stream (Kafka) das modificações em diferentes BD.