#### Parser Content
```Java
{
Name = "google-workspace-cef-file-permission-modify-success-aclchange"
Vendor = "Google"
Product = "Google Workspace"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"applicationName":""", """"drive"""", """"uniqueQualifier":""",  """"acl_change"""" ]
Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    ""","time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    ""","ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    ""","profileId":"({user_id}\d+)""",
    """"type":"acl_change"[^=]*?"name":"({access}[^"]+)"""",
    """"events":[^\}\]]*?"name":"({access}[^"]+)[^=]*?"""",
    """:"({app}drive)""",
    ""","parameters":[^=]*?name":"target_user","value":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"[^=]*?"""",
    ""","parameters":[^=]*?name":"doc_id","value":"({file_id}[^"]+)"[^=]*?name":"doc_type","value":"((?i)unknown|({file_type}[^"]+))"[^=]*?name":"doc_title","value":"\s*({file_name}[^"]+?(\.\s*({file_ext}[a-zA-Z]+?))?)\s*"[^=]*?name":"visibility","value":"({privileges}[^"]+)"""",
    """"name":"owner","value":"({file_owner}[^"]+)\s*"""",
    """suser=(anonymous|({user}[\w\.\-]{1,40}\$?))\s+[\w=]+""",
    """"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
  ]
DupFields = [
  "privileges->operation"
]
ParserVersion = "v1.0.0"


}
```