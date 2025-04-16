#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-login-fdritemsexplorer
  ExtractionType = json
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """dproc=FDR Items explorer""", """"UserName":""", """"LogonType":""", """"LogonTime":""" ]
  Fields = [
    """exa_json_path=$._time,exa_regex=^({time}\d{10})""",
    """exa_json_path=$.UserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.LogonType,exa_field_name=login_type_text""",
    """exa_json_path=$.UserSid_readable,exa_field_name=user_sid""",
    """exa_json_path=$.AccountType,exa_field_name=user_type""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_regex=({app}FDR Items explorer)"""
  ]


}
```