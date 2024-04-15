#### Parser Content
```Java
{
Name = "lexmark-l-cef-printer-activity-success-printjob"
Vendor = "Lexmark"
Product = "Lexmark"
TimeFormat = "epoch"
Conditions = [
"""|Lexmark|Print Release|"""
"""|Print Job|"""
]
Fields = [
"""\sstart=(?:|({time}\d{13}))(\s+\w+=|\s*$)"""
"""\ssuid=(?:|({user}.+?))(\s+\w+=|\s*$)"""
"""\sduid=(?:|({account}.+?))(\s+\w+=|\s*$)"""
"""src=(?:|({host}.+?))\s+name=CEF"""
"""\scn1=(?:|({num_pages}\d+))(\s+\w+=|\s*$)"""
"""\sact=(?:|({event_code}\w+))(\s+\w+=|\s*$)"""
"""\scs5=(?:|({printer_name}.+?))(\s+\w+=|\s*$)"""
"""\sdhost=(?:|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\sdst=(?:|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+\w+=|\s*$)"""
"""\ssrc=(?:|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)(\s+\w+=|\s*$)"""
"""\sfname=(?:|({object}.+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```