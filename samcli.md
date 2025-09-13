[*] Create pipeline: cd projsam && sam pipeline init --bootstrap
[*] Validate SAM template: cd projsam && sam validate
[*] Test Function in the Cloud: cd projsam && sam sync --stack-name {stack-name} --watch


sam buid
sam deploy --guided

In yaml  file

Transform, Resources block is mandatory


sam local invoke HelloWorldFunction --event events/event.json
-> HelloWorldFunction mentioned in yaml file

sam local invoke HelloWorldFunction --event events/event.json


aws lambda invoke --invocation-type Event --function-name lambda_func_name outputfile.txt
aws lambda invoke --invocation-type RequestResponse --function-name <function_name> --payload "data" outputfile.txt
aws lambda invoke --invocation-type RequestResponse --function-name <func_name> outputfile.txt


sam local start-api -> it will work on local url

sam delete --stack-name <stack_name>

