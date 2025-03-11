#### Parser Content
```Java
{
Name = "mimecast-seg-cef-app-login-success-audittype"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
Conditions = [ """"auditType":"User Logged On"""", """"eventInfo":""", """"eventTime":""", """"category":""" ]
Fields = ${mimecast-json-template.mimecast-json-event.Fields}[
"""\"eventTime\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+)"""
"""\WdestinationServiceName =(|({event_subtype}[^=]+?))(\s+\w+=|\s*$)"""
"""\Wdproc=(|({dproc}[^=]+?))(\s+\w+=|\s*$)"""
"""\"auditType\":\"({operation}[^\"]+)"""
"""({result}(?i)success)"""
"""({app}Mimecast Email Security)"""
"""Application:\s*({service_name}[^,]+)"""
"""\WIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"user\":\"({email_address}[^\"]+)"""
"""\"user(A|a)gent\"\s*:\s*\"({user_agent}[^\"]+?)\"\s*[,\}\]]"""
]
ParserVersion = "v1.0.0"


}
```