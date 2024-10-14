#### Parser Content
```Java
{
Name = "imperva-securesphere-leef-alert-trigger-success-description"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Imperva|SecureSphere|"""
"""AlertNumber="""
"""AlertType="""
"""Description="""
]
Fields = [
"""(\s|\||\\t)CreateTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""(\s|\||\\t)SourceIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\||\\t)SourcePort=({src_port}\d+)"""
"""(\s|\||\\t)ServerIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""(\s|\||\\t)ServerPort=({dest_port}\d+)"""
"""(\s|\||\\t)Username=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)AlertType=(|({alert_type}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)ServerGroup=(|({server_group}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)Severity=(|({alert_severity}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)Service=(|({service_name}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)Application=(|({app}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)Description=(|({additional_info}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)Protocol=(|({protocol}.+?))(\\t\w+=|\s*$)"""
"""(\s|\||\\t)RuleName =(|({alert_name}.+?))(\\t\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```