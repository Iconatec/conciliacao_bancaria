# Conciliação Bancária — VBA
Macro `conciliar_banco` para limpar relatórios contábeis e financeiros e gerar uma aba `RESUMO` com os saldos consolidados por filial e agente.
## Estrutura necessária
A pasta de trabalho ativa deve conter:
| Aba | Finalidade |
|---|---|
| `contabilidade` | Razão por agente, extraído da holding |
| `financeiro` | Relatório saldos |
| `proc` | Tabela auxiliar de filiais X contas |
### Mapeamentos da aba proc
| Coluna | Conteúdo |
|---|---|
| A | Identificação completa da filial, conforme o relatório financeiro |
| C | Código da filial |
| F | Conta utilizada no resumo |
| G | Chave `Filial-Agente` para localizar a conta |
Exemplo de identificação na coluna A: `Filial: SCP - PORTO BELLO_ALM`.

## Como utilizar
1. Prepare os relatórios originais nas abas `contabilidade` e `financeiro`.
2. Confira os mapeamentos da aba `proc`.
3. Execute `Formatar relatório e gerar resumo`, botão está na aba Proc.
4. Revise os saldos e diferenças na aba `RESUMO`.
5. Preencha os valores de extrato na coluna E para comparar as três fontes, utilize PROCX (pela conta ou pelo agente), para trazer os saldos dos extratos de outra planilha.
## Cuidados
- Não execute novamente sobre relatórios já tratados. Para atualizar apenas o resumo utilize o botão "Gerar resumo"
- O código depende do formato e da sequência dos registros de conta, filial, banco e agente.
