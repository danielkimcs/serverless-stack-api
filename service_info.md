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

