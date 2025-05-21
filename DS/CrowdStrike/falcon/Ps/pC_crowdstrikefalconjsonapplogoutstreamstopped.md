#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-app-logout-streamstopped"
  ExtractionType = json
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [""""service":""", """"crowdstrike"""", """"type":""", """"AuthActivityAuditEvent"""", """"name":""", """"streamStopped""""]
  Fields = [
    """exa_json_path=$.attributes.evt.timestamp,exa_field_name=time""",
    """exa_json_path=$.attributes.evt.service,exa_field_name=app""",
    """exa_json_path=$.attributes.evt.outcome,exa_field_name=result""",
    """exa_json_path=$.attributes.evt.name,exa_field_name=event_name""",
    """exa_json_path=$.attributes.metadata.customer_id_string,exa_field_name=cid""",
    """exa_json_path=$.attributes.usr.id,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({user_id}api-client-id:[^"]+))$""",
    """exa_json_path=$.attributes.network..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]


}
```