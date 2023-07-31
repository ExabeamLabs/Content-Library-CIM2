#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-cef-alert-trigger-success-productversion
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  TimeFormat =  "epoch"
  Conditions = [ """CEF""","""|KasperskyLab|SecurityCenter|""","""cs3Label=ProductVersion""" ]
  Fields = [
    """Usuario:\s*({domain}[^\\]+)\\+({user}[^\s]+)""",
    """Componente:\s*({product_name}[^\\]+)""",
    """Resultado\\+Descripción:\s*({action}[^\\]+)""",
    """nObjeto:\s*({malware_url}[^\\]+)""",
    """Objeto\\+Adicional:\s*(\s|({additional_info}[^\\]+))""",
    """rt=({time}\d{13})\s""",
    """Fecha de lanzamiento de la base de datos:\s*({time}[^\\]+(a.\s*m.|p.\s*m.))""",
    """dhost=({dest_host}[^\s]+)\s*dst=""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """cs6=({protocol}[^\s"\{\}]+)""",
    """Aplicación\\+Nombre:\s*({app}[^\\]+)""",
    """cs4=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*cs4Label=AttackerIPv4""",
    """cs7=({src_port}\d+)\s*cs7Label""",
    """cs8=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*cs8Label=""",
    """cs5=({alert_name}.*?)\scs5Label="""
    """cs4=({alert_id}.*?)\scs4Label=TaskId""",
    """CEF:0\|([^\|]+\|){3}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|])"""
    """:\d\d:\d\d\s({host}[\w.-]+)\s"""
    """Objeto\\+Tipo:\s*({alert_type}[^\\]+)""",
    """Objeto\\+Nombre:\s*({alert_name}[^\\]+)""",
    ]
   ParserVersion = "v1.0.0"


}
```