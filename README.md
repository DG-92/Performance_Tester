# BlazeDemo Performance Test com JMeter

Este projeto contém um teste de performance automatizado para o cenário de compra de passagem aérea no [BlazeDemo](https://www.blazedemo.com), utilizando Apache JMeter.

## Cenário Testado

- Compra completa de passagem aérea (Boston → London)
- Simulação de 250 requisições por segundo

## Critério de Aceitação

- 90% das respostas abaixo de 2 segundos (p90 < 2s)

## Como executar

1. Instale o [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi)
2. Instale o plugin [Throughput Shaping Timer](https://jmeter-plugins.org/wiki/ThroughputShapingTimer/)
3. Abra o arquivo `scripts/blazedemo_purchase.jmx` no JMeter
4. Execute o teste:
   - Para teste de carga: mantenha 250 req/s por 2 minutos
   - Para teste de pico: aumente rapidamente para 500 req/s por 30 segundos e volte para 250 req/s

5. Gere o relatório HTML:
   - Menu: `Run > Generate HTML Report`
   - Salve em `results/load_test_report.html` ou `results/spike_test_report.html`

## Relatório de Execução

Veja os arquivos em `results/` para detalhes da execução.

### Exemplo de resultado:
<img width="1164" height="765" alt="image" src="https://github.com/user-attachments/assets/c51c24ba-648c-4750-b9b3-0301a61af245" />
<img width="1169" height="320" alt="image" src="https://github.com/user-attachments/assets/f7db64f7-d2e9-4b26-99e8-9ac54cb0016b" />
