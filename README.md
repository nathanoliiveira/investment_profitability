# Automação Python para Acompanhamento de Rentabilidade de Carteira de Investimentos

Este projeto utiliza Python para calcular a rentabilidade de uma carteira de investimentos, com base nas cotações históricas de ações. Além disso, compara o desempenho da carteira com o índice IBOVESPA (IBOV), facilitando o monitoramento em tempo real e permitindo ajustes rápidos para otimizar os resultados.

## Dependências

Este script utiliza as seguintes bibliotecas:

- **pandas**: Para manipulação de dados tabulares.
- **yfinance**: Para obter cotações históricas das ações.

Você pode instalar essas dependências com o comando:

```bash
pip install pandas yfinance
```

## Como Funciona

1. **Leitura da Carteira de Investimentos**  
   O script começa lendo os ativos e valores da carteira a partir de um arquivo de texto (`carteira.txt`). Cada linha do arquivo contém o código da ação (ticker) e a quantidade de ações adquiridas, separados por um hífen (`-`).

   Exemplo de conteúdo do arquivo `carteira.txt`:
   ```
   ITUB4 - 1000
   BBAS3 - 2000
   VALE3 - 1000
   EGIE3 - 500
   SLCE3 - 300
   ```

2. **Obtenção das Cotações de Mercado**  
   O script utiliza a biblioteca `yfinance` para baixar as cotações históricas das ações e do índice IBOVESPA (`^BVSP`) entre as datas definidas no código. As cotações são organizadas em uma tabela para fácil manipulação.

3. **Cálculo da Rentabilidade**  
   A rentabilidade de cada ativo é calculada com base no preço inicial e final da ação dentro do período definido. A rentabilidade total da carteira é ponderada pela quantidade de ações de cada ativo.

4. **Comparação com o Índice IBOVESPA**  
   A rentabilidade da carteira é comparada com a rentabilidade do índice IBOVESPA, proporcionando uma visão clara sobre o desempenho relativo da carteira.

## Exemplo de Saída

Ao rodar o script com a carteira de exemplo, a saída seria:

```
Valor inicial da carteira = 4800.0
Valor final da carteira = 4393.2950646747
Rentabilidade da carteira: -8.5%
Rentabilidade do índice (IBOV): -9.4%
A rentabilidade da carteira superou o IBOV em: 0.9%
```

Neste exemplo, a carteira teve uma rentabilidade negativa de -8.5%, mas superou o índice IBOV, que teve uma rentabilidade de -9.4%. Isso representa uma diferença positiva de 0.9%.

## Personalização

Este script pode ser facilmente personalizado para atender às suas necessidades específicas:

- Modificar o intervalo de datas para análise.
- Ajustar os ativos incluídos na sua carteira.
- Incluir ou excluir o índice IBOVESPA da comparação.

## Conclusão

Essa automação oferece uma maneira eficiente e prática de monitorar o desempenho de carteiras de investimentos. Com este script, você pode obter uma análise rápida da rentabilidade e compará-la com o índice de referência, ajudando a tomar decisões mais informadas sobre ajustes na sua carteira.
