#### Parser Content
```Java
{
Name = cisco-duo-kv-endpoint-authentication-auth
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  Conditions = [ """eventtype="authentication"""", """newenrollment="""", """ip="""", """result=""""]
  Fields = [
    """host="({host}[\w\-\.]+)"""",
    """\Wip="(0.0.0.0|({src_ip}[a-fA-F:\.\d]+))"""",
    """\Wusername="(?:({domain}[^\\"]+)\\)?({user}[^"]+)"""",
    """\Wfactor="(?:n\/a|({auth_method}[^"]+))"""",
    """\Wresult="({action}[^"]+)"""",
    """\Wreason="({failure_reason}[^"]+)"""",
    """\Wnewenrollment="({new_enrollment}True|False)"""
  ]
  ParserVersion = "v1.0.0"


}
```