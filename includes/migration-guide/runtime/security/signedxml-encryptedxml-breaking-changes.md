### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml e EncryptedXml alterações recentes

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2, correções de segurança do <xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name> e <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name> levar a comportamentos de tempo de execução diferentes. Por exemplo,<ul><li>Se um documento tem vários elementos com o mesmo <code>id</code> atributo e uma assinatura tem como alvo um desses elementos como a raiz da assinatura, o documento será agora considerado inválido.</li><li>Documentos usando algoritmos de transformação não canônica XPath nas referências agora são considerados inválidos.</li><li>Usando algoritmos de transformação XSLT não canônica em referências de documentos são agora considere inválido.</li><li>Qualquer programa usa assinaturas de recursos externos desanexado, será possível fazer isso.</li></ul>|
|Sugestão|Desenvolvedores podem querer examinar o uso de <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform> e <xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>, bem como tipos derivados de <xref:System.Security.Cryptography.Xml.Transform> como um destinatário de documento não pode ser capaz de processá-la.|
|Escopo|Secundário|
|Versão|4.6.2|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

