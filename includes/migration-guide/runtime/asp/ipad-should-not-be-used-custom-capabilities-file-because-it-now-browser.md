### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad não deve ser usado no arquivo de recursos personalizados como agora é um recurso do navegador

|   |   |
|---|---|
|Detalhes|A partir do .NET 4.5, iPad é um identificador no arquivo de recursos de navegador padrão ASP.NET, portanto ele não deve ser usado em um arquivo de recursos personalizados|
|Sugestão|Se recursos específicos do iPad forem necessários, é necessário modificar o comportamento de iPad definindo recursos sobre o gateway predefinido refID &quot;IPad&quot; em vez de gerar um novo &quot;IPad&quot; ID pelo agente do usuário correspondência.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|

