#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-alert-trigger-success-alert"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """|SecureSphere|"""
  """cat=Alert"""
  """cs12Label=HostName"""
  """cs3Label=ServiceName"""
]
Fields = [
  """\Wrt=({time}\w+ \d+ \d+ \d+:\d+:\d+)"""
  """\s({host}[\w\.-]+)\s+CEF:"""
  """\Wduser=(|({user}.+?))\s*(\w+=|\||$)"""
  """\Wcs1=(|({alert_name}[^=]+?))\s*(\w+=|\||$)"""
  """\Wcs13=({db_name}[^=\s]+?)\s*(\w+=|\||$)"""
  """\Wcs4=(|({app}[^=]+?))\s*(\w+=|\||$)"""
  """\Wcs3=(|({service_name}[^=]+?))\s*(\w+=|\||$)"""
  """\Wcs2=(|({server_group}[^=]+?))\s*(\w+=|\||$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wcs12=(|({dest_host}.+?))\s*(\w+=|\||$)"""
  """\Wsev=(|({alert_severity}.+?))\s*(\w+=|\||$)"""
  """\Wcs16=(|({additional_info}.+?))\s*(\w+=|\||$)"""
  """\Wcs16=N/A\s*\(({additional_info}.+?)\)"""
  """\Wcs14=(|({db_schema}.+?))\s*(\w+=|\||$)"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```