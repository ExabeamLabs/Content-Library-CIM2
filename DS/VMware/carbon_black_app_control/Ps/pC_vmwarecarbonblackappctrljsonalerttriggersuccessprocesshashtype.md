#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-json-alert-trigger-success-processhashtype
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """"Bit9Server"""", """"ProcessHashType"""" ]
  Fields = [
    """Timestamp":\s+"({time}[^"]+)""",
    """Bit9Server":\s+"({host}[^"]+)""",
    """EventType":\s+"({alert_type}[^"]+)""",
    """EventSubType":\s+"({alert_name}[^"]+)""",
    """HostName":\s+"(({web_domain}[^\\]+)\\+)?({src_host}[^"]+)""",
    """HostIP":\s+"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Priority":\s+"({alert_severity}[^"]+)""",
    """ABId":\s+"({alert_id}[^"]+)""",
    """Message":\s+"({additional_info}[^"]+)""",
    """PathName":\s+"({url}[^"]+)""",
    """UserName":\s+"({user}[^"]+)""",
    """c:\\+users\\+({user}[^"\\]+)""",
  ]


}
```