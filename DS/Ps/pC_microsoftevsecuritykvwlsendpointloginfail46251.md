#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-wls-endpoint-login-fail-4625-1"
Conditions = [
"""LogType="WLS""""
"""EventID="4625""""
]
ParserVersion = "v1.0.0"

json-windows-events-3.Fields}[
    """"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"Computer":"({dest_host}({host}[^"]+))"""",
    """({event_name}A network share object was checked to see whether the client can be granted desired access)""",
    """"ObjectType":"({file_type}[^"]+)""",
    """"ShareName":"(?:[\\\*]+)?({share_name}[^"]+)""",
    """"ShareLocalPath":"(?:[\\\?]+)?(|({share_path}(({d_parent}.+?)\\\\)?(|({d_name}[^\\]*?)))\\?)"""",
    """"RelativeTargetName"+:"+({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\:"]+?(\.\s*({file_ext}[^"\\.]+?))?)"""",
    """AccessList"+:"+({access}[^"]+?)(\s(\\t){1,4})?""""
  
}
```