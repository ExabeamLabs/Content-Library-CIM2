#### Parser Content
```Java
{
Name = juniper-jn-kv-endpoint-authentication-fail-authfailure
  Vendor = Juniper Networks
  Product = Junos OS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """SNMPD_AUTH_FAILURE""", """snmpd""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({host}[\w\-.]+) snmpd""",
    """message="({failure_reason}[^"]+)""",
    """source-address="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """destination-address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"


}
```