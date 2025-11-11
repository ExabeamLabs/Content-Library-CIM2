#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-3"
Conditions = [
"""LogType="WLS""""
"""EventID="4776""""
]
ParserVersion = "v1.0.0"

windows-events-wls.Fields}[
    """TargetUserName ="+(-|({dest_user}[^"]+))"""",
    """SubjectDomainName ="+(-|({src_domain}({domain}[^"]+)))"""",
    """TargetDomainName ="+(-|({dest_domain}[^"]+))"""",
    """IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    """Computer="+({dest_host}({host}[\w\-.]+))"""",
    """SubjectUserName ="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  ]
 },

${WindowsParsersTemplates.windows-events-wls} {
  Name = microsoft-evsecurity-kv-endpoint-login-success-552
  Product = "Event Viewer - Security"
  Conditions = [ """LogType="WLS"""", """EventID="552"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """TargetUserName ="+(-|({dest_user}[^"]+))"""",
    """SubjectDomainName ="+(-|({src_domain}({domain}[^"]+)))"""",
    """TargetDomainName ="+(-|({dest_domain}[^"]+))"""",
    """IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    """Computer="+({dest_host}({host}[\w\-.]+))"""",
    """SubjectUserName ="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  
}
```