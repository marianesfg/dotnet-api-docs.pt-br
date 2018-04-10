### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException gerada pelo verificador ortográfico do WPF

|   |   |
|---|---|
|Detalhes|Aplicativos WPF ocasionalmente falhar durante o desligamento do aplicativo com um <xref:System.ObjectDisposedException?displayProperty=name> gerada pelo verificador ortográfico. Isso foi corrigido no .NET 4.7 WPF pelo tratamento da exceção normalmente e garantindo que os aplicativos são afetados negativamente não. Observe que as exceções de primeira chance ocasionais continuará a ser observado em aplicativos em execução em um depurador.|
|Sugestão|Atualizar para o .NET 4.7|
|Escopo|Microsoft Edge|
|Versão|4.6.1|
|Tipo|Tempo de execução|

