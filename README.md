# Hoffmeister Candles

Indicador Pine Script (TradingView, `@version=6`) que sobrepõe velas de outros
timeframes diretamente no gráfico atual — útil para acompanhar contexto
multi-timeframe (MTF) sem trocar de aba.

- **5 slots independentes**, cada um com timeframe livre (`input.timeframe`,
  não fixo).
- Cada slot define uma faixa de timeframes do gráfico em que ele fica visível
  (`showFrom` / `showTo`), evitando poluir o chart em timeframes onde não faz
  sentido.
- Cores, espessura de borda e de pavio configuráveis por slot.
- Desenhado para ocupar o 2º slot de indicadores do plano free do TradingView
  (é um indicador separado do [Hoffmeister ICT](https://github.com/MarceloHoffmeister/hoffmeister-ict)).

## Instalação no TradingView

1. Abra o [Pine Editor](https://www.tradingview.com/pine-editor/) no
   TradingView.
2. Crie um novo indicador em branco.
3. Copie e cole o conteúdo de
   [`hoffmeister_candles.pine`](hoffmeister_candles.pine).
4. Clique em **Add to chart**.
5. Configure cada slot (timeframe, faixa de exibição e cores) pelo painel de
   inputs do indicador.

## Configuração padrão dos slots

| Slot | Timeframe padrão | Visível entre |
|------|-------------------|----------------|
| 1 | 1W | 1m – 1D |
| 2 | 1D | 1m – 4H |
| 3 | 1H | 1m – 45m |
| 4 | 15m | 1m – 5m |
| 5 | 5m | 1m – 4m |
