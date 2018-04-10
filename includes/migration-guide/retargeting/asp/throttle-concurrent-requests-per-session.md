### <a name="throttle-concurrent-requests-per-session"></a>Limitação de solicitações simultâneas por sessão

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2 e anteriores, ASP.NET executa solicitações com a mesma Sessionid sequencialmente, e ASP.NET sempre emite Sessionid por meio de cookies por padrão. Se uma página leva muito tempo para responder, ele prejudicará significativamente o desempenho do servidor apenas pressionando F5 no navegador. A correção, adicionamos um contador para controlar as solicitações em fila e as solicitações de término quando eles excedem um limite especificado. O valor padrão é 50. Se o limite for atingido, um aviso será registrado no evento de log e uma resposta HTTP 500 podem ser gravadas no log do IIS.|
|Sugestão|Para restaurar o comportamento antigo, você pode adicionar a seguinte configuração ao arquivo web.config para recusar o novo comportamento.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|

