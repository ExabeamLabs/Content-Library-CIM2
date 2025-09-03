#### Parser Content
```Java
{
Name = skyhighsecurity-swg-cef-rule-create-success-creatednewrule
  Conditions = [ """ mwg:""", """ CEF:""", """|Skyhigh Security|WebGateway|""", """ Action=CREATED_NEW_RULE """ ]
  ParserVersion = "v1.0.0"
  Fields = ${McAfeeParsersTemplates.cef-skyhigh_security-secure_web_gateway.Fields}[
    """\sAppliance=({dest_host}[\w\-.]+)\s*(\s\w+=|$|")""",
    """\sSource_Name =({rule}[^=]+)\s\w+=""",
    """\sSource_ID=({rule_id}\d+)\s\w+=""",
    """\sSource_Path=({path}[^=]+)\s\w+=""",
    """\sCriteria=({rule_description}[^=]+)\s+Action=({rule_action}[^=]+)\s*(\s\w+=|$|")"""
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