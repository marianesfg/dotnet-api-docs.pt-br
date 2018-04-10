### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Não há mais capaz de definir o EnableViewStateMac como false

|   |   |
|---|---|
|Detalhes|O ASP.NET não permite mais que os desenvolvedores especifiquem <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> ou <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. O MAC (Message Authentication Code) de estado da exibição agora é obrigatório em todas as solicitações com estado de exibição embutido. Somente os aplicativos que definam explicitamente a propriedade EnableViewStateMac como <code>false</code> são afetados.|
|Sugestão|EnableViewStateMac deve ser considerada true e os erros resultantes de MAC devem ser resolvidos (conforme explicado em [neste guia](https://support.microsoft.com/kb/2915218), que contém várias resoluções dependendo das especificações da causa erros de MAC).|
|Escopo|Principal|
|Versão|4.5.2|
|Tipo|Tempo de execução|

