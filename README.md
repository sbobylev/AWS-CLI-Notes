 # Filter instances by tag
 aws ec2 describe-instances --filters  "Name=tag-key,Values=Stack" "Name=tag-value,Values=VAL3,VAL2" --query 'Reservations[*].Instances[*].[ImageId,InstanceId,Tags[?Key==`SomeKey`].Value | [0]]'
