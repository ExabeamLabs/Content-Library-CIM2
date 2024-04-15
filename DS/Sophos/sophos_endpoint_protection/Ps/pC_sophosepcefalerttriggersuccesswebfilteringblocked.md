#### Parser Content
```Java
{
Name = "sophos-ep-cef-alert-trigger-success-webfilteringblocked"
ParserVersion = "v1.0.0"

cef-sophos-security-alert-1.Fields}[
    """"name"*:"*({alert_name}[^"]+).\sUsername:"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = sophos-ep-sk4-alert-trigger-success-dlpautomaticallyallowed
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """CEF:""", """Event::Endpoint::DataLossPreventionAutomaticallyAllowed""", """group=DATA_LOSS_PREVENTION""" ]
  Fields = [
    """"location":"({host}[\w\-.]+)"""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"type":"({alert_type}Event[^"]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"id":"({alert_id}[^"]+)""",
    """"location":"({src_host}[^"]+)""",
    """"name":\s*"({alert_name}.+?)\s+(\w+:)"""
    """"name":\s*"({additional_info}[^"]+)"""
    """"name".+?Username:\s*(({domain}[^\\]+)\\+)?({user}[^\s\\]+)\s""",
    """"name".+?Rule names:\s*′({rule}[^′]+)""",
    """"name".+?User action:\s*({operation}.+?)\s+(\w+\s+\w+:)""",
    """"name".+?Application Name:\s+({app}.+?)\s+Data Control action:""",
    """"name".+?Data Control action:\s*({action}[^\s]+)\s""",
    """"name".+?File type:\s*({file_type}.+?)\s+File size:\s*({bytes}\d+)\s""",
    """"name".+?Source path:\s*({target}.+?)\s*(\w+\s+\w+:|")"""
  
}
```