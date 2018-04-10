### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Valores nulos coalescedor não são visíveis no depurador até uma etapa posterior

|   |   |
|---|---|
|Detalhes|Um bug no .NET Framework 4.5 faz com que os valores definidos por meio de uma operação de união nulo não fiquem visíveis no depurador imediatamente após a operação de atribuição é executada quando executando a versão de 64 bits do Framework.|
|Sugestão|Passo a passo de um tempo adicional no depurador fará com que o local/valor do campo a ser atualizado corretamente. Além disso, esse problema foi corrigido no .NET Framework 4.6; atualização para essa versão do Framework deve solucionar o problema.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|

