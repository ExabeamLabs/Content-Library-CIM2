#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-601
  Conditions = [ """LogType="WLS"""", """EventID="601"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """TargetUserName ="+(-|({dest_user}[^"]+))"""",
    """SubjectDomainName ="+(-|({src_domain}({domain}[^"]+)))"""",
    """TargetDomainName ="+(-|({dest_domain}[^"]+))"""",
    """IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    """Computer="+({dest_host}({host}[\w\-.]+))"""",
    """SubjectUserName ="+(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  ]


}
```