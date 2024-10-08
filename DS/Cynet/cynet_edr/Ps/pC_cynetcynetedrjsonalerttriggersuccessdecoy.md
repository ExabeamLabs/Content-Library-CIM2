#### Parser Content
```Java
{
Name = cynet-cynetedr-json-alert-trigger-success-decoy
       Vendor = Cynet
       Product = Cynet EDR
       TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
       Conditions = [ """Decoy""", """Cynet""", """"Severity""" ,"""Description"""]
       ExtractionType = json
       ParserVersion = v1.0.0
       Fields = [
         """exa_json_path=$.NetworkRisk,exa_field_name=risk_level""",
         """exa_regex=host Name:\s*({host}[\w\.\-]{1,40}\$?)"""
         """exa_regex=Decoy type:\s*({file_type}[^\s]+)"""
         """exa_json_path=$.Sha256,exa_field_name=hash_sha256""",
         """exa_json_path=$.HostName,exa_field_name=host""",
         """exa_json_path=$.UserName,exa_regex="UserName":"(({domain}[^\\]+)[\\]+)?({user}[\w\.\-]{1,40}\$?)"""
         """exa_json_path=$.Severity,exa_field_name=alert_severity""",
         """exa_json_path=$.Subject,exa_field_name=alert_subject""",
         """exa_json_path=$.StringIP,exa_field_name=alert_source""",
         """exa_json_path=$.LastSeen,exa_field_name=time"""
         """exa_json_path=$.AlertType,exa_field_name=alert_type"""
         """exa_json_path=$.Description,exa_field_name=additional_info"""
      ]
    

}
```