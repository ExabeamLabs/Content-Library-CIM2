#### Parser Content
```Java
{
Name = skyhighsecurity-swg-cef-app-notification-success-action
  Conditions = [ """ CEF:""", """|Skyhigh Security|WebGateway|""", """ Source_ID=""", """Source_Type=""" ]
  ParserVersion = "v1.0.0"
  Fields = ${McAfeeParsersTemplates.cef-skyhigh_security-secure_web_gateway.Fields}[
    """\sSource_Name =({object_name}[^=]+)\s\w+=""",
    """Source_Type=({object_type}[^=]+)\s\w+=""",
    """\sSource_ID=({object_id}[^=]+)\s\w+=""",
    """\sSource_Path=({object}[^=]+)\s({additional_info}\w+=.+)\s*($|")"""
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