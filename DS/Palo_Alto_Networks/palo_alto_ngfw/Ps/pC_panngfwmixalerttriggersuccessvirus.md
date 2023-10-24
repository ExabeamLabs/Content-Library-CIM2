#### Parser Content
```Java
{
Name = "pan-ngfw-mix-alert-trigger-success-virus"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,virus,"""
]
Fields = [
  """"host":\{[^=]*?"name":"({host}[^"]+)"[^=]*?\}"""
  """({host}[\w\-\.]+)\s+\d+,[^,]*,[^,]*,THREAT,virus,"""
  """,THREAT,([^,]*.){55}({host}[^,]+),"""
  """,THREAT(,[^,]*){40

}
```