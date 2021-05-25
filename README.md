# udacity-project2
1. Stack Name: udacity-project2-stack

2. Resource Template Name : Udacity_Project2.yml 

3. Parameters Template Name: Udacity_Project2_Parameters.json

4. Lucid charts AWS Project Diagram: Udacity Example AWS Diagram.pdf


# Output Load Balancer DNS URL: 
----------------------------------
http://udaci-WebAp-1HTALLUYNLT61-1782869306.us-west-2.elb.amazonaws.com


# Shell Scripts:
-----------------
create.sh:
aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --region=us-west-2 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

update.sh:
aws cloudformation update-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --region=us-west-2 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"


# Create Stack command using with shell script create.sh:
-------------------------------------------------------
./create.sh udacity_project2_stack Udacity_Project2.yml Udacity_Project2_Parameters.json 


# Update Stack command using with shell script update.sh:
--------------------------------------------------------
./update.sh udacity_project2_stack Udacity_Project2.yml Udacity_Project2_Parameters.json 

