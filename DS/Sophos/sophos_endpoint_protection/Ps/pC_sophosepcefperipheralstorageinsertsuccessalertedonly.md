#### Parser Content
```Java
{
Name = "sophos-ep-cef-peripheral-storage-insert-success-alertedonly"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """Event::Endpoint::Device::AlertedOnly"""", """"Peripheral allowed:""" ]
Fields = [
""""location":"({src_host}[\w\-.]+)""",
""""when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
""""type":"({additional_info}[^"]+)""",
""""name":"({operation_details}({operation}Peripheral allowed):\s*({device_class}[^"]+))""",
""""source":"(n\/a|({full_name}[^"\\\(\),]+))"""",
""""source":"(n\/a|({last_name}[^",\s]+),\s*({first_name}[^,"\s]+))""",
""""source":"(n\/a|(({domain}[^\\"]+)(\\){1,20}))?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
""""ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
]
DupFields = ["src_host->host"]
ParserVersion = "v1.0.0"


}
```