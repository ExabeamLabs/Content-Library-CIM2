# Code Changes for netskope-webtx-csv-network-traffic-httptransaction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){21}(-|({app}[^,]+))'] |
| edit_regex_field | browser |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){6}(-|({browser}[^,]+))'] |
| edit_regex_field | bytes |  | ['^(-,|"+(.+?)"+,|([^,]*),){0}(-|({bytes}\d+))'] |
| edit_regex_field | category |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){17}(-|({category}[^,]+))'] |
| edit_regex_field | country |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){8}(-|({country}[^,]+))'] |
| edit_regex_field | dest_ip |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){40}(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))'] |
| edit_regex_field | dest_port |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){41}(-|({dest_port}\d+))'] |
| edit_regex_field | device_name |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){9}(-|({device_name}[^,]+))'] |
| edit_regex_field | domain |  | ['^(-,|"+(.+?)"+,|([^,]*),){4}(-|({domain}[^,]+))'] |
| edit_regex_field | host |  | ['^(-,|"+(.+?)"+,|([^,]*),){5}(-|({host}[^,]+))'] |
| edit_regex_field | http_response_code |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){3}(-|({http_response_code}\d+))'] |
| edit_regex_field | method |  | ['^(-,|"+(.+?)"+,|([^,]*),){6}(-|({method}[^,]+))'] |
| edit_regex_field | mime |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){2}(-|({mime}[^,]+))'] |
| edit_regex_field | os |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){14}(-|({os}[^,]+))'] |
| edit_regex_field | protocol |  | ['^(-,|"+(.+?)"+,|([^,]*),){11}(-|({protocol}[^,]+))'] |
| edit_regex_field | referrer |  | ['^(-,|"+(.+?)"+,|([^,]*),){7}(-|"({referrer}[^"]+)",|({=referrer}[^,]+),)'] |
| edit_regex_field | src_ip |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){49}(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))'] |
| edit_regex_field | src_port |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){51}(-|({src_port}\d+))'] |
| edit_regex_field | time |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){59}(-|({time}\d{10}))'] |
| edit_regex_field | traffic_type |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){60}(-|({traffic_type}[^,]+))'] |
| edit_regex_field | uri |  | ['^(-,|"+(.+?)"+,|([^,]*),){8}(-|"({uri}[^"]+)",|({=uri}[^,]+),)'] |
| edit_regex_field | web_content_type |  | ['^(-,|"+(.+?)"+,|([^,]*),){3}(-|"({web_content_type}[^"]+)",|({=web_content_type}[^,]+),)'] |