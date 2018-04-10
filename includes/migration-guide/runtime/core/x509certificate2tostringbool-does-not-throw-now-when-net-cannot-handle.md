### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) não gerará agora quando .NET não pode tratar o certificado

|   |   |
|---|---|
|Detalhes|Anteriormente, esse método lançaria se <code>true</code> foi passado para o parâmetro verbose e houve certificados instalados que não têm suporte pelo .NET Framework. Agora, o método será bem-sucedida e retornar uma cadeia de caracteres válida que omite as partes inacessíveis do certificado.|
|Sugestão|Qualquer código dependendo <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> devem ser atualizadas para esperar que a cadeia de caracteres retornada pode excluir alguns dados de certificado (como a chave pública, a chave privada e extensões) em alguns casos em que a API teria lançado anteriormente.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

