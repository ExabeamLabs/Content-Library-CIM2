#### Parser Content
```Java
{
Name = cisco-duo-kv-endpoint-authentication-auth
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """eventtype="authentication"""", """newenrollment="""", """ip="""", """result=""""]
  Fields = [
    """host="({host}[\w\-\.]+)"""",
    """\Wip="(0.0.0.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """\Wusername="(?:({domain}[^\\"]+)\\)?({user}[^"]+)"""",
    """\Wfactor="(?:n\/a|({auth_method}[^"]+))"""",
    """\Wresult="({action}[^"]+)"""",
    """\Wreason="({failure_reason}[^"]+)"""",
    """\Wnewenrollment="({new_enrollment}True|False)"""
  ]
  ParserVersion = "v1.0.0"


}
```