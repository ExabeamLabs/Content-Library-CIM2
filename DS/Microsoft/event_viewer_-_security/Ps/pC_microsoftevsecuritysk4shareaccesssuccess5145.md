#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-share-access-success-5145
  ParserVersion = v1.0.0
  Conditions = [ """"Activity":"5145 - A network share object was checked to see whether the client can be granted desired access."""", """"EventID":"5145"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-3.Fields}[
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
  ]

json-windows-events-3 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Fields = [
    """"EventID":"?({event_code}\d+)"?""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  
}
```