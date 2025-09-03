#### Parser Content
```Java
{
Name = unix-rsyslog-str-network-notification-rsyslog
  Vendor = Unix
  Product = rsyslog
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """rsyslogd:""", """cannot connect to"""]
  Fields = [
  """\d\d:\d\d:\d\d ({host}\S+)? rsyslogd:"""
  """\srsyslogd:\s*({additional_info}.+?)\s*$"""
  """\srsyslogd:\s*.+?to (({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))(:({dest_port}\d+))?"""
  ]


}
```