### <a name="wpf-textboxtext-can-be-out-of-sync-with-databinding"></a>WPF TextBox. Text pode estar fora de sincronia com associação de dados

|   |   |
|---|---|
|Detalhes|Em alguns casos, a propriedade <xref:System.Windows.Controls.TextBox.Text> reflete um valor anterior do valor da propriedade vinculada se a propriedade é modificada durante uma operação de escrita de vinculação de dados.|
|Sugestão|Isso não deve ter nenhum impacto negativo. No entanto, é possível restaurar o comportamento anterior ao definir a propriedade <xref:System.Windows.FrameworkCompatibilityPreferences.KeepTextBoxDisplaySynchronizedWithTextProperty> como <code>false</code>.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.TextBox.Text?displayProperty=nameWithType></li></ul>|

