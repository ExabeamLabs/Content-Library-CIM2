#### Parser Content
```Java
{
Name = "code42-incydr-json-file-success-file-1"
    ParserVersion = "v1.0.0"
    Vendor = "Mimecast"
    Product = "Code42 Incydr"
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
        """"risk":{"severity"""",
        """"user":{"actorHour""""
           ]
    Fields = [
        """exa_json_path=$.@timestamp,exa_field_name=time""",
        """exa_json_path=$.event.id,exa_field_name=event_id""",
        """exa_json_path=$.event.action,exa_field_name=event_name""",
        """exa_json_path=$.file.name,exa_field_name=file_name""",
        """exa_json_path=$.file.directory,exa_field_name=file_dir""",
        """exa_json_path=$.file.sizeInBytes,exa_field_name=bytes""",
        """exa_json_path=$.file.hash.sha256,exa_field_name=hash_sha256""",
        """exa_json_path=$.file.owner,exa_field_name=file_owner""",
        """exa_json_path=$.file.changeType,exa_field_name=operation""",
        """exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
        """exa_json_path=$.source.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))""",
        """exa_json_path=$.risk.severity,exa_field_name=alert_severity""",
        """exa_json_path=$.risk.score,exa_field_name=risk_score"""
        """exa_json_path=$.file.mimeType,exa_field_name=mime"""
    ]


}
```