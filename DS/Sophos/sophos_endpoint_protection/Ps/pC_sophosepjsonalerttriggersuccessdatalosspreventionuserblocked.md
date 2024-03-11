#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-datalosspreventionuserblocked
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":""", """"Event::Endpoint::DataLossPreventionUserBlocked"""", """"DATA_LOSS_PREVENTION"""" ]
  Fields = [
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """\s"name":\s*"({alert_name}[^"':]+)\s""",
    """"name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({dest_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({domain}[^\\",]+)\\+)?({user}[^",\\\/\s]+)""""
    """"id":\s*"({alert_id}[^"]+)""",
    """"name".+?Username:\s*(({domain}[^\\]+)\\+)?({user}[^\s\\]+)\s""",
    """"name".+?Rule names:\s*′({rule}[^′]+)""",
    """"name".+?User action:\s*({operation}.+?)\s+(\w+\s+\w+:)""",
    """"name".+?Application Name:\s+({app}.+?)\s+Data Control action:""",
    """"name".+?Data Control action:\s*({action}[^\s]+)\s""",
    """"name".+?File type:\s*({file_type}.+?)\s+File size:\s*({bytes}\d+)\s""",
    """"name".+?Source path:\s*({target}.+?)\s*(\w+\s+\w+:|")"""
  ]
  ParserVersion = v1.0.0


}
```