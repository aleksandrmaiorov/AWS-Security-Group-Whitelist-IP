## **AWS Security Group whitelist ip**
Simple python script to update a security group in AWS with a whitelisted IP address.

## **Prerequisites**
python3 & pip3 & boto3 & requests package.
```sh
pip3 install boto3
pip3 install requests
```

## **Setup**
Clone the repo locally and cd into it. Before you run the script, set the AWS credentials locally, in the terminal.
After this, edit the whitelist.py file to change the 
> Note: `sg_id = '__SECURITY_GROUP_ID__'` (line 8 of the script.)

variable with the needed ID of the security group you need to whitelist your IP in.


## **Usage**
After editing the script is done, just run it with 
```sh
python3 whitelistip.py
```
The script is interactive and it will prompt you to add the port you need access to and your name. Your name is used in the sg rule description so that when added, you know exactly whose IP is that. Also, it plays a vital role in a check that checks if you already have an IP whitelisted. If yes, it will just update that one with the new IP instead of just repeatedly adding new IP addresses.

## **What is covered**
- First IP whitelist (with description)
- Consecutive IP changes (when dynamic IP changes) based on the description/name check
