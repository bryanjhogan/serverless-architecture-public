# Compute Services

## Lambda vs Fargate vs App Runner
### Lambda 
 - functions as a service 
 - on-demand, fast scaling
 - cold starts can be an issue 
 - pay for execution, not paying when not running
  
### Fargate and App Runner 
 - always running but with slower scaling
 - paying while running, even when not handling requests

## Orchestration of application

Step functions can connect most AWS services together and perform small pieces of logic like flow control and parallelization. 

# Foundational services

Identity and Access Management (IAM) - handles roles, permissions, and policies. Grants/denies access to services and resources.

CloudWatch - logging and monitoring, logs generated by services and your code.

X-Ray - trace requests as they pass through your system, analysis, debugging, and diagnostics.

# Data

S3 - object/file storage at a massive scale. 

DynamoDB - NoSQL database, best for key-value pairs.

Elastic File System (EFS) - an elastic file system that can be mounted to Lambda functions and Fargate, but not App Runner.

OpenSearch - a managed Elasticsearch-compatible search service

Relation Database Server Proxy (RDS Proxy) - proxies connections to RDS instances, especially useful for Lambda functions. Without this bursts of activity on Lambda can overwhelm a database.

Athena - query structured data stored in S3.

Aurora Serverless - MySQL, Postgres interfaces. Auto scales.

# Integration 

Step Functions - orchestration of services and logic. Lets you build state machines, and workflows co-ordinating your other services. 

Simple Queue Service (SQS) - serverless queues. Easily decoupling your services. A message in the queue is delivered to a single subscriber. Mainly for service/app to service/app.

Simple Notification Service (SNS) - publish/subscribe notification service, for both application to application, or for application to person (email, sms, etc). Can send to mutiple subscribers.

EventBridge - Event bus, to send events from services/applications to other services/applications. Easy way to wire up services. Events contain a lot of detail about what triggered them. Supports custom events.

An event can be sent to multiple targets. Supports filtering of events.

EventBridge scheduler - schedule events to be sent from EventBridge to services or applications. Works like a cron job.

API Gateway - create APIs, and route requests to applications or other services (e.g. Lambda functions, Fargate, Step Functions). Can be used to expose services publicly, e.g. use an API to forward a message to a queue.

Kinesis - like Simple Queue Service (SQS), but more commonly used for streaming data real-time data into applications or services. Can deliver a message to multiple subscribers. Can handle very high volumes of streaming data.

## Vision

### Rekognition 

 - detect and label objects in images
 - find text in an image
 - color analysis, brightness, sharpness, contrast
 - content moderation, block/warn if the content is deemed inappropriate
 - facial analysis - male/female, age range, eyes open, beard, mouth open, emotions, etc
 - celebrity recognition - determine if a celebrity is in the image
 - face comparison - check if a face is in an image or collection of images 
 - PPE detection - determine if the people in the image are wearing protective equipment 
 - recorded video analysis -  finds people, objects, and celebrities. Performs moderation on the video
 - streaming video analysis - notifies when a person, objects, etc are detected

### Lookout for Vision

 - detect defects/anomalies in images - can be used for quality control, detect defects.

## Text 

### Textract
 - document analysis - extract text, tables, forms, and key-value pairs from documents.
 - expense analysis - extract summaries and line items from receipts.
 - US driver's license and passport analysis - extract name, address, license number, date of birth, etc.

### Comprehend text analysis
 - detect entities - people, places, organizations, dates, quantities, etc.
 - identify key phrases, sentiment (neutral, positive, negative, mixed), PII, and language used.

### Translate 
 - translate text between languages.
 - can be performed in real-time or batch.

## Audio 

### Transcribe
 - transcribe audio to text.
 - identify speakers by voice or audio channel.

### Polly
 - text to speech.
 - multiple voices, multiple languages.

## Other 

### Personalize
 - recommendation engine - recommend products, movies, hotels, etc.

### Augmented AI A2I
 - human review of machine learning results
 - set a confidence threshold, and if the confidence is below the threshold, the result is sent to a human for review