### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Chamadas para System.Windows.Input.PenContext.Disable em sistemas sensível podem gerar ArgumentException

|   |   |
|---|---|
|Detalhes|Em algumas circunstâncias, chamadas para interno <strong>System.Windows.Intput.PenContext.Disable</strong> método em sistemas sensível pode lançar sem tratamento <code>T:System.ArgumentException</code> devido à reentrância.|
|Sugestão|Esse problema foi resolvido no .NET Framework 4.7. Para evitar a exceção, atualize para uma versão do .NET Framework, começando com o .NET Framework 4.7.|
|Escopo|Microsoft Edge|
|Versão|4.6.1|
|Tipo|Redirecionando|

