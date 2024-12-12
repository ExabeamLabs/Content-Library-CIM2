#### Parser Content
```Java
{
Name = extrahop-revealx-json-alert-trigger-success-sec-1
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = [ "MMM dd yyyy HH:mm:ss", "MMM dd yyyy HH:mm:ss Z" ]
  ExtractionType = json
  Conditions = [ """categories""", """sec.""", """"extrahop"""", """"event":""", """title"""]
  Fields = [
    """exa_json_path=$.event.start_time,exa_field_name=time""",
    """exa_json_path=$.event.detection_id,exa_field_name=alert_id""",
    """exa_json_path=$.event.title,exa_field_name=alert_name""",
    """exa_json_path=$.event.categories,exa_field_name=alert_type""",
    """exa_json_path=$.event.risk_score,exa_field_name=original_risk_score""",
    """exa_regex="object":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))
?",[^,]+?ipaddr""",
    """exa_json_path=$.event.participants[0].hostname,exa_regex=^({src_host}[\w\-.]+)$"""
    ]
      DupFields = [ "original_risk_score->alert_severity"]
    ParserVersion = "v1.0.0"


}
```