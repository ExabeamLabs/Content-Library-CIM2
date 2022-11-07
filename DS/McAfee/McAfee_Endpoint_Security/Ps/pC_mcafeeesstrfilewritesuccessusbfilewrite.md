#### Parser Content
```Java
{
Name = mcafee-es-str-file-write-success-usbfilewrite
  Conditions = [ """|USB File Write|""" ]
  ParserVersion = "v1.0.0"

splunk-mcafee-usb-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "epoch_sec"
      Fields = [
        """^.*?({alert_id}\d+)\|""",
        """^([^|]*\|){11}({device_type}[^|]+)\|""",
        """^([^|]*\|){14}({dest_ip}[a-fA-F0-9.:]+)\|""",
        """^([^|]*\|){15}({src_host}[^|]+)\|""",
        """^([^|]*\|){17}({src_file_name}[^|]+)""",
        """^([^|]*\|){19}({src_file_path}[^|]+)""",
        """^([^|]*\|){19}({src_file_path}[^|]*?({src_file_name}[^\\\/|]+))\|""",
        """^([^|]*\|){16}({src_file_path}[^|]+)""",
        """^([^|]*\|){16}({src_file_path}[^|]*?({file_name}[^\\\/|]+))\|""",
        """^([^|]*\|){20}(({domain}[^\\]+?)\\)?({user}[^|\\]+)\|""",
        """\|({time}\d+\.\d+)\s*$""",
      ]
    }

 splunk-mcafee-usb-insert-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "yyyy-MM-dd HH:mm:ss"
      Fields = [
        """InsertionTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
        """RulesToDisplay="({operation}[^"]+)""",
        """IP="({dest_ip}[A-Fa-f.\d:]+)""",
        """\sName ="({dest_host}[^"]+)""",
        """Username_NTLM="((({domain}[^\\]+)\\)?({user}[^"]+))""",
        """USBVendorId="(\s*|({device_id}[^"]+))"""",
        """DeviceName ="({device_type}[^"]+)""",
        """\sFileName ="({file_name}[^"]+)""",
        """({action}Block)""",
        """TotalContentSize="({bytes}\d+)"""

      ]
      DupFields = ["operation->activity_details"]
    
}
```