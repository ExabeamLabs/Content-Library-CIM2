#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-app-login-success-console"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "epoch"
Conditions = [
  """|Carbon Black|Protection|"""
  """|Console user login|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+[\w-]+=|\s*$)"""
  """(\||\s)dvc=(|({host_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s+(\w+=|$)"""
  """(\||\s)duser=((|({domain}[^\\\s]+)[\\\/]+)?({user}[^@\s]+?)|({email_address}[^@]+@({email_domain}[^\s']+)))(\s+\w+=|\s*$)"""
  """msg=User\s[\\]?'(({email_address}[^@]+@({email_domain}[^'.]+\.[^']+))|({user}[^\s'@]+?)@({domain}[^\s\\']+))[\\]?"""
  """(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)"""
  """(\||\s)msg=.+from\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```