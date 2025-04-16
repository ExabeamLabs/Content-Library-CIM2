#### Parser Content
```Java
{
Name = mcafee-es-str-file-write-success-filewritepc
  Conditions = [ """|USB/CD/DVD File Write PC|""", """|40102|""" ]
  ParserVersion = "v1.0.0" 

splunk-mcafee-usb-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "epoch_sec"
      Fields = [
        """^.*?({alert_id}\d+)\|""",
        """^([^|]*\|){11}({device_class}[^|]+)\|""",
        """^([^|]*\|){14}({dest_ip}[a-fA-F0-9.:]+)\|""",
        """^([^|]*\|){15}({dest_host}[^|]+)\|""",
        """^([^|]*\|){17}({file_name}[^|]+)""",
        """^([^|]*\|){19}({file_path}[^|]+)""",
        """^([^|]*\|){19}({file_path}[^|]*?({file_name}[^\\\/|]+?(\.({file_ext}[^\s\.\\\/|]+?))?))\|""",
        """^([^|]*\|){16}({file_path}[^|]+)""",
        """^([^|]*\|){16}({file_path}[^|]*?({file_name}[^\\\/|]+?(\.({file_ext}[^\s\.\\\/|]+?))?))\|""",
        """^([^|]*\|){20}(({domain}[^\\]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|""",
        """\|({time}\d{10})(\.\d+)?\s*\|""",
      ]
    }

 splunk-mcafee-usb-insert-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "yyyy-MM-dd HH:mm:ss"
      Fields = [
        """InsertionTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
        """RulesToDisplay="({operation}[^"]+)""",
        """IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """\sName ="({dest_host}[^"]+)""",
        """Username_NTLM="((({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
        """USBVendorId="(\s*|({device_id}[^"]+))"""",
        """DeviceName ="({device_class}[^"]+)""",
        """\sFileName ="({file_name}[^"]+)""",
        """({action}Block)""",
        """TotalContentSize="({bytes}\d+)"""
        """DeviceClassName ="({device_class}[^"=]+)"""

      ]
      DupFields = ["operation->operation_details"]
    }

    mcafee-http-session-2 = {
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd HH:mm:ss"]
    Fields = [
    """(({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s({host}[\w\-.]+)\s(\S+\s+){4})?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({=host}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^;\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)",("[^"]*",){3}"({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",){4}"({http_response_code}\d+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))",("[^"]*"),"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    """"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({host}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)",""""
   """"(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^\?";]+)","({uri_path}\/[^\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)","""
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",)""""
   """",("[^"]*",){6}"({http_response_code}\d+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))",("[^"]*"),"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    ]
    DupFields = ["url->web_domain"]
    }

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