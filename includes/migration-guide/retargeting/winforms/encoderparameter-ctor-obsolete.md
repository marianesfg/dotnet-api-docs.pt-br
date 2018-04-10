### <a name="encoderparameter-ctor-is-obsolete"></a>EncoderParameter construtor está obsoleto

|   |   |
|---|---|
|Detalhes|O construtor <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> agora está obsoleto e introduzirá novos avisos de compilação se for usado.|
|Sugestão|Embora o <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>construtor continuarão a funcionar, o seguinte construtor deve ser usado em vez disso, para evitar o aviso de compilação obsoleto ao compilar novamente o código com as ferramentas do .NET 4.5: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

