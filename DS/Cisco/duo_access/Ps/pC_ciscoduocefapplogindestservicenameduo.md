#### Parser Content
```Java
{
Name = "cisco-duo-cef-app-login-destservicenameduo"
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = ["epoch_sec","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """destinationServiceName =DUO """ ]
  Fields = [
    """"ts"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)""",
    """"isotimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{6})?([+-]\d\d:\d\d)?)"""",
    """\"timestamp\":\s*({time}\d{10})""",
    """\WdestinationServiceName =(|({app}[^=]+?))(\s+\w+=|\s*$)""",
    """"username"+:"+(?!AD Sync:|AD User Sync:)(({email_address}[^"\s@]+@({email_domain}[^"\s@]+))|({full_name}[^\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"phone":\s*"({device_name}({object}[^"]+))"""",
    """"device":\s*"({device_name}({object}[^"]+))""",
    """"object":\s*"(({email_address}[^"@\s]+@[^"\s@]+)|({object}[^"]+))""",
    """"status":\s*"({status_msg}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """\\?"error\\?":\s*\\?"({failure_reason}[^"\\]+)\\?"""",
    """"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\\?"ip(_address)?\\?":\s*\\?"(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\\?"""",
    """"description":\s*"\{({additional_info}[^"]+?)\}",""",
    """"factor":\s*"(n\/a|({factor}[^"]+))""",
    """"reason":\s*"(User approved|Valid passcode|({failure_reason}[^"]+))"""",
    """"context":\s*"({operation}[^"]+)"""",
    """"action":"({operation}[^"]+)"""",
    """"browser":\s*"({browser}[^"]+)"""",
    """"os":\s*"({os}[^"]+)"""",
    """"description":"\{\\"uname\\":\s\\"(({dest_email_user}[^"\s@]+@[^"\s@]+)|({dest_user}[^"]+?))\\?"""",
    """msg=({additional_info}[^=]+)\s+\w{1,200}=""",
  ]


}
```