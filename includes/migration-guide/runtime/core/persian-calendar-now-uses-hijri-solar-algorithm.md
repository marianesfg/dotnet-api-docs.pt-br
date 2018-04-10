### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>Calendário persa agora usa o algoritmo solar islâmico

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.6, a <xref:System.Globalization.PersianCalendar?displayProperty=name> classe usa o algoritmo solar islâmico. Converter datas entre a <xref:System.Globalization.PersianCalendar?displayProperty=name> e outros calendários podem produzir um resultado ligeiramente diferente que começa com o .NET Framework 4.6 para datas anteriores a 1800 ou posteriores 2023 (Gregoriano). Além disso, <xref:System.Globalization.PersianCalendar.MinSupportedDateTime> agora é <code>March 22, 0622 instead of March 21, 0622</code>.|
|Sugestão|Lembre-se de que algumas datas anteriores ou posteriores podem ser ligeiramente diferentes quando se usa o PersianCalendar no .NET 4.6. Além disso, ao serializar datas entre processos que podem ser executados em diferentes versões do .NET Framework, não armazene-as como cadeias de caracteres de data PersianCalendar (uma vez que esses valores podem ser diferentes).|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

