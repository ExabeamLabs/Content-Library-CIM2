# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-sshbruteforce-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tags | ['"tags":\[({tags}.+"\})\]\}'] | ['"tags":\s*({tags}[^$]+?)\]', 'exa_regex="tags":\s*({tags}[^$]+?)\]'] |