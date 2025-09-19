# DND-automation-and-MSISDN-lookup-
for a telecommunication company where MSISDN lookup and DND is a crucial task to done on daily bases which is really time and resource consuming  . I have designed a automation process that fetch the file name form S3 bucket and send the response via mail 

Replace the variable 

this is the automation script that work on the base script 

schedule this script into the cron in every 1o minutes

suppose if we want to delecte x numbers in permanent dnd 

we would craete a text fiel with name "filename.txt"
with input formet 53685******,add,permanent if u want to add he numbers into permanent dnd 
                  53685******,add,critical  if add into critical
                  53685******,delete,permanent if u want to delete/remove form permanet dnd
                  53685******,delete,critical if you want to delete/remove form critical dnd
every number in the file should follow the formet number,add/delete,permanent/critical

for example if i want to add some numbers in permanent dnd , some numbers in critical and some numbers to delete from dnd i would create the file 
"**file-name.txt**"
6253472*****,add,permanent
635873*****,add,permanent
6347451872****,delete,permanet
63547254****,add,permanent
654825*****,delete,critical

and send to the s3 bucket 

when the script would run in 10 minute teh script would pick teh file and perform the following action and generate a mail that teh following action has been done with teh details of teh numbers present in the database.


