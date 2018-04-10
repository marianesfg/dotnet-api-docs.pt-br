### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal. sizeof e sobrecargas PtrToStructure quebrar o código dinâmico

|   |   |
|---|---|
|Detalhes|A partir do .NET Framework 4.5.1, associando dinamicamente para os métodos <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>, <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>, <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>, ou <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>(via Windows PowerShell, IronPython ou o c# palavra-chave dinâmica, por exemplo) pode resultar em <code>MethodInvocationExceptions</code> porque foram adicionadas novas sobrecargas dos métodos a seguir que pode ser ambígua para os mecanismos de script.|
|Sugestão|Atualize scripts para indicar claramente qual sobrecarga deve ser usada. Normalmente, isso pode ser feito convertendo explicitamente os parâmetros de tipo dos métodos como <xref:System.Type>. Clique [neste link](https://support.microsoft.com/kb/2909958/) para obter mais detalhes e exemplos de como contornar o problema.|
|Escopo|Secundário|
|Versão|4.5.1|
|Tipo|Tempo de execução|

