Usando a indexação baseada em caractere com o <xref:System.Text.StringBuilder.Chars%2A> propriedade pode ser extremamente lenta sob as seguintes condições:

- O <xref:System.Text.StringBuilder> instância for grande (por exemplo, ele consiste em várias dezenas de milhares de caracteres).
- O <xref:System.Text.StringBuilder> é "robustos". Ou seja, repetidas chamadas para métodos como <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> ter expandido automaticamente o objeto <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> propriedade e partes de novo alocadas da memória para ela.

É o desempenho gravemente impactado porque acesso cada caractere orienta toda a lista vinculada de blocos para localizar o buffer correto ao qual indexar.

> [!NOTE]
>  Mesmo para um grande "robustos" <xref:System.Text.StringBuilder> do objeto, usando o <xref:System.Text.StringBuilder.Chars%2A> propriedade baseada em índice acesso a um ou um pequeno número de caracteres tem um impacto no desempenho insignificante; normalmente, é um **0(n)** operação. O impacto de desempenho significativa ocorre quando se itera os caracteres no <xref:System.Text.StringBuilder> objeto, que é um **O(n^2)** operação. 

Se você encontrar problemas de desempenho ao usar a indexação baseada em caractere com <xref:System.Text.StringBuilder> objetos, você pode usar qualquer uma das seguintes alternativas:

- Converter o <xref:System.Text.StringBuilder> instância para uma <xref:System.String> chamando o <xref:System.Text.StringBuilder.ToString%2A> método, acesse os caracteres na cadeia de caracteres.

- Copie o conteúdo existente <xref:System.Text.StringBuilder> um novo objeto dimensionados previamente <xref:System.Text.StringBuilder> objeto. Melhora o desempenho porque o novo <xref:System.Text.StringBuilder> o objeto não é robusto. Por exemplo:

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Definir a capacidade inicial do <xref:System.Text.StringBuilder> objeto como um valor que é aproximadamente igual ao tamanho máximo esperado chamando o <xref:System.Text.StringBuilder.%23ctor(System.Int32)> construtor. Observe que isso aloca o bloco inteiro se até mesmo de memória a <xref:System.Text.StringBuilder> raramente atingir sua capacidade máxima.
