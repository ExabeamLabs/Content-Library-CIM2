#### Parser Content
```Java
{
Name = skyhighsecurity-swg-cef-app-login-fail-userloginfailed
  Conditions = [ """ mwg:""", """ CEF:""", """|Skyhigh Security|WebGateway|""", """ Action=USER_LOGIN_FAILED """ ]
  ParserVersion = "v1.0.0"
  Fields = ${McAfeeParsersTemplates.cef-skyhigh_security-secure_web_gateway.Fields}[
    """\sSource_ID=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\sUser-Agent=({user_agent}[^=]+)\s\w+=""",
    """\sRole=({role}[^"=]+)\s*($|"|\s\w+=)""",
    """\sAppliance=({dest_host}[\w\-.]+)\s*(\s\w+=|$|")""",
    """\sDetails=({failure_reason}[^=]+)\s*(\s\w+=|$|")"""
  ]

cef-skyhigh_security-secure_web_gateway = {
  Vendor = Skyhigh Security
  Product = Secure Web Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss.SSS"
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\smwg:""",
    """Timestamp=({time}\d{1,2}\/\w{3}\/\d{4}:\d\d:\d\d:\d\d\.\d{3})\s""",
    """\sUser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """\sAction=({action}[^\s]+)\s"""
  
}
```