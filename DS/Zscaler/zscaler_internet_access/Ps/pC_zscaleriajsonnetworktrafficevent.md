#### Parser Content
```Java
{
Name = "zscaler-ia-json-network-traffic-event"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Internet Access"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
""""department":"""
""""avgduration":"""
""""locationname":"""
""""event" :{"""
  ]
  Fields = [
"""({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""\"action\":\"({action}[^\"]+)\""""
"""user\":\"(({email_address}[^@]+@[^\"]*)|({user}[^\"]+))\""""
"""csip\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""sdip\":\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""sdport\":\"({dest_port}\d+)\""""
"""csport\":\"({src_port}\d+)\""""
"""proto\":\"({protocol}[^\"]+)\""""
"""inbytes\":\"({bytes_in}\d+)\""""
"""outbytes\":\"({bytes_out}\d+)\""""
"""devicehostname\":\"(NA|\s+|({host}[^\"]+))\""""
  ]


}
```