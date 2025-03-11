#### Parser Content
```Java
{
Name = skyhighsecurity-swg-cef-file-download-success-filedownload
  Conditions = [ """ mwg:""", """ CEF:""", """|Skyhigh Security|WebGateway|""", """ Action=FILE_DOWNLOAD """ ]
  ParserVersion = "v1.0.0"
  Fields = ${McAfeeParsersTemplates.cef-skyhigh_security-secure_web_gateway.Fields}[
    """\sAppliance=({dest_host}[\w\-.]+)\s*(\s\w+=|$|")""",
    """\sSource_Type=({file_type}[^=]+)\s\w+=""",
    """\sSource_ID=({file_path}({file_dir}[^"]*?))[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?)\s"""
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