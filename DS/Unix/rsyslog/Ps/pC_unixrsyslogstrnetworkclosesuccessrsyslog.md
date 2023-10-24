#### Parser Content
```Java
{
Name = unix-rsyslog-str-network-close-success-rsyslog
Vendor = Unix
Product = rsyslog
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = v1.0.0
Conditions = [ """rsyslogd:""", """closed connection"""]
Fields = [
"""\d\d:\d\d:\d\d ({host}\S+)? rsyslogd:"""
"""\srsyslogd:\s*({additional_info}.+?)\s*$"""
"""\srsyslogd:\s*.+?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]


}
```