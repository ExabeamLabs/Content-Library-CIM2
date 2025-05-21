#### Parser Content
```Java
{
Name = lastpass-l-sk4-app-activity-success-report
Vendor = LastPass
Product = LastPass
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = "v1.0.0"
Conditions = [ """Action":""","""dproc=EventReporting""","""destinationServiceName =LastPass"""]
Fields = [
""""Time":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
""""IP_Address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
"""destinationServiceName =({app}[^=]+?)\s\w+=""",
""""+Action"+:"+({event_name}[^"]+)"+""",
""""Username"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
""""Username"+:"+API:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
""""+Action"+:"+({action}[^"]+)"+""",
""""+Data"+:"+({additional_info}[^"\}\,]+)""",
"""fname=({file_name}[^=]+?)\s+[\w]+=""",
"""filePermission=({access}[^=]+?)\s+[\w]+=""",
"""duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w]+=""",
"""Resource:\s+({file_type}[^:]+)\s+::"""
]
DupFields = [ "event_name->operation" ]


}
```