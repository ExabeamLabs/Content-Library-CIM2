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
        """^([^|]*\|){11}({device_type}[^|]+)\|""",
        """^([^|]*\|){14}({dest_ip}[a-fA-F0-9.:]+)\|""",
        """^([^|]*\|){15}({dest_host}[^|]+)\|""",
        """^([^|]*\|){17}({file_name}[^|]+)""",
        """^([^|]*\|){19}({file_path}[^|]+)""",
        """^([^|]*\|){19}({file_path}[^|]*?({file_name}[^\\\/|]+))\|""",
        """^([^|]*\|){16}({file_path}[^|]+)""",
        """^([^|]*\|){16}({file_path}[^|]*?({file_name}[^\\\/|]+))\|""",
        """^([^|]*\|){20}(({domain}[^\\]+?)\\)?({user}[^|\\]+)\|""",
        """\|({time}\d{10}\.\d+)\s*\|""",
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
        """Username_NTLM="((({domain}[^\\]+)\\)?({user}[^"]+))""",
        """USBVendorId="(\s*|({device_id}[^"]+))"""",
        """DeviceName ="({device_type}[^"]+)""",
        """\sFileName ="({file_name}[^"]+)""",
        """({action}Block)""",
        """TotalContentSize="({bytes}\d+)"""

      ]
      DupFields = ["operation->operation_details"]
    
}
```