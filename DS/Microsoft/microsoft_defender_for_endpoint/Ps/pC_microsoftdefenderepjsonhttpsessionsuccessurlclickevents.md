#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-http-session-success-urlclickevents"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"operationName":""", """"Publish"""", """"category":""", """"AdvancedHunting-UrlClickEvents"""", """"UrlChain":""", """"ActionType":""" ]
  Fields = [
    """exa_json_path=$..Timestamp,exa_field_name=time""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$..ActionType,exa_field_name=action""",
    """exa_json_path=$..UrlChain,exa_regex=\[\\?"({malware_url}[^\s,"]+?)\\?"\]""",
    """exa_json_path=$..Url,exa_field_name=url""",
    """exa_json_path=$..AccountUpn,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$..IPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```