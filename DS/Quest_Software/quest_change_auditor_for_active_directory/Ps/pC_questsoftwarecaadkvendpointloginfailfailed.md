#### Parser Content
```Java
{
Name = "questsoftware-caad-kv-endpoint-login-fail-failed"
  ParserVersion = "v1.0.0"
  Vendor = "Quest Software"
  Product = "Quest Change Auditor for Active Directory"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
"""Quest Software"""
"""Change Auditor"""
"""|Logon Activity|User failed to authenticate through"""
"""categoryOutcome=Failed""" 
]
  Fields = [
"""dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdomain=({domain}[^\s]+)"""
"""\sevent=({event_name}[^=]+)\s\w+="""
"""logonFailureReason=({failure_reason}[^=]+)\s\w+="""
"""dvchost=({host}[^\s]+)"""
"""logonType=({login_type}\d+)"""
"""categoryOutcome=({result}[^\s]+)"""
"""shost=({src_host}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sstart=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
"""\suser=(({domain}[^\\=]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""userPrincipalName =(({email_address}[^\s=@]+@[^@\s=]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""userMail=({email_address}[^\s=@]+@[^@\s=]+)"""
"""suid=({user_sid}[^\s]+)"""
  ]


}
```