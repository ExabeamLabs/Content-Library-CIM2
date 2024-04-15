#### Parser Content
```Java
{
Name = "hp-arubamm-cef-endpoint-login-fail-userauthenticationfailed"
Vendor = "HP"
Product = "Aruba Mobility Master"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = ["""CEF:""", """"ident":""", """"extradata":""", """User Authentication failed.""", """method"""]
Fields = [
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
  """"host":"({host}[^\"]+)""""
  """MAC\\*=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"""
  """usermac\\*=({src_mac}[\w:]+)"""
  """username\\*=({email_address}({user}[^@]+)@({domain}[^\s]+))"""
  """Authentication Succeeded for User ({user}[^,]+)"""
  """Logged in from\\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\sport\s({src_port}\d+))?"""
  """Connecting to\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\sport\s({dest_port}\d+))?"""
  """IP\\*=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """smethod\\*=({auth_type}[^=]+)\s+\w+\\*="""
  """server\\*=({auth_server}[^"]+)""""
  """servername\\*=({auth_server}[^=]+)\s+\w+\\*="""
  """username\\*=({user}\w+)\s"""
  """authmethod\\*=({auth_type}[^=]+)\s+\w+\\*="""
]


}
```