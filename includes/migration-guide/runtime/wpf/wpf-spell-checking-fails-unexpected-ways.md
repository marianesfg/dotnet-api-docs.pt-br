### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>Falha de verificação ortográfica WPF de maneiras inesperadas

|   |   |
|---|---|
|Detalhes|Isso inclui um número de problemas de verificação ortográfica WPF:<ul><li>Às vezes, gera um verificador de ortografia do WPF <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>Falha de verificação ortográfica WPF com <xref:System.UnauthorizedAccessException> quando os aplicativos são iniciados usando 'Executar como usuário diferente'</li><li>WPF corretor ortográfico incorretamente identifica erros de ortografia palavras compostas como Hausnummer em alemão.</li></ul>|
|Sugestão|Problema #1 - esse problema foi corrigido no .NET Framework 4.6.2 problema n º 2 - WPF verificação ortográfica não tem suporte quando os aplicativos são iniciados usando 'Executar como usuário diferente'. A partir do .NET Framework 4.6.2, aplicativos iniciados dessa maneira não irá falhar inesperadamente - em vez disso, o verificador ortográfico será desabilitado silenciosamente. Problema #3 - esse problema foi corrigido no .NET Framework 4.6.2.|
|Escopo|Microsoft Edge|
|Versão|4.6.1|
|Tipo|Tempo de execução|

