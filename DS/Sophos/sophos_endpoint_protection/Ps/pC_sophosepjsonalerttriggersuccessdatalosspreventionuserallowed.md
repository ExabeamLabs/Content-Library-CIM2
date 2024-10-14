#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-datalosspreventionuserallowed
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":""",""""Event::Endpoint::DataLossPreventionUserAllowed"""", """"DATA_LOSS_PREVENTION"""" ]
  Fields = [
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """\s"name":\s*"({alert_name}[^"':]+)""",
    """"name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({dest_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({domain}[^\\",]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"id":\s*"({alert_id}[^"]+)""",
    """"rule":\s*"({rule}[^"]+)""",
    """"action":\s*"({action}[^"]+)""",
    """"app_name":\s*"({app}[^"]+)""""
    """"file_path":\s*"({target}.+?)\s*(\w+\s+\w+:|")"""
  ]
  ParserVersion = v1.0.0


}
```