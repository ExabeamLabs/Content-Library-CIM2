#### Parser Content
```Java
{
Name = sophos-ep-sk4-alert-trigger-success-dlpautomaticallyallowed
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Event::Endpoint::DataLossPreventionAutomaticallyAllowed""", """DATA_LOSS_PREVENTION""", """endpoint_type""" ]
  Fields = [
    """"location":"({host}[\w\-.]+)"""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"type":"({alert_type}Event[^"]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"id":"({alert_id}[^"]+)""",
    """"location":"({src_host}[^"]+)""",
    """"name":\s*"({alert_name}.+?)\s+(\w+:)"""
    """"name":\s*"({additional_info}[^"]+)"""
    """"name".+?Username:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
    """"name".+?Rule names:\s*′({rule}[^′]+)""",
    """"name".+?User action:\s*({operation}.+?)\s+(\w+\s+\w+:)""",
    """"name".+?Application Name:\s+({app}.+?)\s+Data Control action:""",
    """"name".+?Data Control action:\s*({result}[^\s]+)\s""",
    """"name".+?File type:\s*({file_type}.+?)\s+File size:\s*({bytes}\d+)\s""",
    """"name".+?Source path:\s*({target}.+?)\s*(\w+\s+\w+:|")"""
    """"group":"({group_name}[^"]+)"""",
    """"source":"(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\\\(\)]+))","\w+""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"user_id":"({user_id}[^"]+)"""
    """"endpoint_type":"({device_type}[^"]+)"""
  ]


}
```