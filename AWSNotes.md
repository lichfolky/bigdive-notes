## AWS for Data
Alex Comunian
By ThroughtWorks

### Environment
development->production

**local machine** good for:
+ develop initial version of the process
+ try it on a small dataset
+ no need of external resources

We can't use our local machine to deploy, possible constraints:
+ access data (big, permission )
+ security
+ memory
+ time constraints
+ tech. infrastructure

we should deploy in a production Environment

**Cloud computing** is on-demand availability of computer system resources. Data storage and computing power without active management by user.

### CloudSolution, AWS

#### Compute

**EC2 virtual servers in the cloud**
secure and resizable computing resource

**Lambda function**
to run code with no administration, automatic scaling and availability, stateless

#### Database

+ **Dynamo DB**: Key-value and Document DB
+ Relational database services (**RDS**)
+ **Amazon document DB**: based on MongoDB API

#### Storage

There's **Amazon S3**!

#### Analytics

**Kinesis** realtime processing, data indigestion for ML and Analytics

+ **data stream**
+ **data firehose**, you don't store data
+ **data pipeline**, to automize transfers and transformations

**EMR elastic map reduce cluster** TO KNOW

### Cloudformation

 **JSON** or **YAML** configuration files


### from Data Warehouses to Data Lake

*PRO:*
+ single schema
+ direct access to the database for querying

*CONS:*
+ centralized access: everybody use the same resources
+ no flexibility: we have a single scheme
+ cost
+ availability

**DataLake**
+ it's **raw data**
+ **Schema Less**
+ **Immutable**: because most of the time it's for historical dataset

**S3 bucket**
divided by date
Apache Parquet column-oriented Data Storage Format Open source

## Exercise

docker-compose
ps

**Docker**
**LocalStack** AWS simulator

pandas works with aws s3 read_csv('s3://...')

Kinesis
shardId -> ShardIterator

nextShharditerator
it's better to not take a single record but a bunch of them
