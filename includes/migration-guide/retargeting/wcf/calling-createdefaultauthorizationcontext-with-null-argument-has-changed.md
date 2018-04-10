### <a name="calling-createdefaultauthorizationcontext-with-a-null-argument-has-changed"></a>Chamando CreateDefaultAuthorizationContext com um argumento nulo foi alterado

|   |   |
|---|---|
|Detalhes|A implementação do <xref:System.IdentityModel.Policy.AuthorizationContext?displayProperty=name> retornado por uma chamada para o <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=name> com um nulo authorizationPolicies argumento mudou sua implementação no .NET Framework 4.6.|
|Sugestão|Em casos raros, os aplicativos WCF que usam a autenticação personalizada podem ver diferenças de comportamento. Nesses casos, o comportamento anterior pode ser restaurado de uma destas duas maneiras:<ol><li>Recompile o aplicativo para se destinar a uma versão anterior ao .NET Framework 4.6. Para serviços hospedados no IIS, use o &lt;httpRuntime targetFramework =&quot;x&quot;  / &gt; elemento para uma versão anterior do .NET Framework de destino.</li><li>Adicione a seguinte linha à seção <code>&lt;appSettings&gt;</code> de seu arquivo app.config: <code>&lt;add key=&quot;appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext&quot; value=&quot;true&quot; /&gt;</code></li></ol>|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext(System.Collections.Generic.IList{System.IdentityModel.Policy.IAuthorizationPolicy})?displayProperty=nameWithType></li></ul>|

