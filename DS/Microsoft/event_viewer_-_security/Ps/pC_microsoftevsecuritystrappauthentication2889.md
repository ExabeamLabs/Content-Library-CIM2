#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-app-authentication-2889
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """2889""", """The following client performed a SASL""" ]
  Fields = [
    """({event_code}2889)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+EvntSLog""",
    """({event_name}The following client performed a SASL.+?)\s*\.\s*Client IP address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s+""",
    """attempted to authenticate as:\s*(({domain}[^\\\/]+?)[\\\/]+)?({user}[^\\\/]+?)\s*Binding Type:\s*(\d+)""", # binding_type is removed
  ]


}
```