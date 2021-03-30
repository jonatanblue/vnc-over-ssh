# VNC over SSH

## Motivation

For doing development on a VM in EC2 instead of locally on a laptop.

Because network speeds and compute power are better.

## How to run

1. Create an EC2 VM 
1. Upload the xstartup file to ~/.vnc on the VM
1. Install all the dependencies 
1. Set up your AWS profile in `~/.aws/config`
1. Run the script:
  `vnc-ssh-tunnel my-aws-profile us-west-1 i-0000111122223333`

When you are done you can stop the VM with:

```
aws --profile my-aws-profile ec2 --region eu-west-1 stop-instances --instance-ids i-0000111122223333
```

