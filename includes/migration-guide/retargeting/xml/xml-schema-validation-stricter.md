### <a name="xml-schema-validation-is-stricter"></a>Validação de esquema XML é mais rígida

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.5, validação de esquema XML é mais restrito. Se você usar xsd:anyURI para validar um URI como um protocolo mailto, a validação falhará se houver espaços no URI. Nas versões anteriores do .NET Framework, a validação foi bem-sucedida. A alteração afeta somente os aplicativos que visam o .NET Framework 4.5.|
|Sugestão|Se menos rígida validação do .NET Framework 4.0 é necessário, o aplicativo de validação pode direcionar a versão 4.0 do .NET Framework. No entanto, quando o redirecionamento para o .NET 4.5, revisão de código deve ser feita para certificar-se de que os URIs inválido (com espaços) não são esperados como valores de atributo com o tipo de dados anyURI.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Redirecionando|

