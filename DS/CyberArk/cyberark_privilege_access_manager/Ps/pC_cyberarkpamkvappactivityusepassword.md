#### Parser Content
```Java
{
Name = "cyberark-pam-kv-app-activity-usepassword"
Conditions = [
"""%CYBERARK:"""
"""Message="Use Password"""
""";Safe="""
]
ParserVersion = "v1.0.0"

s-cyberark-events.Fields}[
    """;UserName ="(|(({domain}[^\s\\"]+)\\+)?({dest_user}[^\s\\"]+))"""",
    """;LogonDomain="(|[\d\.]+|({dest_domain}[^"]+?))"""",
  ]
  ParserVersion = "v1.0.0"
},

${CyberArkParsersTemplates.s-cyberark-events}{
  Name = cyberark-vault-kv-endpoint-login-fail-psm
  Conditions = [ """%CYBERARK:""", """Message="PSM Connect Failed""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields}[
    """;UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))"""",
    """;LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))"""",
  ]
  ParserVersion = v1.0.0
},

${CyberArkParsersTemplates.s-cyberark-events}{
  Name = cyberark-vault-kv-rdp-traffic-success-psmconnect-1
  Conditions = [ """%CYBERARK:""", """Message="PSM Connect"""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields}[
    """;UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))"""",
    """;LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))"""",
  ]
  ParserVersion = v1.0.0
},

${CyberArkParsersTemplates.s-cyberark-events}{
  Name = cyberark-vault-kv-rdp-traffic-success-psmsecure
  Conditions = [ """%CYBERARK:""", """Message="PSM Secure Connect Session Start""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields}[
    """;UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))"""",
    """;LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))"""",
  ]

  ParserVersion = v1.0.0
},

${CyberArkParsersTemplates.s-cyberark-events}{
  Name = cyberark-vault-kv-user-password-modify-fail-changepassword
  Conditions = [ """%CYBERARK:""", """Message="CPM Change Password Failed"""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields} [
    """;UserName ="(|({dest_user}[^"]+))"""",
    """;LogonDomain="(|({dest_domain}[^"]+))"""",
  ]
  DupFields=[ "host->dest_host" ]
  ParserVersion = "v1.0.0"
},

${CyberArkParsersTemplates.s-cyberark-events}{
  Name = cyberark-vault-kv-app-login-logon
  Conditions = [ """%CYBERARK:""", """Message="Logon""", """;Safe=""" ]
  Fields = ${CyberArkParsersTemplates.s-cyberark-events.Fields} [
    """;CPMStatus="(|({result}[^"]+))"""",
    """;Reason="(|({failure_reason}[^"]+))""""
  ]
  DupFields=[ "host->dest_host" ]
  ParserVersion = v1.0.0
}

{
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK"""
"""\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK"""
"""({app}CYBERARK)"""
""";Message="(|({operation}[^"]+?))\s*""""
"""MessageID="({event_code}\d+)"""
""";Issuer="({user}[\w\.\-]{1,40}\$?)"""
""";Station="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""";Safe="(|({safe_value}[^"]+))""""
""";UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))""""
""";LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))""""
""";DeviceType="(|({dest_service_name}[^"]+))""""
""";Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""""
""";UserName ="(|({dest_user}[^"]+))""""
""";LogonDomain="(|({dest_domain}[^"]+))""""
]
Name = "cyberark-pam-kv-user-password-modify-success-cpmpasswordchanged"
Conditions = [
"""%CYBERARK:"""
"""Message="CPM Change Password""""
""";Safe="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK"""
"""\d\d:\d\d:\d\d(Z)? ({host}[\w\-.]+) %CYBERARK"""
"""({app}CYBERARK)"""
""";Message="(|({operation}[^"]+?))\s*""""
"""MessageID="({event_code}\d+)"""
""";Issuer="({user}[\w\.\-]{1,40}\$?)"""
""";Station="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""";Safe="(|({safe_value}[^"]+))""""
""";UserName ="(|(({domain}[^\s\\"]+)\\+)?({account}[^\s\\"]+))""""
""";LogonDomain="(|[\d\.]+|({account_domain}[^"]+?))""""
""";DeviceType="(|({dest_service_name}[^"]+))""""
""";Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""""
""";UserName ="(|({dest_user}[^"]+))""""
""";LogonDomain="(|({dest_domain}[^"]+))""""
]
Name = "cyberark-pam-kv-user-password-reset-success-setpassword"
Conditions = [
"""%CYBERARK:"""
"""Message="Set Password""""
""";Safe="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
Name = cyberark-epm-json-user-privilege-use-success-setname
Vendor = CyberArk
Product = CyberArk Endpoint Privilege Manager
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""RestrAccessEvent":"""
""""setName":""""
""""RestrictedObjectId":""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d\d:\d\d)""",
"""\d\d:\d\d\s({host}[^\s]+)\sLOGSTASH""",
"""({event_name}RestrAccessEvent)""",
""""Size"+:"+({bytes}\d+)""",
""""computerName"+:"+({src_host}[^"]+)""",
""""Description"+:"+({additional_info}[^"]+)""",
""""PolicyName"+:"+({policy_name}[^"]+)""",
""""@user"+:"+(({domain}[^"\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
""""@OsProcessId"+:"+({process_id}\d+)""",
""""Path"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
""""@allowed"+:"+({result}[^"]+)""",
""""eventId"+:"+({event_code}[^"]+)""",
""""RestrictedObjectId"+:"+\{({object_id}[^"}]+)""",
  
}
```