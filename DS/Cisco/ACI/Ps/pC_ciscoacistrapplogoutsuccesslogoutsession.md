#### Parser Content
```Java
{
Name = cisco-aci-str-app-logout-success-logoutsession
  Vendor = Cisco
  Product = ACI
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""ACI""","""logout,session""",""" From-"""]
  Fields = [
        """\d+:\d+:\d+(.\d+)?\s({host}[^\s]+)""",
        """remoteuser-({user}[^\]]+)""",
        """From-({src_ip}[\da-fA-F.:]+)""",
  ]


}
```