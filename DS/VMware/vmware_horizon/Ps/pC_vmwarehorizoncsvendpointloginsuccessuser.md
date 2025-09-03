#### Parser Content
```Java
{
Name = vmware-horizon-csv-endpoint-login-success-user
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """connected to the""","""User""","""session ID:"""] //session ID added to avoid conflict
  Fields = [
      """User ({user}[\w\.\-\!\#\^\~]{1,40}\$?) connected to the""",
      """(?:session ID: [^\s]{1,2000}({session_id}\w{4}))"""
  ]
  ParserVersion = "v1.0.0"


}
```