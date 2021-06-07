Service Information
service: notes-api
stage: prod
region: us-east-1
stack: notes-api-prod
resources: 32
api keys:
  None
endpoints:
  POST - https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod/notes
  GET - https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  GET - https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod/notes
  PUT - https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  DELETE - https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
functions:
  create: notes-api-prod-create
  get: notes-api-prod-get
  list: notes-api-prod-list
  update: notes-api-prod-update
  delete: notes-api-prod-delete
layers:
  None

npx aws-api-gateway-cli-test \
--username='admin@example.com' \
--password='Passw0rd!' \
--user-pool-id='us-east-1_KzL3NF9bf' \
--app-client-id='qpekgcso2mebhcnup6mcurnb7' \
--cognito-region='us-east-1' \
--identity-pool-id='us-east-1:022f07b7-eb19-4798-8cb4-8ecfbb276b5f' \
--invoke-url='https://fn3o37cxvd.execute-api.us-east-1.amazonaws.com/prod' \
--api-gateway-region='us-east-1' \
--path-template='/notes' \
--method='POST' \
--body='{"content":"hello world","attachment":"hello.jpg"}'