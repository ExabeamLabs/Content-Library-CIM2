#### Parser Content
```Java
{
Name = microsoft-o365-json-user-mfa-enable-success-enablestrongauthentication
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Operation":"""", """Strong Authentication""", """"Workload":"""", """"ResultStatus":""""   ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"Operation":"({event_name}({operation}[^"]+))"""",
    """"ResultStatus":"({result}[^"]+)"""",
    """"Workload":"({app}[^"]+)"""",
    """"OrganizationId":"({tenant_id}[^"]+)",""",
    """"Value":"({object}[^"]+)","Name":"extendedAuditEventCategory"""",
    """"extendedAuditEventCategory","Value":"({object}[^"]+)""",
    """ObjectId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """UserId":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.CreationTime,exa_field_name=time""",
    """exa_json_path=$.Operation,exa_field_name=operation""",
    """exa_json_path=$.Operation,exa_field_name=event_name""",
    """exa_json_path=$.ResultStatus,exa_field_name=result""",
    """exa_json_path=$.Workload,exa_field_name=app""",
    """exa_json_path=$.OrganizationId,exa_field_name=tenant_id""",
    """exa_regex="extendedAuditEventCategory","Value":"({object}[^"]+)""",
    """exa_regex="Value":"({object}[^"]+)","Name":"extendedAuditEventCategory"""",
    """exa_json_path=$.ObjectId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.UserId,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  ]


}
```