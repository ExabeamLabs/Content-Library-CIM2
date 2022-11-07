#### Parser Content
```Java
{
Name = unix-unix-str-app-notification-httpdauth
Vendor = Unix
Product = Unix
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """pam_""", """ httpd: """, """(httpd:auth):""", """message:""" ]
Fields = [
"""({host}[\w\-.]+)\s+httpd:""",
"""({event_code}http)""",
"""message:\s*({event_name}.+?)\s+$""",
]


}
```