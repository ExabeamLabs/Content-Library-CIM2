#### Parser Content
```Java
{
Name = amazon-eks-json-app-activity-success-annotations
    Product = Amazon EKS
    Vendor = Amazon
    TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
    Conditions = [
      """apiVersion""",
      """responseStatus""",
      """annotations""" ,
      """eks"""
      ]
    Fields =[
      """"*sourceIPs\\?"*:\[\\?"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user":\{"*username\\?"*(=>|:)\\?"*(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """"*groups\\?"*(=>|:)\[\\?"*({group_name}[^"\]\\]+)""",
      """"*authorization.k8s.io\/decision\\?"*(=>|:)\\?"*({action}[^\s"]+?)\\?"""",
      """({time}\d+\-\d+\-\d+T\d\d:\d\d:\d\d(\.\d+)?Z)""",
      """"*code\\?"*(=>|:)({result_code}\d+)""",
      """"*userAgent\\?"*:\\?"*({user_agent}.+?)\s*kubernetes""",
      """"annotations\\":\{\\({result_reason}[^\}]+)\\"\}"""
      """requestURI\\?":\\?"({url}[^\"]+)\\""""
      """"AccountName":"({account}[^"\\]+)""""
      """"logStream":"({service_name}[^"]+)""""
      """"owner":"({owner_id}[^"]+)""""
      """"verb":"({method}[^"]+)""""
      """"resource\\?":\\?"({resource}[^"\\]+)"""
      """"objectRef":\{({additional_info}[^\}]+)"""
      """"objectRef":[^\$]+?"apiVersion":"({version}[^"]+)""""
      """"objectRef":[^\$]+?"apiGroup":"({group_info}[^"]+)""""
      """"objectRef":[^\$]+?"name":"({object}[^"]+)""""
      ]
    ParserVersion = "v1.0.0"
  

}
```